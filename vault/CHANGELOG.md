- fix: Renovate token and hassio-addon-vault image slug (#2)

* fix: use GITHUB_TOKEN for Renovate workflow

RENOVATE_TOKEN secret is not configured in this repo; GITHUB_TOKEN
is automatically available and has sufficient write access for
Renovate to open PRs within the same repository.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

* fix: use hassio-addon-vault as image slug for GHCR naming

Override the slug in both deploy workflows so images are pushed to
ghcr.io/kalw/hassio-addon-vault/{arch} instead of ghcr.io/kalw/vault/{arch}.
The addon slug in config.yaml stays 'vault' (HA identifier is unchanged).

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

---------

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
