# cygpkg
## Setup
1. Add the cygpkg script to `/usr/bin`.
2. Mark cygpkg executable `chmod +x /usr/bin/cygpkg`.
3. Head over to https://cygwin.com/mirrors.html and pick a download mirror.
4. Set the mirror in `cygpkg`
        MIRROR=http://cygwin.mirror.constant.com/
5. Run `cygpkg update` to grab the cygwin setup.exe
6. Install curl or wget to help with `cygpkg update`.
        cygpkg install curl

## Usage
        # download an updated cygwin setup.exe 
        cygpkg update

        # search for package wget
        # only show packages that have wget in their
        # command line description
        cygpkg search wget

        # search for packages and output everything from cygcheck
        cygpkg search --all wget

        # install package
        cygpkg install wget

        # upgrade all installed packages
        cygpkg upgrade

## TODO
- Move mirror to a config file in etc. and add a mirror-select option. Scrape https://cygwin.com/mirrors.html for choices
- investigate integrating other package managers like NetBSD pkgsrc or chocolatey
