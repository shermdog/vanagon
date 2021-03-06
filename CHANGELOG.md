# Change Log
All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/).

This changelog adheres to [Keep a CHANGELOG](http://keepachangelog.com/).

## [Unreleased]

## [0.3.17] - 2015-10-02
### Added
- Initial support for custom pre- and post-install actions from the component
  level. Currently implemented for RPM, we will expand that as needed.
- platform_triple now available as a platform DSL method. Very useful when
  cross-compiling.
- replaces and provides are now available in the project DSL (they were
  previously only available in the component DSL)

### Changed
- apply_patch component DSL method now accepts fuzz and strip as arguments for
  patches that don't apply cleanly with just -p1. patch application now ignores
  whitespace by default

## [0.3.16] - 2015-09-24
### Fixed
- Configfiles installed explicitly on debian

## [0.3.15] - 2015-09-22
### Added
- Support for AIX services
- .sh and .csh added as valid plaintext file sources
- WindRiver Linux added as a distinct platform type subclassing RPM

### Changed
- File/configfile implementation refactored to remove duplicate file issues in
  rpm packaging.

### Fixed
- AIX rpm spec no longer requires chkconfig

### Removed
- aix_package dsl method was removed. Packages desired for a build should be
  added as build_requires or via platform provisioning.

## [0.3.14] - 2015-09-15
### Changed
- OSX packages no longer include the platform codename and instead use
  the platform version.

## [0.3.13] - 2015-09-14
### Added
- Pooler engine now has token support to ensure long template life. Use
  VMPOOLER_TOKEN environment variable or write token into ~/.vanagon-token

### Changed
- Noarch project method is now applied to solaris packages

### Fixed
- Cross compiles will no longer attempt to install the produced package on
  solaris 11.

## [0.3.12] - 2015-09-03
### Changed
- Empty directories now included in vanagon builds

### Fixed
- Broken usage of ips_version fixed for solaris 11

## [0.3.11] - 2015-09-02
### Added
- Solaris 11 support
- Support a custom release string in package names
- Support platform-specific 'install' commands
- Miscellaneous updates to better support Mac OS X, Solaris, and AIX

### Changed
- Updated Mac OS X package name and directory structure to match other platforms

## [0.3.10] - 2015-08-26
### Added
- Added a CHANGELOG.md to track high level user facing changes
- Include HuaweiOS for RPM5 tweaks

### Changed
- Update vanagon_hosts.log format to use FQDN instead of the short name
- Updates to RPM scriptlets for consistency and better handling of upgrades

## Versions <= 0.3.9 do not have a change log entry

[Unreleased]: https://github.com/puppetlabs/vanagon/compare/0.3.17...HEAD
[0.3.17]: https://github.com/puppetlabs/vanagon/compare/0.3.16...0.3.17
[0.3.16]: https://github.com/puppetlabs/vanagon/compare/0.3.15...0.3.16
[0.3.15]: https://github.com/puppetlabs/vanagon/compare/0.3.14...0.3.15
[0.3.14]: https://github.com/puppetlabs/vanagon/compare/0.3.13...0.3.14
[0.3.13]: https://github.com/puppetlabs/vanagon/compare/0.3.12...0.3.13
[0.3.12]: https://github.com/puppetlabs/vanagon/compare/0.3.11...0.3.12
[0.3.11]: https://github.com/puppetlabs/vanagon/compare/0.3.10...0.3.11
[0.3.10]: https://github.com/puppetlabs/vanagon/compare/0.3.9...0.3.10
