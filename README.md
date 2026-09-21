# CheryX Releases

Public binaries-only distribution repository for CheryX.

Private source code is maintained separately in `XproTN-dev/CheryX`.

## Authoritative DEV channel

Always use:

`channels/dev.json`

Raw endpoint:

`https://raw.githubusercontent.com/XproTN-dev/CheryX-Releases/main/channels/dev.json`

The channel JSON identifies the current supported DEV release and contains the exact package, versionCode/versionName, APK filename, byte size, SHA-256, permanent signer fingerprint and direct APK URL for both Owner and Mobile.

Current supported DEV generation:

- Owner **1.7.1 (13)** — `cheryx-owner-1.7.1.apk`
- Mobile **0.9.1-alpha (13)** — `cheryx-mobile-0.9.1-alpha.apk`

Both are signed with the permanent CheryX certificate SHA-256:

`8ec125791a8a8a088d4f1a8e9417b8c103728f1898427e1426bc5ba832c8dc56`

Do not select an older release merely because it has a similar version label. Development/intermediate releases are retained as build history; `channels/dev.json` is the authoritative pointer used by CheryX updaters.

## Mobile signing migration

Mobile builds before 0.9.1-alpha were debug-signed. Android cannot update an installed package across different signing certificates, so moving from an old debug-signed Mobile build to the permanent-release-signed 0.9.1-alpha build requires one uninstall/reinstall. Future canonical Mobile releases use the permanent CheryX signer and are intended to update in place.

## Files

Release assets are published individually so devices can download only the required APK. Actions ZIP artifacts are CI evidence and are not the application update transport.
