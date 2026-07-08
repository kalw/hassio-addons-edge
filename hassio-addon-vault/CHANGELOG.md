- fix: upgrade vault 1.6.2→1.21.4 and terraform 0.14.3→1.15.8 (#20)

* fix: upgrade vault 1.6.2→1.21.4 and terraform 0.14.3→1.15.8

Vault 1.6.2 (2021) is incompatible with the current hashicorp/vault
terraform provider (v5.x) which calls GET /v1/sys/mounts/auth/<path> —
an endpoint that returns 405 on vault 1.6.x. Upgrading vault to 1.21.4
makes the full current provider API available without version pinning.

Terraform is bumped from 0.14.3 to 1.15.8 (current stable) in the same
pass; the vault.tf.template HCL is compatible with no changes.

Note: existing Raft data from vault 1.6.x may not migrate cleanly across
15 minor versions. Users with existing vault data should back up
/data/vault before updating.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

* ci: retrigger build after transient download failure

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

* fix: use unzip -p to avoid busybox data-descriptor incompatibility

Terraform 1.15.8 zip entries have flag_bits=0x0008 (data descriptor),
meaning file sizes are stored after the data rather than in the local
header. Alpine's busybox unzip cannot handle this and exits with
"EOF or read error, treating as [N]one". Vault 1.21.4 uses
flag_bits=0x0000 so it was unaffected.

Switch from `unzip -d /bin <archive>` to `unzip -p <archive> <entry>
> /bin/<entry>` which pipes the entry to stdout (no size needed in
the local header) for both vault and terraform. Also removes LICENSE.txt
from /bin which was a side-effect of the old approach.

Co-Authored-By: Claude Sonnet 4.6 <noreply@anthropic.com>

---------

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
