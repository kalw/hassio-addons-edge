- fix: install gnupg in Docker image (#17)

init.sh uses gpg to generate a key pair that encrypts vault's unseal
keys and root token before init. Without gnupg, every start fails at
generate_gpg_key with "gpg: command not found", causing a restart loop.

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
