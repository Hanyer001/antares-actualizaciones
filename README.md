# Antares — Downloads and Updates

Official distribution repository for **Antares on Windows and Android**. This repository hosts release packages and update metadata. Application development lives in **[Hanyer001/Antares](https://github.com/Hanyer001/Antares)**.

**[Latest stable Windows release](https://github.com/Hanyer001/antares-actualizaciones/releases/latest)** · [Android beta](https://github.com/Hanyer001/antares-actualizaciones/releases/tag/android-v0.3.3-beta.1) · [Product website](https://hanyer001.github.io/Pagina-Antares/)

## Choose a platform

| Platform | Published version | Requirements | Download |
| --- | --- | --- | --- |
| Windows | 0.3.3 stable | 64-bit Windows 10 or 11 | [Installer](https://github.com/Hanyer001/antares-actualizaciones/releases/download/v0.3.3/Antares-Setup.exe) |
| Android | 0.3.3 Beta 1 | Android 7.0+, 32-bit or 64-bit ARM | [APK](https://github.com/Hanyer001/antares-actualizaciones/releases/download/android-v0.3.3-beta.1/Antares-Android.apk) |

Previous versions remain in the [release history](https://github.com/Hanyer001/antares-actualizaciones/releases).

## Windows installation

1. Open the latest stable release and download `Antares-Setup.exe` or `Antares_<version>_x64-setup.exe`. Both names refer to the same installer contents for that release.
2. Run the installer. Installation is per-user and does not require administrator rights.
3. To update manually, run the new installer over the existing installation. Library data and preferences are stored separately from installation files.

Create an additional backup through **Ajustes → Tus datos** before updating if desired.

## Windows in-app updates

The application updater is available from version 0.3.0. When **Ajustes → Sistema → Avisar de versiones nuevas** is enabled, Antares checks at startup and every six hours while running. A manual check is also available through **Buscar versión nueva**.

A newer version prompts the user to confirm download and installation. Antares verifies the package signature before installing and restarting. Older installations without the updater need one manual update first.

## Android beta

The public Android package uses `com.hanyer.antares`. Future public packages must preserve its application ID and signing identity for installation over an existing copy.

Preview can coexist with the public application. Export a complete backup from Preview and restore it in Antares to migrate your library. See [ANDROID.md (Spanish)](ANDROID.md) for installation details.

Android is published as a **prerelease** and does not replace Windows as the latest stable release. `android-latest.json` is a separate manifest prepared for future update notifications; the Android app does not yet consult it.

## Release artifacts

| Artifact | Purpose |
| --- | --- |
| `Antares_<version>_x64-setup.exe` | Versioned Windows installer. |
| `Antares-Setup.exe` | Identical fixed-name copy for download links. |
| `latest.json` | Windows updater manifest with version, notes, installer URL and verification signature. |
| `Antares-Android.apk` | Android application package attached to its prerelease. |
| `android-latest.json` | Separate Android release metadata. |

Windows users only need the `.exe`; the application consumes `latest.json`. The updater signature verifies a package against the public key embedded in Antares. It is separate from a Windows code-signing certificate.

## Publish a release

Follow the [source repository's release guide (Spanish)](https://github.com/Hanyer001/Antares/blob/main/docs/releases.md).

For Windows, prepare the installer and its matching signed manifest, attach the versioned installer, fixed-name copy and `latest.json` to `vX.Y.Z`, then publish it as the stable **Latest** release. Confirm that the manifest points to the intended package and advertises a newer version. Keep Android prereleases separate.

A commit to the application source does not distribute an update. Users receive new packages only after the release artifacts are published. Private signing keys, passwords and GitHub credentials must remain outside this repository and release assets.

## Support

Report installation and update problems in [Antares Issues](https://github.com/Hanyer001/Antares/issues). Include the application version, operating system and error message, without credentials or private data.
