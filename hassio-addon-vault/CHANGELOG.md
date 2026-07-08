- fix: add disable_mlock = true to vault.hcl template (#21)

Vault 1.20+ requires disable_mlock to be set explicitly; previously it
defaulted to false. HA addon containers cannot use mlock (no CAP_IPC_LOCK
by default), so true is the correct value here. Without this, vault
crashes on startup with "disable_mlock must be configured 'true' or
'false'".

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
