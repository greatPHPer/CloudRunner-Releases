# CloudRunner

CloudRunner is a Windows desktop application with two execution paths: cloud-hosted Windows sessions and the experimental local Linux-on-Windows runtime.

This repository is the public distribution point for downloadable builds and release notes.

## Latest: Linux on Windows — Preview 1

**Version:** `v0.1.0-preview.1`  
**Status:** Prerelease  
**Platform:** Windows x64

CloudRunner can run a bundled x86-64 Linux desktop guest locally through QEMU. The bundled guest includes Xorg, `xeyes`, and `xterm`. The embedded guest mode does **not** require an installed WSL distribution.

The package also includes the Windows controller and HostAgent, with a workflow for launching local Linux application packages from WSL2/WSLg.

### Downloads

- **[CloudRunner Linux on Windows — Preview 1 (ZIP, approximately 1.26 GB)](https://github.com/greatPHPer/CloudRunner-Releases/releases/download/v0.1.0-preview.1/CloudRunner-Linux-on-Windows-v0.1.0-preview.1.zip)**
- [SHA256SUMS.txt](https://github.com/greatPHPer/CloudRunner-Releases/releases/download/v0.1.0-preview.1/SHA256SUMS.txt)
- [Release notes and all assets](https://github.com/greatPHPer/CloudRunner-Releases/releases/tag/v0.1.0-preview.1)

### Requirements

- Windows 10 x64, version 2004 (build 19041) or later, or a compatible Windows 11 system.
- .NET 10 Desktop Runtime.
- Microsoft Edge WebView2 Evergreen Runtime.
- Windows Hypervisor Platform for accelerated QEMU. QEMU software emulation is available as a fallback.
- For the optional local Linux ZIP workflow: WSL2, a Linux distribution, and WSLg for Linux GUI applications.

### Getting started

1. Download and extract the ZIP while preserving its folder structure.
2. Run `CloudRunner.WinForms.exe` as a standard, non-elevated Windows user.
3. Use the bundled Linux controls to launch `xeyes` or `xterm`.
4. Use the WSL2 section for local Linux EXE/ZIP packages that require a full Ubuntu/WSL filesystem.

### Verify the download

The published ZIP was checked against this SHA-256 digest:

```text
a7a0ca7d2afe6c7e4c7641d1815e1fd7fd8870e38b1cf55f07e3f1dca134c715
```

You can also verify it with the included checksum file:

```powershell
Get-FileHash .\CloudRunner-Linux-on-Windows-v0.1.0-preview.1.zip -Algorithm SHA256
```

This is an experimental local execution prototype, not a hardened malware sandbox. It does not provide arbitrary Linux package installation inside the embedded guest. Run only software you trust.

## Cloud Windows releases

Earlier CloudRunner beta builds provide the cloud Windows desktop workflow. Their downloads and release notes remain available on the [releases page](https://github.com/greatPHPer/CloudRunner-Releases/releases):

- [CloudRunner 0.1.0 Beta 2](https://github.com/greatPHPer/CloudRunner-Releases/releases/tag/v0.1.0-beta.2)
- [CloudRunner 0.1.0 Beta 1](https://github.com/greatPHPer/CloudRunner-Releases/releases/tag/v0.1.0-beta.1)

The cloud Windows workflow requires an internet connection and a valid CloudRunner activation.

## Security

- Do not put API keys, administrator tokens, or private credentials in this repository.
- Run the desktop application as a standard, non-elevated Windows user.
- Treat preview builds as experimental and review the release notes before installing.

## Releases

Browse all published builds, prereleases, checksums, and release notes on the [CloudRunner Releases page](https://github.com/greatPHPer/CloudRunner-Releases/releases).
