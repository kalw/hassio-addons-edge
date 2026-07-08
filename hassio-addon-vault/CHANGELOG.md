- fix: add version resolvers to release-drafter config (#16)

Without name-template, tag-template, and version-resolver, release-drafter
produces a draft release with an empty tag_name when there is no prior
non-draft release to compute a version from. The repository-updater then
hits `semver.parse_version_info("")` and crashes.

Add explicit version resolvers matching the standard hassio-addons label
convention. This matches the pattern used by hassio-addon-seaweedfs.

Co-authored-by: release-bot <release-bot@ci.net>
Co-authored-by: Claude Sonnet 4.6 <noreply@anthropic.com>
