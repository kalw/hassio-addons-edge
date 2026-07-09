- fix: correct ingress_entry path to /ui/ (#24)

Vault's UI is served at /ui/ (not /ui/vault/ which is a client-side
router path within the SPA). Setting ingress_entry to /ui/vault/ caused
vault to 404 the server-side request.

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
