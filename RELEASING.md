# Release-only distribution

This repository publishes Zorofin Tizen binaries and release information only.
Never copy private application source, history, signing keys, credentials, logs,
workstation paths or real-server screenshots into it.

1. In the private application repository, follow `docs/TIZEN_RELEASE_1_4.md` and
   the Tizen build/packaging scripts. Retain source revision, staged dependency
   lock, exact validation results and hardware-test status there.
2. Review the TPK identity, version, privileges and notices. Scan its decompressed
   members for private data and debug/signing files. Keep Dart symbols private.
3. Update this repository's README, package.json, SHA256SUMS and SOURCE.json on a
   scoped feature branch. Validate JSON and confirm checksum/size against the TPK.
   Publish reviewed documentation through a PR before creating its release tag.
4. Create a GitHub prerelease with the exact reviewed TPK, package.json,
   SHA256SUMS and SOURCE.json. Use a new immutable tag/filename for a new package;
   do not replace the previous preview's binary. Example:

   ```sh
   gh release create tizen-v1.4.0-preview.1 \
     --repo Zoraz01/zorofin-tizen-releases --target main --prerelease \
     --title 'Zorofin Tizen 1.4.0 experimental sideload preview' \
     --notes-file /path/to/reviewed-release-notes.md \
     /path/to/zorofin-tizen-1.4.0.tpk package.json SHA256SUMS SOURCE.json
   ```

5. Download all public release assets anonymously with normal HTTPS verification.
   Compare their exact bytes to the reviewed local copies; record the receipt in
   the private application release record.
6. Update the existing Apps2Samsung PR's manifest to select the exact reviewed
   tag prefix and TPK asset. Run its validation checks and update the PR's version,
   release URL and test results. Keep the draft status until Tizen device/emulator
   evidence satisfies the catalog's requirement. Never equate build/test success
   or catalog review with real-TV or Samsung store acceptance.

The website download and Samsung Seller Office are separate release workflows.
Keep the earlier release available for rollback and preserve the README's
redistribution/re-signing permission and third-party notices.
