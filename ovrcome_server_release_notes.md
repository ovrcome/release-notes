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

## [1.21.0] - 2025-02-25 - VR Library Improvements

### Added

* Groundwork for 8k adaptive bit-rate streaming of VR.
* Show search terms when searching in VR library.

### Changed

* More consistent messaging around for clinics pending approval.
* Backend changes for recording live session events.

## [1.20.1] - 2025-02-19 - Add new Javascript function for Unity Live Session App

### Added
- Added a new javascript function for the Unity Live Session app which goes back 2 pages. This is so you can click “return to portal” and skip over the live session steps page 

## [1.20.0] - 2025-02-18 - VR Library and Hierarchy Building Improvements

### Added:

- Added a “+” icon to quickly add videos by clicking on their thumbnail in the VR library
- Added a “select all” button to the trigger modal so all triggers can be selected for filtering

### Removed:

- Removed a ui tooltip which is no longer used

## [1.19.0] - 2025-02-17 - Hosting and API Improvements

### Changed

- Changes to server deployment and hosting process.
- Backend changes to allow for additional webhooks.
- Better request validation for video views API.

## [1.18.0] - 2025-02-12 - Clinician Portal Tweaks and Improved Live Session Step Logic

### Added:

- Added a segment tracking event for when a clinician uses the live session preview functionality for a hierarchy

### Changed:

- Updated the live session for smartphone instruction check list. Refactored the logic and split it out into further steps

- If triggers haven’t been confirmed, don’t ask a clinician to confirm them if they’re just toggling the hierarchy for homework toggle on and off

### Fixed:

- Fixed a bug where the subscription tab was showing/hiding incorrectly and was confusing

## [1.17.1] - 2025-02-03 - Extend Pay-What-You-Want Offer

### Added

* Extended pay-what-you-want offer.

## [1.17.0] - 2025-01-30 - Video Library UX and Invoicing Improvements

### Added

* Pagination for videos in our VR library and hierarchy editing screens.
* Client name is shown on invoices from Stripe.

## [1.16.1] - 2025-01-27 - UX Improvements for Clinicians

### Added

* Added info about supported browsers for live sessions, so clinicians will have less failed live sessions from using an unsupported browser
* Added a skip button to the rate triggers page, to allow for a more streamlined UX

## [1.16.0] - 2025-01-24 - Live Session Preview

### Added

* Added ability to simulate a live session directly from the hierarchies screen.
* Update clinician portal live session app version from 0.10.0 to 0.11.0.

## [1.15.2] - 2025-01-24 - Responsive client reports

### Added

- Added the Hotjar feedback widget

## [1.15.1] - 2025-01-23 - Responsive client reports

### Changed

- Client reports page now reflows to have better layout on smaller screens
 
## [1.15.0] - 2025-01-21 - Registration Improvements

### Added

* Create demonstration client and data for new clinic registrations.

## [1.14.1] - 2025-01-21 - Bug fix to live session

### Fixed

* Fixed a bug causing live sessions to fail

## [1.14.0] - 2025-01-20 - Clinician portal improvements

### Added

* SUDs ratings are now taken into account when marking a video as completed or locked (previously a video just had to be watched all the way through for it to be completed)
*Made it easier and more clear to add videos to hierarchies. The “add to hierarchy” button is now not hidden behind a scroll, and you can add videos directly from the thumbnail by clicking the “+” icon

### Fixed

* Fixed a bug where the video counts in hierarchies could display wrong, since it was counting inactive videos as well as active videos.

## [1.13.0] - 2025-01-16 - Clinician portal improvements

### Added

* Added ability to purchase a smartphone subscription before the end of a free trial.

### Fixed

* Fixed inconsistencies when switching between client-pays and clinician-pays for smartphone subscriptions.

### Removed

* Removed a deprecated database field.
* Removed old live session code.

## [1.12.5] - 2024-01-09 - Clinician portal UX improvements

### Added
Ability to create video descriptions using html to format them nicely

- The ability to update and change the client address during checkout

### Fixed
- The clinic menu on the VR library page not matching the menu throughout the rest of the portal
- Updated the T&Cs links to go the current terms and conditions page

### Removed
- The version check for the native quest and pico apps since they’re no longer being used

## [1.12.3] - 2024-12-19 - Subscription bug fixes

### Fixed

* Fixes an issue viewing subscriptions in some scenarios.

## [1.12.2] - 2024-12-18 - Subscription process updates

### Fixed

* Small updates to the subscription process to improve messaging and consistency for new users.

## [1.12.1] - 2024-12-17 - Add new Segment event

### Added

- A new event for when a subscription trial for a standalone headset has been activated, so that relevant emails can be triggered

## [1.12.0] - 2024-12-16 - Upgrade to Unity 6

### Changed

- Upgrade all Unity apps to Unity 6
- Update minimum required mobile app version to 1.67.0.
- Update standalone headset Web XR live session app version from 0.15.6 to 0.16.0.
- Update clinician portal live session app version from 0.9.5 to 0.10.0.

## [1.11.1] - 2024-12-13 - Pay What You Want Improvements

### Fixed

* Small improvements to wording for the pay-what-you-want process.

## [1.11.0] - 2024-12-13 - Pay What You Want

### Added

* New “pay what you want” promotion for clinician subscriptions.

### Fixed

* Subscription improvements.

## [1.10.2] - 2024-12-12 - Bugfixes and subscription updates

### Fixed

- A bug which was causing the client overview page to error sometimes
- A bug that was sometimes causing errors when logging in on standalone headsets

### Added

- A new event for when a subscription trial for a standalone headset has been activated, so that relevant emails can be triggered
- Supporting infrastructure for taking SUDS ratings when assessing if a hierarchy video is to be considered completed or not
- Ability for clinicians to cancel subscriptions for themselves and their clients

## [1.10.1] - 2024-12-11 - Live session instruction pages

### Added

- Instruction pages for connecting to clients through both smartphone and standalone headset live sessions

## [1.10.0] - 2024-12-09 - Live session improvements

### Added

- Added new audio controls for clinicians in mobile live sessions:
  - Allows clinicians to:
    - Adjust volume/Mute/Unmute client microphone
    - Mute/Unmute their own microphone
    - Adjust volume/Mute/Unmute video audio for client
    - Adjust volume/Mute/Unmute video audio for themselves
- Added an exit button to navigate backward when creating a live session.

### Fixed

- Fixed a bug in live sessions where playback would sometimes get stuck in a paused state indefinitely on standalone headsets.
- Fixed a bug in live sessions where hierarchy list scroll bar position would change when clicking on a video in hierarchies with a lot of videos.
- Fixed a bug in live sessions where scroll bar position would be reset when the hierarchy is reloaded.
- Fixed a bug in live sessions where clinicians would sometimes see a different number next to the video title than was shown in the hierarchy panel for that video.

### Changed

- Improved video timeline seeking functionality in live sessions.
- Update minimum required mobile app version to 1.66.0.
- Update standalone headset Web XR live session app version from 0.15.3 to 0.15.6.
- Update clinician portal live session app version from 0.9.2 to 0.9.5.

## [1.9.3] - 2024-12-06 - Bug fix for iPhone 8 live sessions

### Fixed

- An issue that was preventing live session invites from showing up on iPhone 8 devices


## [1.9.2] - 2024-12-06 - Clinician Portal Improvements

### Fixed

* Changes to wording to improve user experience.
* Fix inconsistent pricing on checkout page in rare scenarios.
* Improvements to developer experience.
* Improvements to administration interface.

## [1.9.1] - 2024-12-05 - Backend Improvements

### Fixed

* Improvements to developer experience.
* Improvements to logging.
* Subscription consistency improvements.

## [1.9.0] - 2024-12-04 - Subscription Visibility Improvements

### Added

* Clinician billing page now shows the status of your trials and subscriptions.
* Clinician billing page now shows the status of your client’s trials and subscriptions.
* Subscription detail page shows relevant subscription information, including upcoming billing dates and amounts, and previous invoices.

## [1.8.5] - 2024-12-03 - Bug fix for smartphone live session

### Fixed
- Fixed an issue preventing smartphone live sessions from connecting when clinician and client share the same user email

## [1.8.4] - 2024-12-03 - Bug fixes for subscriptions and set-up advice

### Fixed
- Fixed an issue preventing clinicians from creating a smartphone subscription for a client after an expired trial
- Fixed an issue where the clinic admin page could render incorrectly when handling a second request to delete the same client-clinician association in quick succession

### Changed
- Subscription tab more clearly shows the distinction between a client’s invitation state and their subscription state
- Device call-to-action messages adjusted so that clinicians are advised to create a populated hierarchy while waiting for their clinic to be approved

## [1.8.3] - 2024-11-29 - Wording Tweaks

### Fixed

* Tweaks to wording now that we are out of beta.

### Added

* Improvements to testing framework.

## [1.8.2] - 2024-11-27 - Client Management Improvements

### Added

* Allow clinic admins to grant access to clients to other clinicians in their clinic.

### Fixed

* Optimisations to page load time.

## [1.8.1] - 2024-11-25 - Subscription Improvements

### Added

* Further improvements for administration pages.

### Fixed

* Improvements to subscription handling.

## [1.8.0] - 2024-11-25 - Subscription Improvements

### Fixed

* Updates to subscription process to better differentiate who is paying for a subscription.
* Updates to subscription administration pages.

## [1.7.0] - 2024-11-22 - Responsive layout and UI improvements

### Changed

- Layout improvements for the client index, show, and resources pages in the Clinician Portal
- Improved calls-to-action for live sessions and homework
- Improved styling for heading and link text in resources
- Resources menu is hidden if there are no resources available for an organisation
- Updates to internal automated testing system

## [1.6.0] - 2024-11-21 - Subscription Improvements

### Added

- Backend functionality improvements around subscription handling.
- Improvements to client administration functionality for clinic administrators.

## [1.5.0] - 2024-11-20 - Improve Clinician Onboarding Process

## Changelog

### Added

- Updated the clinician onboarding process. When signing up for a clinic, there is now one new field (“How did you hear about us”), which has been added to the form

- When inviting a new clinician to your clinic, these clinicians must fill in their own onboarding form, with T&Cs clearly shown, to make their onboarding process cleaner

## [1.4.3] - 2024-11-19 - Allow clinic admins to remove clinician access to clients

## Changelog

### Added

- The ability to remove a clinician's access to a client from the clinic admin screen.

## [1.4.2] - 2024-11-19 - Patch to fix a bug caused by the previous release related to hierarchy reorder

## Changelog

### Fixed

- A bug which was causing errors when trying to reorder a hierarchy in some situations.

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
