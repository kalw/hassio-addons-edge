- fix: strip CSP and X-Frame-Options headers to allow HA ingress iframe (#26)

Vault sets Content-Security-Policy: frame-ancestors 'none' and X-Frame-Options
which block the HA ingress iframe. Strip them in nginx so the UI loads.

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
