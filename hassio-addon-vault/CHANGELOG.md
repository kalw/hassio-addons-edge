- fix: inject <base href> so Vault Ember SPA routes correctly via ingress (#27)

Vault's compiled HTML has no <base> tag. Ember's router uses its built-in
rootURL (/ui/) which doesn't match the browser URL when served through HA
ingress (/api/hassio_ingress/<token>/ui/), causing a 404 on all routes.
Injecting <base href="$http_x_ingress_path/ui/"> after <head> lets Ember
read the correct rootURL at runtime.

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
