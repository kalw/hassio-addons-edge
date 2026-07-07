- fix: add init: false to prevent Docker wrapping s6-overlay (#3)

Without init: false, HA starts the container with Docker's tini as
PID 1, pushing s6-overlay to PID 2. s6-overlay-suexec then fatal-errors
because it requires being PID 1.

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
