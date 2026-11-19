## AzaharPlus 2126.2.A — Armada OS (ARM64)

**Experimental, unofficial prerelease.** An AArch64 AppImage build of AzaharPlus targeting Armada OS. Not affiliated with the official AzaharPlus or Armada OS projects.

### Included

- Native **ARM64 / AArch64** AppImage, assembled on **Fedora 44**
- **Qt 6 / Wayland** integration and **GStreamer** as the Qt Multimedia backend
- **FFmpeg 7.1.5**, with FFmpeg 8 dependencies removed from the final AppImage
- AppImage icon, desktop entry and validated AppStream metadata
- Corresponding source archives, build workflow and `SHA256SUMS.txt` are attached as release assets below. The same five files are preserved in the [successful Actions run #7](https://github.com/millee91/AzaharPlus-Armada/actions/runs/44022901906).

### Installation

Download `AzaharPlus-2126.2.A-Armada-aarch64.AppImage` from the **Assets** section of this prerelease. Mark it executable in your file manager and double-click it. Alternatively, in a terminal:

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

The AppImage currently attached to this release **matches build #7** (SHA-256 shown above). Download the accompanying `SHA256SUMS.txt` from **Assets**, put it in the same folder as all files being checked, then run `sha256sum -c SHA256SUMS.txt`. The release includes the source-with-submodules archive, FFmpeg 7.1.5 source archive and the build workflow.

### Public testing and bug reports

**Testers wanted.** This build has passed CI packaging and dependency checks, but has **not been verified to start or run games on a physical Armada OS handheld**. Expect possible issues with AppImage startup, graphics/Vulkan, audio, input, or game compatibility. It is not a stable or officially supported build.

Please report results through [Issues in this fork](https://github.com/millee91/AzaharPlus-Armada/issues/new/choose), including successful launches as well as bugs. For bugs, include:

- Your handheld model and Armada OS version
- Whether the AppImage starts from desktop mode or a terminal
- Graphics backend, what you expected, and what happened
- Reproduction steps and the relevant terminal log/error output

Do not upload copyrighted game dumps, system files, encryption keys, or personal information. Please keep reports specific to this ARM64 AppImage packaging; upstream emulator bugs should be reported to [AzaharPlus](https://github.com/AzaharPlus/AzaharPlus).
