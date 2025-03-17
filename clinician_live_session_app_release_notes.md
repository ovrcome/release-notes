# Release notes for oVRcome's Clinician Live Session App

This file contains public release notes for oVRcome's Clinician Live Session app. This is a Unity app which can be accessed by clinicians via the Clinician portal web interface.

For each release we note where we've Added, Changed, Fixed, or Removed code.

We also note compatibility of each release with the Mobile App and the VR web app for standalone headsets.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.13.0] - 2025-03-17 - Live Session Improvements

### Added

- Tooltips for live session UI elements.
- Easier way to exit to lobby in a live session.
- Easier way to return to portal in a live session.

### Fixed

- Improvements to audio state synchronising between live sessions.
- UI and navigation improvements to live session app.

## [0.10.0] - 2024-12-15 - TODO: title

### Compatibility
- Compatible with VR web app for standalone headsets TODO:version
- Compatible with Mobile App TODO:version

### Added

- TODO

### Changed

- TODO

### Fixed

- TODO

### Removed

- TODO

## [0.9.5] - 2024-12-09 - TODO: title

### Compatibility

- Compatible with VR web app for standalone headsets v0.15.6
- Compatible with Mobile App v1.66.0

### Added

- Added event notifications.
- Added an exit button to navigate backward when creating a session.

### Changed
- New audio controls tab that has the ability to control portal and remote media sound and microphone volumes.
- Improved video timeline seeking functionality.
- Add new task feature to coordinate tasks with connection client.

### Fixed
- Fixed bug where scroll bar position would change when clicking on item in large lists.
- Fixed bug where refreshing the hierarchy would reset the scroll position.
- Fixes bug where video title index would incorrectly display a different index than the hierarchy.

### Known Issues
- Due to the overlay of the GUI parts of the video is obfuscated and off center.
- Closing the live session causes headless live session to continue to be available.
- There are scenarios where Vivox will not correctly log in and continuously fail until the browser is refreshed.

## [0.9.2] - 2024-11-14 - TODO: title

TODO: details

## [0.8.0] - 2024-10-28 - TODO: title

### Compatibility

- Compatible with VR web app for standalone headsets v0.15.3
- Compatible with Mobile App v1.65.0

### Added

- Added the ability to have voice chat with WebXR. Disabled by default.

### Changed

- Replace custom voice chat solution with Vivox voice chat.
- Implemented foundation of basic-handshaking to allow host and all client to have synchronization around video complete.
- Connected client devices can be mic mute can be controlled from the Portal end in settings panel (temporary placement).

### Fixed

- Fixed bug where video views for live session were not properly being reported.

### Known Issues
- Due to the overlay of the GUI parts of the video is obfuscated and off center.
- Reseeking video progress functionality doesn’t always work.
- Closing the live session causes headless live session to continue to be avaliable.
- There are scenarios where Vivox will not correctly log in and continuously fail until the browser is refreshed.

## [0.7.0] - 2024-10-08 - TODO: title

### Compatibility

- Compatible with VR web app for standalone headsets TODO:version
- Compatible with Mobile App TODO:version

### Added

- Added prototype voice chat based upon custom libraries

## [0.6.2] - 2024-09-10 - TODO: title

### Compatibility

- Compatible with VR web app for standalone headsets TODO:version
- Compatible with Mobile App TODO:version

### Added

- Added VideoSyncData which include id and instance value with URL for better tracking of video playback
- Added support for initial loading web overlay

### Changed

- Recreated live session view with UGUI to replace UI toolkit version due to inability to support web images
- Recreated session ended view with UGUI to fix button interaction issues

### Removed

- Removed old login functionality which is now handled by the web page itself
