# DevSweep releases

Downloads and update feed for [DevSweep](https://github.com/trongify0114/devsweep-releases/releases),
a macOS app that measures and safely cleans developer caches. This repository holds
releases only. The source code is not here.

## Install

Download `DevSweep-<version>.dmg` from the newest release on the [releases page](https://github.com/trongify0114/devsweep-releases/releases),
open it and drag DevSweep to Applications. DevSweep needs macOS 26 or later.

### Releases marked "ad-hoc signed" (prereleases)

DevSweep doesn't have a Developer ID certificate. Its releases are ad-hoc signed and not
notarized by Apple, so GitHub lists them as prereleases. They are still the current
version, and DevSweep updates to them by itself. Two steps are needed:

- **First install:** macOS blocks the app the first time you open it. Open System Settings ›
  Privacy & Security, scroll to the message about DevSweep and click **Open Anyway**.
- **After each update:** DevSweep shows Full Disk Access as not granted. Grant it again in
  System Settings › Privacy & Security › Full Disk Access. macOS ties the grant to the app's
  signature, and an ad-hoc signature changes with every build.

If DevSweep ever gets a Developer ID, its releases will be notarized and neither step will be needed.

## Updates

DevSweep checks for updates once a day. It installs them itself when you quit,
using [Sparkle](https://sparkle-project.org). You can change this in
DevSweep › Settings › General › Updates, or choose DevSweep › Check for Updates….

`appcast.xml` is the update feed, served at
`https://trongify0114.github.io/devsweep-releases/appcast.xml`. The feed and every update
are signed with DevSweep's EdDSA key. DevSweep installs nothing that doesn't carry that signature.
