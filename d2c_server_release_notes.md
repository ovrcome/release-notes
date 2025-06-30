# Release notes for oVRcome's D2C Server Software

This file contains public release notes for oVRcome's direct-to-consumer Server Software.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.2.3] - 2025-06-30 - Exposure viewing improvements

### Changed

- Change logic around viewing exposures and when we allow users to continue to the next one.

### Removed

- Removed deprecated monitoring code.

## [1.2.2] - 2025-06-30 - Backend Improvements

### Removed

- Remove support for retired program type.
- Remove retired logistics method.

### Changed

- Simplify triggers API due to removal of retired program type.

## [1.2.1] - 2025-06-24 - Backend Improvements

### Changed

- Updates to onboarding process for bespoke customers.

### Removed

- Removed retired CRM sync code.

## [1.2.0] - 2025-05-28 - Subscription management improvements

### Added

- Backend changes for subscription management, preparing for D2C special offers.
- Developer tooling improvements.

## [1.1.2] - 2025-05-27 - Backend Improvements

### Removed

* Remove deprecated/unused purchase pages.

## [1.1.1] - 2025-05-20 - Backend Improvements

### Added

* Improved deploy process.

### Fixed

* Fix access issues for annual and in-app subscriptions.
* Improvements to password reset process.

## [1.1.0] - 2025-05-15 - Backend Improvements

### Changed

- Updates to source code hosting and deployment processes.

### Added

- Added better suited API for web onboarding to call to fetch delivery methods.

### Removed

- Removed deprecated logistics handling methods.

## [1.0.11] - 2025-05-13 - Backend Improvements

### Added

- Preparations for D2C special offers.

### Changed

- Tweaks to testing process.
- Fixed invalid registration path for parents program.
- Fixed handling of subscriptions for subscriptions purchased in-app.

### Removed

- Remove bespoke reporting for a discontinued program.
- Removed deprecated code from very early app release.

## [1.0.10] - 2025-03-28 - Device Compatibility Search Improvements

### Fixed

- Fix opening links from the device compatibility tool.

## [1.0.9] - 2025-03-27 - Onboarding Improvements

### Added

- Add a note during web onboarding about Meta & Pico headset compatibility.

## [1.0.8] - 2025-03-27 - Onboarding Improvements

### Changed

- Improved messaging and handling of promotional offers when subscribing online.
- Fix embedding of device compatibility page.

## [1.0.7] - 2025-03-25 - Device Compatibility Search Improvements

### Changed

* New design for device compatibility page.
* Update device compatibility database.

## [1.0.6] - 2025-03-18 - Stability Improvements

### Changed

* Upgrade of infrastructure tooling to latest version.
* Fix sporadic request error when processing payments.
* Improvements to children & adolescents program subscription handling.
* Infrastructure stability improvements.

## [1.0.5] - 2025-03-03 - Subscription Bug Fixes

### Fixed

* Fix display of recurring amount for old subscriptions.

## [1.0.4] - 2025-02-10 - Vaping Program Individualisation

### Added

- AI hierarchy individualisation for vaping programs.

## [1.0.3] - 2025-02-07 - Fix Subscription Handling

### Fixed

- Fix error handling subscriptions that are no longer recurring.

## [1.0.2] - 2025-01-14 - Custom Report Updates

### Fixed

- Minor tweaks to a customer custom report.

## [1.0.1] - 2025-01-14 - Custom Report Updates

### Fixed

- Minor tweaks to a customer custom report.

## [1.0.0] - 2025-01-13 - Initial versioned release

### Added

- Beginning version numbering at 1.0.0 with this release.

### Removed

- The D2C server no longer reports data to Honeybadger. We no longer use this monitoring service.
