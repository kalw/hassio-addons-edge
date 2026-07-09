# ![Project Stage][project-stage-shield] Home Assistant Community Add-ons

![Project Stage][project-stage-shield]
![Maintenance][maintenance-shield]
[![License][license-shield]](LICENSE.md)

[![Discord][discord-shield]][discord]
[![Community Forum][forum-shield]][forum]

## WARNING! THIS IS AN EDGE VERSION!

This Home Assistant Add-ons repository contains edge builds of add-ons.
Edge builds add-ons are based upon the latest development version.

- They may not work at all.
- They might stop working at any time.
- They could have a negative impact on your system.

This repository was created for:

- Anybody willing to test.
- Anybody interested in trying out upcoming add-ons or add-on features.
- Developers.

If you are more interested in stable releases of our add-ons:

<https://github.com/kalw/hassio-addons>


## Installation

Adding this add-ons repository to your Home Assistant instance is
pretty straightforward. In the Home Assistant add-on store,
a possibility to add a repository is provided.

Use the following link to add this repository:

[![Open your Home Assistant instance and show the add add-on repository dialog with a specific repository URL pre-filled.](https://my.home-assistant.io/badges/supervisor_add_addon_repository.svg)](https://my.home-assistant.io/redirect/supervisor_add_addon_repository/?repository_url=https%3A%2F%2Fgithub.com%2Fkalw/hassio-addons-edge)


.. or use the following URL to add this repository:

```txt
https://github.com/kalw/hassio-addons-edge
```


## Add-ons provided by this repository

### &#10003; [HA Stats Lake][addon-hassio-addon-stats-lake]

![Latest Version][hassio-addon-stats-lake-version-shield]
![Supports armhf Architecture][hassio-addon-stats-lake-armhf-shield]
![Supports armv7 Architecture][hassio-addon-stats-lake-armv7-shield]
![Supports aarch64 Architecture][hassio-addon-stats-lake-aarch64-shield]
![Supports amd64 Architecture][hassio-addon-stats-lake-amd64-shield]
![Supports i386 Architecture][hassio-addon-stats-lake-i386-shield]

Long-term storage for Home Assistant sensor data. Samples a list of entities every 30 minutes to per-entity monthly CSVs, then consolidates nightly into a DuckLake (Parquet) on any S3-compatible store and optionally syncs raw CSVs to any rclone remote.

[:books: HA Stats Lake add-on documentation][addon-doc-hassio-addon-stats-lake]

### &#10003; [Hashicorp Vault Addon][addon-hassio-addon-vault]

![Latest Version][hassio-addon-vault-version-shield]
![Supports armhf Architecture][hassio-addon-vault-armhf-shield]
![Supports armv7 Architecture][hassio-addon-vault-armv7-shield]
![Supports aarch64 Architecture][hassio-addon-vault-aarch64-shield]
![Supports amd64 Architecture][hassio-addon-vault-amd64-shield]
![Supports i386 Architecture][hassio-addon-vault-i386-shield]

Add-on that launch an Hashicorp Vault server

[:books: Hashicorp Vault Addon add-on documentation][addon-doc-hassio-addon-vault]

### &#10003; [SeaweedFS][addon-hassio-addon-seaweedfs]

![Latest Version][hassio-addon-seaweedfs-version-shield]
![Supports armhf Architecture][hassio-addon-seaweedfs-armhf-shield]
![Supports armv7 Architecture][hassio-addon-seaweedfs-armv7-shield]
![Supports aarch64 Architecture][hassio-addon-seaweedfs-aarch64-shield]
![Supports amd64 Architecture][hassio-addon-seaweedfs-amd64-shield]
![Supports i386 Architecture][hassio-addon-seaweedfs-i386-shield]

SeaweedFS S3-compatible distributed object storage

[:books: SeaweedFS add-on documentation][addon-doc-hassio-addon-seaweedfs]

## Releases

Add-on releases are **NOT** based on [Semantic Versioning][semver], unlike
all our other repositories. The latest build commit SHA hash of each
add-on, represents the version number.

## Support

Got questions?

You have several options to get them answered:

- The Home Assistant Community Add-ons [Discord Chat Server][discord]
- The Home Assistant [Community Forum][forum].
- The Home Assistant [Discord Chat Server][discord-ha].
- Join the [Reddit subreddit][reddit] in [/r/homeassistant][reddit]

You could also open an issue here on GitHub. Note, we use a separate
GitHub repository for each add-on. Please ensure you are creating the issue
on the correct GitHub repository matching the add-on.

- [Open an issue for the add-on: HA Stats Lake][hassio-addon-stats-lake-issue]
- [Open an issue for the add-on: Hashicorp Vault Addon][hassio-addon-vault-issue]
- [Open an issue for the add-on: SeaweedFS][hassio-addon-seaweedfs-issue]

For a general repository issue or add-on ideas [open an issue here][issue]

## Contributing

This is an active open-source project. We are always open to people who want to
use the code or contribute to it.

Thank you for being involved! :heart_eyes:

## Adding a new add-on

We are currently not accepting third party add-ons to this repository.

For questions, please contact [Kalw][kalw]:


## License

MIT License

Copyright (c) 2018-2024 Franck Nijhof

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

[addon-hassio-addon-stats-lake]: https://github.com/kalw/hassio-addon-stats-lake/tree/3e2df71
[addon-doc-hassio-addon-stats-lake]: https://github.com/kalw/hassio-addon-stats-lake/blob/3e2df71/README.md
[hassio-addon-stats-lake-issue]: https://github.com/kalw/hassio-addon-stats-lake/issues
[hassio-addon-stats-lake-version-shield]: https://img.shields.io/badge/version-3e2df71-blue.svg
[hassio-addon-stats-lake-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[hassio-addon-stats-lake-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[hassio-addon-stats-lake-armhf-shield]: https://img.shields.io/badge/armhf-no-red.svg
[hassio-addon-stats-lake-armv7-shield]: https://img.shields.io/badge/armv7-no-red.svg
[hassio-addon-stats-lake-i386-shield]: https://img.shields.io/badge/i386-no-red.svg
[addon-hassio-addon-vault]: https://github.com/kalw/hassio-addon-vault/tree/7edb75e
[addon-doc-hassio-addon-vault]: https://github.com/kalw/hassio-addon-vault/blob/7edb75e/README.md
[hassio-addon-vault-issue]: https://github.com/kalw/hassio-addon-vault/issues
[hassio-addon-vault-version-shield]: https://img.shields.io/badge/version-7edb75e-blue.svg
[hassio-addon-vault-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[hassio-addon-vault-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[hassio-addon-vault-armhf-shield]: https://img.shields.io/badge/armhf-no-red.svg
[hassio-addon-vault-armv7-shield]: https://img.shields.io/badge/armv7-no-red.svg
[hassio-addon-vault-i386-shield]: https://img.shields.io/badge/i386-no-red.svg
[addon-hassio-addon-seaweedfs]: https://github.com/kalw/hassio-addon-seaweedfs/tree/64a6af8
[addon-doc-hassio-addon-seaweedfs]: https://github.com/kalw/hassio-addon-seaweedfs/blob/64a6af8/README.md
[hassio-addon-seaweedfs-issue]: https://github.com/kalw/hassio-addon-seaweedfs/issues
[hassio-addon-seaweedfs-version-shield]: https://img.shields.io/badge/version-64a6af8-blue.svg
[hassio-addon-seaweedfs-aarch64-shield]: https://img.shields.io/badge/aarch64-yes-green.svg
[hassio-addon-seaweedfs-amd64-shield]: https://img.shields.io/badge/amd64-yes-green.svg
[hassio-addon-seaweedfs-armhf-shield]: https://img.shields.io/badge/armhf-no-red.svg
[hassio-addon-seaweedfs-armv7-shield]: https://img.shields.io/badge/armv7-no-red.svg
[hassio-addon-seaweedfs-i386-shield]: https://img.shields.io/badge/i386-no-red.svg
[discord-ha]: https://discord.gg/c5DvZ4e
[discord-shield]: https://img.shields.io/discord/478094546522079232.svg
[discord]: https://discord.me/hassioaddons
[forum-frenck]: https://community.home-assistant.io/u/frenck/?u=frenck
[forum-shield]: https://img.shields.io/badge/community-forum-brightgreen.svg
[forum]: https://community.home-assistant.io?u=frenck
[kalw]: https://github.com/kalw
[issue]: https://github.com/kalw/hassio-addons-edge/issues
[license-shield]: https://img.shields.io/github/license/kalw/hassio-addons-edge.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2025.svg
[project-stage-shield]: https://img.shields.io/badge/project%20stage-experimental-yellow.svg
[reddit]: https://reddit.com/r/homeassistant
[semver]: http://semver.org/spec/v2.0.0.html
[third-party-addons]: https://home-assistant.io/hassio/installing_third_party_addons/