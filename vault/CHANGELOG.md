- revert: restore vault image to ghcr.io/kalw/vault/{arch}

The deploy workflow uses the slug field (vault) to name the pushed image,
not the image field. Changing image: created a mismatch — HA tried to pull
from hassio-addon-vault/{arch} while the workflow kept pushing to vault/{arch}.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>
