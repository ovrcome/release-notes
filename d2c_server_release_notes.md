# Release notes for oVRcome's D2C Server Software

This file contains public release notes for oVRcome's direct-to-consumer Server Software.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.4.17] - 2026-01-15 - Backend Improvements

### Added

- Updates for new real world challenge functionality.

### Removed

- Remove deprecated Firebase code.

### Changed

- Improvements to developer experience.

### Updated

- Update shared dependencies to latest version.

## [1.4.16] - 2025-12-07 - Backend Improvements

### Added

- Improvements to CI visibility.

### Changed

- Fix contributors not being able to log in.

## [1.4.15] - 2025-11-27 - Administration Improvements

### Fixed

- Fix activation date formatting in bespoke reporting.

### Changed

- Use SSO for admin logins.

## [1.4.14] - 2025-11-24 - Administration Improvements

### Changed

- Fix logging unsatisfactory VR calibration feedback.
- Fix error storing triggers.
- Improved admin search interfaces.
- Fix headset delivered not being recorded for plan sales.

## [1.4.13] - 2025-11-20 - Administration Improvements

### Changed

- Revamp of admin UI for viewing client progress and details.
- Enhancements to CI process.

## [1.4.12] - 2025-11-12 - Backend Improvements

### Added

- Better control over what videos end up in generated hierarchies.
- Extract hierarchy generator as external service.

### Fixes

- Fix for incorrect reporting of progress in bespoke reporting.
- Fix for extra events being created.

## [1.4.11] - 2025-11-03 - Administration Improvements

### Changed

- Improvements to admin interface for viewing user progress.

## [1.4.10] - 2025-10-30 - Backend Improvements

### Fixed

- Fix issue causing duplicate database records for storing sync data.

## [1.4.9] - 2025-10-28 - Backend Improvements

### Removed

- Removed deprecated video analysis service.

### Changed

- Improved performance of background messaging sync task.

### Fixed

- Fix failure to process subscription data webhook in certain rare scenarios.

## [1.4.8] - 2025-10-23 - Backend Improvements

### Added

- Database updates to label AI generated content.
- Administration updates to allow sending push notifications to app.

### Fixes

- Improve speed and reliability of sign up communictions.

## [1.4.7] - 2025-10-21 - Backend Improvements

### Fixed

- Fix error generating hierarchies with large pools of available videos.

### Added

- Backend functionality to collect GIC score from users.
- Backend functionality to collect calibration feedback from users.

## [1.4.6] - 2025-10-19 - Administration improvements

### Fixed

- Allow adding historical communication logs.

## [1.4.5] - 2025-10-15 - Backend Improvements

### Added

- Better tracking of client communication.
- Tweaks to bespoke reporting.

### Updated

- Update dependencies with recent security updates.

## [1.4.4] - 2025-10-12 - Dependency Updates

### Changed

- Update system dependencies with security updates.

## [1.4.3] - 2025-10-08 - Backend Improvements

### Changed

- Improve automation of NZ shipping process.

## [1.4.2] - 2025-10-05 - Backend Improvements

### Fixed

- Better tracking of delivery date for sales.
- Ensure subscriptions are cancelled when removing a user.
- Improvements to hierarchy generator.
- Improvements to viewing sale receipts and shipping invoices in certain rare scenarios.

## [1.4.1] - 2025-09-25 - Backend Improvements

### Changed

- Expose additional details to app API.
- Tweaks to bespoke reporting.

## [1.4.0] - 2025-09-24 - Backend Improvements

### Removed

- Retired old therapist, children & adults dashboard.

### Added

- Improved logging context for background jobs.
- Improvements for customer support visibility of headset details.

### Changed

- Prevent duplicate subscriptions for users.

## [1.3.15] - 2025-09-19 - Backend Improvements

### Changed

- Improvements to bespoke reporting.
- Improvements to shipping logistics.

## [1.3.14] - 2025-09-16 - Backend Improvements

### Changed

1. Minor fixes to video content syncing.
2. Improved tracking of video views.
3. Simplified generation of survey results.

## [1.3.13] - 2025-09-09 - Backend Improvements

### Added

- Additional reporting added for users who fail to complete onboarding.
- Added bespoke reporting.

### Changed

- Tweaks to how hierarchies are regenerated.
- Fix error when accessing order tracking page.

## [1.3.12] - 2025-09-06 - API Fix

### Fixed

- Hotfix for timeout when loading D2C program data.

## [1.3.11] - 2025-09-02 - Backend Improvements

### Fixed

- Fix sorting order of videos changing after rating them.

### Added

- Prepare hooks for email automations for new content types.

## [1.3.10] - 2025-09-01 - Backend Improvements

### Fixed

- Small bug fixes in preparation of new app functionality.

### Changed

- Improvements to handling of certain rare scenarios during onboarding.

### Added

- Preparations for future personalisation of VR plans.
- Logistics routing rules for large headsets.

## [1.3.9] - 2025-08-28 - Backend Content Improvements

### Added

- Preparations for new types of content and presentation of programs.

## [1.3.8] - 2025-08-27 - Backend Improvements

### Added

- Add new API for fetching triggers.

### Changed

- Streamline toolbox content.
- Improvements to logging.

## [.1.3.7] - 2025-08-27 - Backend Improvements

### Added

- Additional monitoring of security events.
- Preparations for new categories of content.
- Choose a default calming scene for new users.
- Preparations for streamlined headset calibration experience for users.

### Fixed

- Ensure progress of users is maintained when program structure is changed.

## [1.3.6] - 2025-08-26 - Program Bug Fix

### Fixed

- Fix audio data not coming through to programs correctly.

## [1.3.5] - 2025-08-26 - Backend Improvements

### Added

- Background preparations for automatically generating hierarchies for users.

## [1.3.4] - 2025-08-26 - Backend Improvements

### Changed

- Changes to data structure in preparation for multiple exposure programs.

## [1.3.3] - 2025-08-25 - Backend Improvements

### Changed

- Speed improvements and simplifications to core APIs and models.

## [1.3.2] - 2025-08-25 - Backend Content Improvements

### Added

- Backend maintenance service to consolidate video content library.

## [1.3.1] - 2025-08-25 - Backend Content Improvements

### Added

- Preparations for simplifying sharing video content between clinician portal and D2C users.

## [1.3.0] - 2025-08-25 - Backend Improvements

### Changed

- Preparations to database structure to allow improved organisation of VR content.

## [1.2.7] - 2025-08-11 - Backend Improvements

### Fixed

- Fix error on logout page.

### Removed

- Removed purchase pages for bespoke sales process.

## [1.2.6] - 2025-08-04 - Backend Improvements

### Fixed

- Fixed handling of registrations to bespoke programs.

## [1.2.5] - 2025-07-10 - Backend Improvements

### Fixed

- Improved logic in a background job.

## [1.2.4] - 2025-07-10 - Backend Improvements

### Added

- Backend database improvements in preparation of new content.
- Improvements to database hygiene.

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
