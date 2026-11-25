# Zorofin for Samsung Tizen TV

A native Flutter Jellyfin client for Samsung Tizen 6.0+ TVs (normally 2021 and
newer). Free to download; bring your own Jellyfin server. No server address,
account or media library is bundled.

[Download the 1.5 TPK](https://github.com/Zoraz01/zorofin-tizen-releases/releases/download/tizen-v1.5.0/zorofin-tizen-1.5.0.tpk) ·
[Install guide](https://zorofin.app/samsung-tv) ·
[Release notes](https://github.com/Zoraz01/zorofin-tizen-releases/releases/tag/tizen-v1.5.0) ·
[Support](https://zorofin.app/support) · [Privacy](https://zorofin.app/privacy)

## Release 1.5.0

Release `tizen-v1.5.0` contains app version **1.5.0** (build 170): "Who's
watching?" profiles, trailer previews in rows, chapters with scrub previews,
Skip intro, subtitle timing, automatic reconnect and per-show audio/subtitle
language memory.

Device testing: a friend's Samsung Q80B ran an earlier 1.5.0 test build. **Build
170 itself has not been run on a Samsung TV or emulator.** Its shared Flutter
code passed on Fire TV and the Android phone emulator. Package identity,
version, privileges and the absence of signing keys, PDBs and private
workstation paths were checked. The minimum API is a build target;
compatibility with every model is not claimed.

This is a `.tpk`, not a `.wgt` or Android `.apk`. Use Apps2Samsung's
**Custom WGT / TPK** option. Enable Developer Mode on the TV and connect from a
computer or supported phone on the same network. The installer must re-sign the
package with Samsung certificates covering your TV's DUID. Its bundled test
distributor signature does not authorize retail-TV installation.
Keep your signing profile for later updates. Never send us certificate passwords
or private keys. Downloading the file in the TV browser does not install it.

You can ask Codex on a computer connected to the TV's network to follow the
[install guide](https://zorofin.app/samsung-tv), verify the checksum and help with
the install. Someone at the TV still needs to enable Developer Mode and complete
Samsung sign-in/certificate setup where required.

## Verify the download

The immutable 1.5 TPK is attached to the versioned GitHub release. The website
may still offer an earlier version; use the release link above for 1.5.0.
Earlier releases remain available for rollback. Compare the SHA-256 with
`SHA256SUMS` in the release:

```sh
shasum -a 256 zorofin-tizen-1.5.0.tpk
```

## Distribution and credits

Zorofin is closed source, independently developed by Vitality Labs LLC with
substantial AI assistance. It is not an official Jellyfin or Samsung app.
This repository contains release information and binaries, not application source.

Vitality Labs LLC permits Apps2Samsung and its Tizen Community Packages catalog
to redistribute these unmodified Zorofin TPK release binaries, and permits users
and installers to re-sign copies solely for installation on their own TVs.
Preserve the app's attribution and bundled third-party notices. This permission
does not license the application source or third-party trademarks.

Flutter, flutter-tizen and their dependencies retain their respective licenses.
Their bundled notices are included in `res/flutter_assets/NOTICES.Z` inside the
TPK. The Zorofin icon and wordmark belong to Vitality Labs LLC.
