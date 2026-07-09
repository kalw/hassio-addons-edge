- fix: remove leading slash from ingress_entry to fix ingress 404 (#25)

* fix: correct ingress_entry path to /ui/

Vault's UI is served at /ui/ (not /ui/vault/ which is a client-side
router path within the SPA). Setting ingress_entry to /ui/vault/ caused
vault to 404 the server-side request.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

* fix: remove leading slash from ingress_entry to fix 404

Supervisor builds ingress_url as token_path + ingress_entry. With
ingress_entry: /ui/ (leading slash), this produces //ui/ which returns 404.
Changing to ui/ produces the correct /api/hassio_ingress/<token>/ui/.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

---------

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
