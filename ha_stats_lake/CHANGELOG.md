- fix(consolidate): use path-style S3 URLs for custom endpoints (#20)

* fix(consolidate): use path-style S3 URLs for custom endpoints

DuckDB defaults to virtual-hosted style (bucket.endpoint/key) which
breaks S3-compatible stores like SeaweedFS and MinIO that expect
path-style (endpoint/bucket/key). Set URL_STYLE 'path' whenever a
custom endpoint is configured; fall back to 'vhost' for AWS.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

* fix(consolidate): honour http:// scheme — set USE_SSL false for plain HTTP endpoints

DuckDB ignores the scheme prefix and always uses HTTPS by default.
Detect http:// explicitly and pass USE_SSL false so plain-HTTP S3
endpoints (local SeaweedFS, MinIO without TLS) work correctly.

Tested against SeaweedFS over HTTPS: 72 rows written, parquet confirmed on S3.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

---------

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
