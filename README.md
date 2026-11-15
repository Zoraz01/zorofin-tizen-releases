# Zorofin for Samsung Tizen TV

An experimental native Flutter Jellyfin client for Samsung Tizen 6.0+ TVs
(normally 2021 and newer). Free to download; bring your own Jellyfin server.
No server address, account or media library is bundled.

[Download the 1.4 TPK](https://github.com/Zoraz01/zorofin-tizen-releases/releases/download/tizen-v1.4.0-preview.1/zorofin-tizen-1.4.0.tpk) ·
[Install guide](https://zorofin.app/samsung-tv) ·
[Release notes](https://github.com/Zoraz01/zorofin-tizen-releases/releases/tag/tizen-v1.4.0-preview.1) ·
[Support](https://zorofin.app/support) · [Privacy](https://zorofin.app/privacy)

## Experimental preview

Release `tizen-v1.4.0-preview.1` contains app version **1.4.0**.
Built from the shared-TV baseline used for the released LG 1.4, packaged with
the native Tizen runner. The release build and 269 automated tests passed
(8 existing skips). The analyzer reports nine informational diagnostics with
no errors or warnings. These checks do not prove Samsung device behavior. Package integrity, app identity,
privileges and the absence of signing keys, PDBs and private workstation paths
were checked. **It has not been installed or tested on a Samsung TV or emulator.**
The minimum API is a build target; compatibility with every model is not claimed.

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

The immutable 1.4 TPK is attached to the versioned GitHub prerelease.
The website may still offer the earlier 1.3 preview; use the release link above
for this 1.4 package. The previous 1.3 release remains available for rollback. Compare its SHA-256 with `SHA256SUMS` in that release:

```sh
shasum -a 256 zorofin-tizen-1.4.0.tpk
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
