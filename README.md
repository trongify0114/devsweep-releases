# DevSweep releases

Downloads and update feed for [DevSweep](https://github.com/trongify0114/devsweep-releases/releases),
a macOS app that measures and safely cleans developer caches. This repository holds
releases only. The source code is not here.

## Install

Download `DevSweep-<version>.dmg` from the newest release on the [releases page](https://github.com/trongify0114/devsweep-releases/releases),
open it and drag DevSweep to Applications. DevSweep needs macOS 26 or later.

Releases from 0.3.0 on are signed with a Developer ID and notarized by Apple, so macOS
opens them without warnings.

### Upgrading from 0.1.0 or 0.2.0

Those two releases were ad-hoc signed prereleases. After DevSweep updates from one of them,
it shows Full Disk Access as not granted, because macOS ties the grant to the app's signature.
Grant it once more in System Settings › Privacy & Security › Full Disk Access. Later updates
keep the same signature, so the grant stays.

## Updates

DevSweep checks for updates once a day. It installs them itself when you quit,
using [Sparkle](https://sparkle-project.org). You can change this in
DevSweep › Settings › General › Updates, or choose DevSweep › Check for Updates….

`appcast.xml` is the update feed, served at
`https://trongify0114.github.io/devsweep-releases/appcast.xml`. The feed and every update
are signed with DevSweep's EdDSA key. DevSweep installs nothing that doesn't carry that signature.
