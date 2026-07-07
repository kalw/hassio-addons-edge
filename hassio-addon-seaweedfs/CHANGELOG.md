- fix: restore nginx install and bind to 0.0.0.0 for external S3 access (#47)

* fix: restore nginx install and correct BUILD_FROM regressed in slug rename PR

The slug rename PR (#42) was branched off an older commit, accidentally
dropping the nginx install (PR #39) and reverting BUILD_FROM back to
the inaccessible ghcr.io/hassio-addons/base image.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

* fix: bind to 0.0.0.0 instead of 127.0.0.1 to allow external S3 access

With -ip=127.0.0.1, all services listen on loopback only so the port
mapping in the addon config (8333/tcp) cannot forward traffic into the
container. Removing -ip lets SeaweedFS auto-detect the container IP and
bind to all interfaces. Volume registration stays explicit via
-volume.publicUrl=127.0.0.1:8080 so internal peer communication works.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

---------

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
