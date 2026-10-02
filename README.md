# PiSugar kernel modules

This repository builds and archives precompiled PiSugar desktop battery modules.
It runs daily, obtains Raspberry Pi OS kernel headers, and builds the module
source from `PiSugar/pisugar-power-manager-rs`.

Each exact kernel ABI is published as a GitHub Release:

* branch: `kernel/<uname -r>`
* tag and Release: `kernel-<uname -r>`
* asset: `pisugar-module_<uname -r>_<arm64|armhf>.tar.gz`

The release assets are the source of truth. The power-manager installer first
downloads the exact matching asset; if it is not available, it builds locally.
