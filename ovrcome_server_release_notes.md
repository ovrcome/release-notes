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
