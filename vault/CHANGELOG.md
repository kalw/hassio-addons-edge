- fix: rename image to ghcr.io/kalw/hassio-addon-vault/{arch}

The bare 'vault' package name was ambiguous in GHCR alongside other
unrelated vault images; prefixing with hassio-addon-vault matches the
repo name and makes it clear this is the HA addon image.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>
