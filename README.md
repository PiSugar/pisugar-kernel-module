# PiSugar kernel modules

This repository builds and archives precompiled PiSugar desktop battery modules.
It runs daily, obtains Raspberry Pi OS kernel headers, and builds the module
source from `PiSugar/pisugar-power-manager-rs`.

Each numeric kernel version is published as a pre-release:

* branch: `kernel/<major.minor.patch>`
* tag and Release: `kernel-<major.minor.patch>`
* asset: `pisugar-module_<uname -r>_<arm64|armhf>.tar.gz`

The release assets are the source of truth. The power-manager installer first
downloads the exact matching asset; if it is not available, it builds locally.

`Backfill historical Raspberry Pi kernel modules` is a manual-only workflow
for rebuilding supported historical headers retained in Raspberry Pi's official
package pool.
