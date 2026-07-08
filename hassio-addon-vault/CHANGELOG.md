- fix: use RSA key type for GPG key generation (#18)

Key-Type: default resolves to ed25519 in newer GPG, but the Alpine
libgcrypt in the base image does not support that curve, causing:
  gpg: key generation failed: Unknown elliptic curve

Switch to RSA 4096 which is universally supported across all libgcrypt
versions shipped with current Alpine-based Hass.IO base images.

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
