- fix: use ip.bind=0.0.0.0 for external access, ip=127.0.0.1 for stable discovery

Without -ip, SeaweedFS auto-detects the container IP which can be
unreliable in the HA supervisor network, causing volume server to fail
registration (0 node candidates). With -ip=127.0.0.1, all internal
component discovery stays on stable loopback. -ip.bind=0.0.0.0 makes
all services (including S3 port 8333) listen on all interfaces so
the addon port mapping works.

Also removes the hardcoded amd64 default from ARG BUILD_FROM — the
build system always passes the correct arch-specific image via build.yaml.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>
