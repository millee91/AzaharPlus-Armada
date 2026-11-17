## AzaharPlus 2126.2.A — Armada OS (ARM64)

**Experimental, unofficial prerelease.** An AArch64 AppImage build of AzaharPlus targeting Armada OS. Not affiliated with the official AzaharPlus or Armada OS projects.

### Included

- Native **ARM64 / AArch64** AppImage, assembled on **Fedora 44**
- **Qt 6 / Wayland** integration and **GStreamer** as the Qt Multimedia backend
- **FFmpeg 7.1.5**, with FFmpeg 8 dependencies removed from the final AppImage
- AppImage icon, desktop entry and validated AppStream metadata
- Corresponding source code, build workflow, license notices and checksums available in the [Actions release-files artifact](https://github.com/millee91/AzaharPlus-Armada/actions/runs/44022901906)

### Installation

Download `AzaharPlus-2126.2.A-Armada-aarch64.AppImage` from this release **after the final asset has been replaced**. Mark it executable in your file manager and double-click it. Alternatively, in a terminal:

```bash
chmod +x AzaharPlus-2126.2.A-Armada-aarch64.AppImage
./AzaharPlus-2126.2.A-Armada-aarch64.AppImage
```

Only ARM64 Linux / Armada OS is targeted. Game compatibility, Vulkan performance and runtime behavior on a physical Armada device have **not yet been confirmed**.

### Integrity and source

The most recent successfully packaged AppImage is from [Actions run #7](https://github.com/millee91/AzaharPlus-Armada/actions/runs/44022901906):

```text
b13593e8f32a8618343f3c55c620898f7d4a25fd5d8f8e2168dd1f2ec21618d0  AzaharPlus-2126.2.A-Armada-aarch64.AppImage
```

[Version-specific SHA256SUMS.txt](https://github.com/millee91/AzaharPlus-Armada/blob/AzaharPlus/checksums/2126.2.A/SHA256SUMS.txt) · [Build workflow](https://github.com/millee91/AzaharPlus-Armada/blob/AzaharPlus/.github/workflows/armada-appimage.yml) · [Upstream AzaharPlus](https://github.com/AzaharPlus/AzaharPlus)

Verify by putting `SHA256SUMS.txt` next to the **corresponding build #7 AppImage**, then running `sha256sum -c SHA256SUMS.txt`. The CI release-files artifact also includes source archives and checksums for the whole build.

> **Draft-release note:** The AppImage currently attached to this draft was uploaded from an **older** build. Its SHA-256 does **not** match the checksum above. Replace the AppImage with the file from successful run #7, and attach the run's `SHA256SUMS.txt`, **before publishing** this release.

Report ARM64 packaging issues in [this fork's issue tracker](https://github.com/millee91/AzaharPlus-Armada/issues).
