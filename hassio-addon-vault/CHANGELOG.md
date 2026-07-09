- fix: patch Ember rootURL meta tag so Vault UI routes correctly via ingress

Vault's Ember SPA (locationType=history) reads rootURL from the
vault/config/environment meta tag. With rootURL=/ui/ and the browser URL
at /api/hassio_ingress/<token>/ui/, Ember can't match any route → 404.

Extend the injected shim to decode that meta tag before Ember boots,
prepend the X-Ingress-Path value to rootURL, and re-encode it.
Ember then sees rootURL=/api/hassio_ingress/<token>/ui/ and routes correctly.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>
