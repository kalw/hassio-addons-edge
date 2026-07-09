- fix: fix shim JS syntax and add service worker patch (#28)

- Use getElementsByName instead of querySelector to avoid backslash-escaping
  issues in the bash heredoc that produced a JS SyntaxError at runtime
- Patch navigator.serviceWorker.register so sw.js is fetched through
  the ingress path instead of hitting ha.indolore.net/ui/sw.js directly

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
