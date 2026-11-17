# AzaharPlus for Armada OS (ARM64)

**Unofficial, experimental community build** of [AzaharPlus](https://github.com/AzaharPlus/AzaharPlus), a Nintendo 3DS emulator, packaged as an AArch64 AppImage for Armada OS.

This repository is a fork of the upstream AzaharPlus source with an additional ARM64 AppImage build workflow. It is **not an official AzaharPlus or Armada OS release**. Packaging checks pass, but launching and running games on an actual Armada OS device has not yet been confirmed.

## Downloads

- [Releases for this Armada build](https://github.com/millee91/AzaharPlus-Armada/releases) — public downloads appear once a release is published.
- [Latest successful packaging run (#7)](https://github.com/millee91/AzaharPlus-Armada/actions/runs/44022901906) — download the `AzaharPlus-Armada-release-files` artifact (GitHub sign-in may be required).
- [Official upstream AzaharPlus releases](https://github.com/AzaharPlus/AzaharPlus/releases) — other supported platforms.

Current target version: **AzaharPlus 2126.2.A**; AppImage filename: `AzaharPlus-2126.2.A-Armada-aarch64.AppImage`.

## Install and run on Armada OS

1. Download the Armada ARM64 AppImage from the correct release, or extract it from the GitHub Actions `AzaharPlus-Armada-release-files` ZIP artifact.
2. In the file manager, open **Properties → Permissions** and enable executing the file as a program (the exact wording depends on the file manager).
3. Double-click the AppImage to start it. No system-wide installation is intended.

If your file manager does not launch it, open a terminal in the directory containing the AppImage and run:

```bash
chmod +x AzaharPlus-2126.2.A-Armada-aarch64.AppImage
./AzaharPlus-2126.2.A-Armada-aarch64.AppImage
```

Requires an **ARM64 / AArch64 Linux** environment. This is **not** an Android APK, an x86-64 build or a Windows executable. Compatibility with Armada OS and other Linux variants remains experimental.

## Verify your download

The checksum below is for the **AppImage produced by successful Actions run #7**, not for an older file attached to a draft release:

```text
SHA256: b13593e8f32a8618343f3c55c620898f7d4a25fd5d8f8e2168dd1f2ec21618d0
File:   AzaharPlus-2126.2.A-Armada-aarch64.AppImage
```

Download the [version-specific SHA256SUMS.txt](https://github.com/millee91/AzaharPlus-Armada/blob/AzaharPlus/checksums/2126.2.A/SHA256SUMS.txt) into the same folder as that AppImage, then run:

```bash
sha256sum -c SHA256SUMS.txt
```

Expected output ends with `OK`. If the hashes do not match, **do not use that AppImage as though it were build #7**. The build artifact itself also contains an `SHA256SUMS.txt` covering the files packaged in that run.

## Build details and sources

- Built in **Fedora 44 AArch64**, using **Qt 6 / Wayland** and Qt Multimedia's **GStreamer backend**.
- Uses **FFmpeg 7.1.5**; the AppImage packaging check confirms no FFmpeg 8 shared-library dependencies remain.
- [AppImage GitHub Actions workflow](.github/workflows/armada-appimage.yml) includes compiled-output reuse and compiler/FFmpeg caching.
- The Actions release-files artifact contains the AppImage, corresponding source archive (including submodules), FFmpeg source archive, build workflow and a generated `SHA256SUMS.txt`.
- License notices for AzaharPlus, FFmpeg and bundled dependencies are included in the AppImage under `usr/share/doc/azaharplus/`. Follow the licenses in the corresponding source distributions.

## Issues and acknowledgements

For ARM64 packaging or launch problems, [open an issue in this fork](https://github.com/millee91/AzaharPlus-Armada/issues) and include the Armada OS version, device, and the relevant terminal output. Upstream emulator questions belong with [AzaharPlus](https://github.com/AzaharPlus/AzaharPlus).

AzaharPlus is based on [Azahar](https://github.com/azahar-emu/azahar). The Azahar logo is credited to **PabloMK7 and angyartanddraw** (CC BY 4.0). This fork does not claim ownership of upstream code, artwork or trademarks.
