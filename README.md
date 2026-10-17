# DevSweep releases

Downloads and update feed for [DevSweep](https://github.com/trongify0114/devsweep-releases/releases/latest),
a macOS app that measures and safely cleans developer caches. This repository holds
releases only. The source code is not here.

## Install

Download `DevSweep-<version>.dmg` from the [latest release](https://github.com/trongify0114/devsweep-releases/releases/latest),
open it and drag DevSweep to Applications. DevSweep needs macOS 26 or later.

## Updates

DevSweep checks for updates once a day. It installs them itself when you quit,
using [Sparkle](https://sparkle-project.org). You can change this in
DevSweep › Settings › General › Updates, or choose DevSweep › Check for Updates….

`appcast.xml` is the update feed, served at
`https://trongify0114.github.io/devsweep-releases/appcast.xml`. The feed and every update
are signed with DevSweep's EdDSA key. DevSweep installs nothing that doesn't carry that signature.
