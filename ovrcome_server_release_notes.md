# Release notes for oVRcome's Server Software

This file contains public release notes for oVRcome's Server Software, which includes:
- The Clinician Portal
- API endpoints used by the iOS and Android mobile client apps
- API endpoints used by the VR apps
- VR web app for standalone headsets
- VR web app for live sessions
- Internal admin and maintenance tools
- Webhook integration with Stripe

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.4.1] - 2024-11-19 - Added new organisation feature flags

## Changelog

### Added

- A new tab to the clinic admin menu where clinic admins can see all clients in the whole clinic along with their assigned clinicians.
- Several new organisation level features which can be toggled on and off for the clients of that organisation
- A new /client/show endpoint which returns details about the client in the mobile app

## [1.4.0] - 2024-11-14 - Live session bug fix

## Changelog

### Added

- Error handling for failing to connect to the voice call in a live session.
- Includes clinician portal live session web app at version 0.9.2

## [1.3.1] - 2024-11-13 - Usability improvements

## Changelog

Further improvements to the trial and subscription process

### Added

- Ability for clinician to resend client invite emails

### Fixed

- A bug which was allowing broken subscription trials to be saved

## [1.3.0] - 2024-11-11 - Subscription and Shipping Updates

### Added

- Adjusted some of the copy in the portal now that we're coming out of beta
- Added some functionality to make it clearer on how to add videos to hierarchies from the library page
- Added further admin functionality to allow for easier setup of clinicians and organizations

### Changed

- Made some improvements to the shipping process for headsets

### Fixed

- Fixed a bug that prevented clients from signing up if they had a previous order
- Fixed a bug preventing video modals from scrolling if the video description was too long

## [1.2.0] - 2024-10-31 - Video and Hierarchy Updates

### Added

- API extension to support future live session features.

### Changed

- Videos can now be deleted from the view page, instead of only the edit page.
- Shows a more useful error message when a user attempts to register with an existing email.

### Fixed

- A bug where the list of triggers did not display correctly on the VR Library video modal.
- A bug which was unintentionally preventing access to the smartphone live session sometimes.

## [1.1.2] - 2024-10-31 - Administration UI improvements

### Added
* Administration UI improvements.

### Fixed
* Use oVRcome CDN for videos and thumbnails.

## [1.1.1] - 2024-10-30 - Live session fixes

### Fixed
* Fixes link used when initiating a new live session with a smartphone user.
* Fixes an issue where access codes weren't visible in the Clinician Portal

## [1.1.0] - 2024-10-29 - Live session call quality improvements

### Added
* Add microphone permission check for smartphone live session calls.

### Changed
* Update minimum required mobile app version to 1.65.0.
* Update Web XR live session app version from 0.15.2 to 0.15.3.
* Update clinician portal live session app version from 0.7.0 to 0.8.0.

## [1.0.0] - 2024-10-29 - Introducing release notes

### Added
- Introducing release notes
  In line with our new operating procedure for software development, we'll begin to create releases with notes for each deploy to production. Version numbers will follow the [Semantic Versioning](https://semver.org) format.
  As this is the first release, it contains nearly 800 commits dating back to March 2023, implementing our Clinician Portal and associated API to be used by the mobile app.
  Relative to what's currently in production, this release restructures how we store subscriptions and trials in our database, and introduces a new approach to trial subscriptions for standalone headsets that will provide more flexibility for customers.
- Includes standalone headset VR web app at version 0.15.2
- Includes live session VR web app at version 0.7.0
