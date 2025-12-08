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

## [2.6.2] - 2025-12-08 - Clinician Portal Improvements

### Changed

- Improvements to login verification system to be more user-friendly.

## [2.6.1] - 2025-12-08 - Clinician Portal Improvements

### Added

- Allow ordering headsets for users using access codes.
- UI improvements to make viewing trigger intensities clearer.
- API improvements for school users.
- Create new sandbox environment.

## [2.6.0] - 2025-12-03 - Bulk Headset Ordering

### Added

- In-portal ordering of multiple headsets.
- Expose testing metrics to improve code quality visibility.
- Automatically generate thumbnails for uploaded environments.

### Changed

- Updated how video quality assessments are added and added some more attributes
- Expose headset_delivered field on authentication of client
- Update wording on free-premium offer.
- Optimisation of database connections.
- Fix rare race condition when saving participant during a live session.

## [2.5.3] - 2025-11-24 - 

### Changed

- Internal improvements to developer container experience.
- Adds display of statuses for content request progression. When the status is updated on the admin site it updates a clinician friendly messaging on the portal as well.

### Added

- Adds ability to create content requests for clinicians who email them through, by adding them via the admin site ourselves and slotting them into the existing workflow.

### Updated

- Update JS dependencies to address security warnings.

## [2.5.2] - 2025-11-18 - Schools Product Improvements

### Changed

- Changes to school onboarding process.
- Removed deprecated code paths and database links.

## [2.5.1] - 2025-11-17 - Clinician Portal Improvements

### Added

- Add 3 new fields to the video quality assessment table and form.
- Add some new response fields to login for schools product.
- Add API for fetching gaze data from users doing VRET.

### Updated

- Update system dependencies.
- Updates to internal test data tooling.
- Updates to video quality assessment existing fields, to make them all framed positively

## [2.5.0] - 2025-11-10 - Content Request Mock-ups

### Added

- Almost instant mock-ups of content requests.
- Backend improvements for managing content types in the system.

## [2.4.4] - 2025-11-05 - Clinician Portal Bug Fixes

### Fixed

- Fix logging of smartphone live session events from clients.
- Fix bug where the preview modal wouldn’t open up in the library view after filtering

## [2.4.3] - 2025-11-03 - Backend Improvements

### Updated

- Improvements to video conversion process.

## [2.4.2] - 2025-10-28 - Clinician Portal Improvements

### Added

- Added content request section to the admin site, where admins can view and edit content requests that have come through from clinicians.
- Added sending of new content requests through to [requests@ovrcome.io](mailto:requests@ovrcome.io). These are then forwarded to Trello automatically and populate there
- Added a Segment event for when a content request is added
- Added functionality to require a clinician to give each trigger an intensity rating when requesting content

### Fixed

- Made some UI tweaks to the content request modal and the smart hierarchy generator modal to improve user experience

## [2.4.1] - 2025-10-22 - Clinicin Portal Improvements

### Added

- Database field to flag AI generated content.
- Clinician can change email when resending invites to clients.

### Fixed

- Fix bug previewing videos.

## [2.4.0] - 2025-10-22 - Clinician Admin Improvements

### Added

- Add ability for a clinician to revoke client access.
- Ability to choose access level when inviting colleagues to portal.

This release requires app version v1.74.0 for new functionality to work.

## [2.3.12] - 2025-10-21 - Clinician Portal Improvements

### Added

- Implemented the ability to make content requests as a clinician. The data from these are added to the content_requests and content_request_triggers tables

## [2.3.11] - 2025-10-14 - Clinician Portal Improvements

### Added

- Added the historical video quality assessments for each video, so you can see what assessments have been made previously and view the history for them.
- Ability to edit client’s email address before resending invites.

### Changed

- Adjusted the video quality assessment feature on the admin site, so that you can now view past video quality assessments and the history of video quality assessments per video.

### Fixed

- Fixed the "Clinician Registered" call, by moving its location to when the clinician is actually created, and passing in the clinician's id instead of the user id.
- Fix error inviting clinician when client with same email already exists.

## [2.3.10] - 2025-10-12 - Backend Improvements

### Fixed

- Fix handling of videos when they have both tags and triggers.

### Added

- Add Video Quality Assessment feature, so that videos can be internally assessed and marked by those on the admin site as to whether they’re up to acceptable quality.

### Changed

- Automate shipping for NZ headset orders.
- Update dependencies with latest security updates.

## [2.3.9] - 2025-10-05 - Clinician Portal Improvements

### Changed

- Backend improvements to controlling general video library access.
- Update dependencies.
- Improved consistency on admin pages.

### Added

- Add ability for clinicians to give feedback on videos in the portal

## [2.3.8] - 2025-09-30 - Clinician Portal Improvements

### Fixed

- Fix to bug where template hierarchies/programs modal couldn't scroll properly

## [2.3.7] - 2025-09-24 - Clinician Portal Improvements

### Changed

- Update system dependencies.
- Improvements to forum login provider.
- Allow clinicians to collect SUDs scores during live sessions.
- Allow reactivating deactivated clinicians in self-service admin.
- Code cleanups.

## [2.3.6] - 2025-09-19 - Clinician Portal Improvements

### Added:

- Set up SSO provider for forum integration.

### Changed:

- In clinician onboarding, changed ‘A research project’ copy to ‘Academic research’.
- Tweaks to default feature flags for managing clinicians.

## [2.3.5] - 2025-09-16 - Backend Improvements

### Added

- Require onboarding ‘other’ selections to also fill the textfield associated with the 'other selection

### Changed

- Hide “exposure readiness” column for schools.
- Improvements to database structure.
- Fix rare error when verifying email during registration.
- Update system dependencies.
- Remove some deprecated code.

## [2.3.4] - 2025-09-11 - Content Improvements

### Added

- Add the icons for PTSD.
- Hooks for automatic content synchronisation.

### Changed

- Finer-grained control of smart hierarchy generator feature.

## [2.3.3] - 2025-09-09 - v2.3.3 Clinician Portal Improvements

### Fixed
- Fixed bug where the wrong clinician images were showing for when clinicians were invited by another clinician to the portal

### Added

- Expand clinic auto-approval by allowing auto-approval in the case where a clinician selects they want to use the portal for a "research_project", provided that they also have a valid licence.
- Added a new feature flag called “hierarchy_live_session_preview_enabled” that can be enabled/disabled at an org level and also overriden at the clinic level
- Added clinicianFirstName to the “Clinic Created” Segment event

## [.2.3.2] - 2025-09-02 - Clinician Portal Improvements

### Added

- Administration interface improvements for managing clinician details.

## [2.3.1] - 2025-08-26 - Clinician Portal Improvements

### Added

- Add video explaining differences between live session types.

### Changed

- Security updates to dependencies.

## [2.3.0] - 2025-08-21 - Clinician Portal Improvements

### Added

- Backend improvements to allow greater granularity over video visibility.

### Fixed

- Fix error generating hierarchies with many triggers.

## [2.2.3] - 2025-08-21 - Clinician Portal Improvements

### Fixed

- Improve onboarding experience in certain uncommon scenarios.
- Prevent registration “submit” buttons from being able to be clicked twice and register you twice by disabling after clicking.
- Display the “At-Home Use” column for hierarchies in the admin site.
- Display video view “Quality” column for view_views on the admin site.
- Fix error generating instructions with non-western writing systems.

### Removed

- Simplify some backend data handling.

### Added

- Preparations for simpler headset calibration process.
- Added ability to request a resend of your verification email if you’re coming back as a clinician and trying to login when you’ve started but haven’t fully completed your registration process fully yet.

## [2.2.2] - 2025-08-20 - Live Session Bug Fix

### Fixes

- Remove error popup when previewing a live session

### Updates

- Live session app version: 0.16.1

## [2.2.1] - 2025-08-14 - Live Session Improvements

### Fixed

- Handle new types of content in live sessions.
- Better handling of upstream provider outages.

### Updated

- Live session app version: 0.16.0
- WebXR app version: 0.19.0

## [2.2.0] - 2025-08-11 - Backend Improvements

### Changed

- More fine-grained control over clinic features.

## [2.1.4] - 2025-08-11 - Backend Improvements

### Fixed

- Fix accessibility of admin portal.
- Adjust logic around claiming of free headset.
- Fix rate limiting issue when generating hierarchies.
- Fix error when inviting users when links are opened multiple times.
- Improved user experience when creating new hierarchies.

## [2.1.3] - 2025-08-05 - UI Improvements

### Changed

- Hide unnecessary UI elements for schools.

## [2.1.2] - 2025-08-04 - Personalised Instructions

### Added

- Generate personalised instructions for students using the schools product.

## [2.1.1] - 2025-08-04 - Backend Improvements

### Added

- Collect first/last name rather than just name when registering.

### Fixed

- Fix handling of unusually large uploads.

## [2.1.0] - 2025-08-01 - Preparing for Schools Programs

### Added

- New onboarding process for schools.
- Automatically create access codes for students.

### Changed

- Wording changes to be less clinic-specific.

## [2.0.12] - 2025-07-29 - Live Session Bug Fix

### Fixed

- Re-enable live session audio functionality after upstream provider outage.
- Improve default wording when using programs.

## [2.0.11] - 2025-07-25 - Live Session Bug Fix

### Added

- Preparations for future features.

### Fixed

- Reliability improvements to video conversion process.
- Temporarily disable voice channel in smartphone live sessions to mitigate service outage.

## [2.0.10] - 2025-07-24 - Live Session Improvements

### Updated

- Live session app version: 0.15.0

### Added

- Enhanced error logging when starting a live session.

### Fixed

- Fix player controls while live session video is paused.
- Improve text legibility in live sessions.
- Enablee SUDS feature for Live Session portal for D2C Live Sessions.

## [2.0.9] - 2025-07-16 - Admin management improvements

### Added

- Improvements to admin interface for client management.

## [2.0.8] - 2025-07-09 - Invite Improvements

### Fixes

- Improved handling around inviting existing clients.

## [2.0.7] - 2025-07-08 - UI Improvements

### Fixed

- Improve visual feedback when adding a video to a user’s hierarchy.

## [2.0.6] - 2025-07-03 - Backend Improvements

### Added

- Sync additional fields to CRM.

### Fixed

- Fixes error when client is paying for additional orders.

## [2.0.5] - 2025-07-02 - Add EMDR

### Added

- Add EMDR content to portal
- Improvements to admin UI

## [2.0.4] - 2025-06-30 - Exposure viewing improvements

### Changed

- Change logic around viewing exposures and when we allow users to continue to the next one.

## [2.0.3] - 2025-06-30 - Admin management improvements

### Added

- Homework toggle added to client overview page.
- Improvements to HQ record navigation.
- Additional CRM events during user journey.

### Fixed

- Improvements to HQ record editing.
- Improvements to auto approval process.

## [2.0.2] - 2025-06-18 - Admin management improvements

### Added

- Improvements to tag and category management in administration interface.
- Improvements to clinic administration interface.

### Fixed

- Fix issue with logging of categories.

## [2.0.1] - 2025-06-16 - Sign up fixes

### Fixed

- Fix error when verifying new email address.

## [2.0.0] - 2025-06-16 - Introducting free and premium subscriptions

### Added

- New invite process for inviting users to oVRcome and ordering a headset.
- Improvements to administration of clinics.

### Removed

- Removed subscription requirements from portal and for starting a live session.

### Changed

- Revamped billing page.
- Improved sign up process for qualifying clinics.
- Improved/simplified process to start live sessions.
- Improved messaging on next steps when adding clients.

## [1.34.2] - 2025-06-15 - Admin management improvements

### Added

- OCD category added for exposures.

### Changed

- Improvements to administration interface for managing videos and categories.

## [1.34.1] - 2025-06-09 - Subscription fixes

### Fixed

* Fix incorrect workflow when creating a new subscription.

## [1.34.0] - 2025-06-08 - v1.34.0

### Added
- Changed the clinic and clinician registration process to make it clearer and easier to go through

- Changed the registration process for a clinician invited by another clinician to make it clearer and easier to go through

## [1.33.3] - 2025-05-26 - Backend Improvements

### Fixed

- Fix issue inviting clients for a second, third time.

## [1.33.2] - 2025-05-22 - v1.33.2

### Added

- Additional logging of live session lifecycle events.

- Improvements to developer experience.

## [1.33.1] - 2025-05-12 - Minor Clinician Portal Improvements

### Added:
* Added a “browser” field to the Clinic User table which is populated on authentication so we can better help clinicians diagnose any issues

### Changed:
* After starting a trial, redirect back to the location the clinician navigated to the trial from
* Remove the “live” from “live preview”

### Fixed:
* Fixed a bug where hierarchy dropdown could be cut off

## [1.33.0] - 2025-04-30 - Clinician Portal Improvements

### Changed

* Trigger search status is saved between hierarchies, so when returning to modify a hierarchy in the hierarchy edit page, the previous trigger search filter history is loaded.
* Updated the smartphone live session explanation copy to better explain the steps needed to start a live session.
* Improvements to server logging, removed deprecated logging system.
* Updated the client/show call to add the client’s email and whether they have an access code.
* Improvements to developer environment.

### Fixed

* Fixed a bug where the trigger filter wasn’t being applied when first loading the hierarchy edit page.

## [1.32.1] - 2025-04-30 - Clinician Portal Improvements

### Changed

* Tweaks to shipping notification emails.
* Improvements to developer tooling.
* Improvements to searching in admin UI.
* Updated the calendly post-approval link in the portal
* Changed meeting length copy from 15 minutes to 30 minutes
* Add video ID in video modal

## [1.32.0] - 2025-04-28 - Smart Hierarchy Generator for Clinician Portal

### Added

* New tool: Smart Hierarchy Generator, for clinicians to create a hierarchy directly from their prompts.

### Fixed

* Clinician portal UI improvements.
* Fixes to testing process.

## [1.31.5] - 2025-04-28 - Clinician Portal Improvements

### Added

* Improvements to logging for customer support.
* Improvements to logging of client experience when watching videos.
* Improved live session data shown in client reporting dashboard

### Changed

* Improvements to developer experience.
* Improvements to accuracy of logging.
* Improvements to invitation process for existing clients.

## [1.31.4] - 2025-04-08 - Live Session Fixes

### Fixed

- Fix authentication issue with QuestPro standalone headsets during live sessions.

## [1.31.3] - 2025-04-08 - Clinician Portal UI Improvements

### Added

* Improvements to testing data.

### Fixed

* Improvements to display of video titles on hierarchy detail page.

## [1.31.2] - 2025-04-02 - Subscription Improvements

### Fixes

- Improvements to messaging during subscription process.

### Updates

- Security updates for some build dependencies.

## [1.31.1] - 2025-04-01 - Live Session Improvements

### Added

- Improvements to administration portal navigation.

### Fixed

- Fixed some UI issues in live session apps.

### Updated

- Live session app version: 0.14.1

## [1.31.0] - 2025-04-01 - Live Session Improvements

### Added

- Allow clinician to collect SUDs scores during live sessions.

### Updated

- Live session app version: 0.14.0
- WebXR app version: 0.18.0

## [1.30.0] - 2025-04-01 - Clinician Portal UI Improvements

### Changed

- VR Library page, Hierarchy page, and Add Environments page updated to use a more responsive layout, and adjusted for responsive behaviour.
- Responsive behaviour for video preview modal.
- Overall responsive layout applied to other pages where a clinician is logged in, but content within these pages has not been tuned for responsive behaviour.

### Fixed

- Standardisation of CSS and JS code, resulting in minor cosmetic changes but no functional changes.

## [1.29.0] - 2025-03-24 - Clinician Portal Improvements

### Fixed

- Fix recording of live session video views in certain rare scenarios.
- Fix issue with onboarding in certain rare scenarios.

## [1.28.0] - 2025-03-24 - Clinician Portal Improvements

### Added

* Improve messaging and add links to book a demo session for clinicians.
* Create demo clients for additional clinicians added to clinics.

## [1.27.1] - 2025-03-18 - Subscription Fixes

### Fixed

- Fix an issue cancelling client subscriptions in certain rare scenarios.

## [1.27.0] - 2025-03-18 - Live Session Improvements

### Added

- Administration UI improvements for reviewing live sessions and hierarchies.

### Changed

- Tooling changes to improve developer productivity.
- Live session API tweaks to improve data consistency.

### Removed

- Removed unused database tables.

## [1.26.0] - 2025-03-17 - Live Session Improvements

### Added

- Tooltips for live session UI elements.
- Easier way to exit to lobby in a live session.
- Easier way to return to portal in a live session.

### Fixed

- Backend improvements to live session APIs.
- Improvements to audio state synchronising between live sessions.
- UI and navigation improvements to live session app.

Live session version: 0.13.0 • WebXR version: 0.17.0

## [1.25.1] - 2025-03-12 - Clinician Portal Improvements

### Added

- Improvements to subscription process when entering email addresses already in use.
- Improvements to infrastructure tagging.
- Backend improvements for container management.

### Fixed

- Fix memory bug when analysing uploaded environments.
- Fix resilience of CI tests to external tool version updates.
- Fix rare login loop when logging in to VR portal.

## [1.25.0] - 2025-03-12 - Clinician Portal Improvements

### Added

- Collect feedback from clinicians when purchasing a subscription.

### Fixed

- Fixed check to determine whether a clinician has logged into a headset or not.
- Small tweaks to third party client-success integrations.
- Improved messaging when purchasing a client subscription before a trial has ended.


## [1.24.0] - 2025-03-07 - Record video search history

### Added

- Record search history from the video library and hierarchy edit pages for internal analytics.

### Fixed

- Improve messaging when clients attempt to log in to clinician portal.
- Fix subscription status display during certain rare scenarios with multiple subscriptions for a client.

## [1.23.0] - 2025-02-28 - Email for shipping tracking number

### Added

- Send shipping tracking number email when headsets are shipped.
- Administration UI improvements for video management.

### Fixed

- Fix rare error in administration UI.

### Changed

- Simplify hosting configuration.

## [1.22.0] - 2025-02-25 - Administration Improvements

### Added

* Administration UI improvements for VR workflow.

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



