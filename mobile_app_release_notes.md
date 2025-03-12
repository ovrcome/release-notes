# Release notes for oVRcome's Server Software

This file contains public release notes for oVRcome's mobile app. CHanges apply to both Android and iOS versions, except where noted.

For each release we note where we've Added, Changed, Fixed, or Removed code.

As the Mobile App supports live sessions between clinicians and clients, we also note compatibility of each release with the Clinician Live Session App.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.69.3] - 2025-03-12 - Update to Google Cardboard and VR
### Compatibility

- Compatible with Clinician Live Session App v0.11.0
  
### Changed
* Updated Google Cardboard from v1.26.0 to v1.28.0 to be compatible with newer phone models
* Made some tweaks to the VR aiming to improve the experience

## [1.69.0] - 2025-02-03 - Improvements to onboarding and logging in
### Compatibility

- Compatible with Clinician Live Session App v0.11.0
  
### Changed
* Updated the RANZP research link on the start welcome page so that it didn't go to an out of date page
* Swap the order of the login button and create account button, and make create account less prominent to reduce the number of clinician clients accidently creating an account
* Update the user type selection screen to direct clinicians and clinician clients to the right pages
* Update the login profile select screen to make it clearer what accounts you can choose to log in to
* Update copy for the headset purchase selection page to give the size of the phones that can fit in the headset
* Update the layout of the start welcome screen in the mobile app so that it's more responsive to different phone screen sizes

### Fixed
* Fix a bug where the user/exists endpoint wouldn't recognise user's emails if you entered some characters in uppercase.

## [1.68.0] - 2025-01-23 - Various UI/UX Improvements
### Compatibility

- Compatible with Clinician Live Session App v0.10.0

### Added
* Send through device info with model and name to the server to help with troubleshooting
  
### Changed
* Updated the sign in message copy to suit email or access code

### Fixed
* Fixed issue where children toolbox images were squashed
* Fixed bug where if you used your phones back button you could log yourself out of the app on the home page
* Fixed bug where in the mild depression program, playing a video would always start playing the first video in the playlist
* Fixed bug where you could log in to the app even on an old version where you were required to update
* Fixed bug where anxiety panel would still show, even when the suds_ratings_enabled boolean for the clients organisation was set to false.

## [1.67.0] - 2024-12-16 - Update for Unity 6

### Compatibility

- Compatible with Clinician Live Session App v0.10.0

### Changed

- Updated to Unity 6
- Updated all old UI input screens

## [1.66.0] - 2024-12-09 - Support feature toggles for clincians

### Compatibility

- Compatible with Clinician Live Session App v0.9.5

### Fixed

- Updates to live sessions

### Changed

- Improvements on connection to the Clinician Portal, with the app now responsive to many feature toggles


## [1.64.12] - 2/10/24 - Rework live session foundations

### Compatibility

- Compatible with Clinician Live Session App 0.7.0

### Changed

- Updates for a trial project with NHS
- Updated live session which removes Agora dependency

## [1.64.9] - 26/8/24 - Server switch

### Added

- Server switch
- Vaping triggers screen for research project

### Changed

- Updated Google Cardboard version

## [1.64.8] - 22/7/24 - Bug fix for end-of-module errors

### Fixed

- Hotfix to a bug causing errors at the end of modules

## [1.64.7] - 19/7/24 - Bug fixes

### Changed

- Updates to a program for vaping research

### Fixed

- Handle a bug which could cause crashes when not all video quality encodings were present.
- Various other bug fixes and improvements.

## [1.64.6] - 9/7/24 - Improvements for client/clinician use

### Changed

- The “next” button now functions like a next button in a mobile app live session to bring it in line more with the standalone headset.
- The “rate your anxiety” pops up at the end of a video now, in the client of a clinician mobile app.
