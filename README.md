## Fast Align Debian Package

This repository contains the latest version (master branch) of [fast_align](https://github.com/clab/fast_align) packaged for Debian/Ubuntu/derivatives.

### Development

#### Installation

In order to produce `.debs`, you should first install, on a Debian-based distro:

    sudo apt install dh-make fakeroot devscripts build-essential

Then, you should install this package's build dependencies:

    sudo apt install cmake libgoogle-perftools-dev libsparsehash-dev

#### Packaging

From within the `fast-align-[VERSION]` folder, run:

    debuild -uc -us

This will compile and produce the `.deb` package in the upper directory.

#### Merging upstream changes

The `fast-align-[VERSION]` is essentially a simple clone of the upstream sources with a special extra `Makefile`, `.gitignore` and `debian/` folders.

In order to merge changes from upstream, you should clone the latest version in a new `fast-align-[VERSION]` folder and copy over the `Makefile`, `.gitignore` and the `debian/` folder. `[VERSION]` should be the date of the latest commit, in `YYYY.MM.DD` format. Then, just change the `debian/` folder's contents to match the new version of the package, its name and maintainer. Essentially open all the text files in your preferred code editor and perform any required changes.

Afterwards, just follow [Packaging](#packaging).