# Nitrux SB Manager | [![License](https://img.shields.io/badge/License-BSD_3--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause)

<p align="center">
  <img width="128" height="128" src="https://raw.githubusercontent.com/Nitrux/luv-icon-theme/master/Luv/mimetypes/64/application-x-ms-dos-executable.svg">
</p>

SB Manager helps you sign kernels for Secure Boot with ease and efficiency.

# Introduction

Nitrux SB Manager is a simple utility that creates machine owner keys (MOK) compatible with [Secure Boot](https://learn.microsoft.com/en-us/windows-hardware/design/device-experiences/oem-secure-boot).

> _⚠️ Important: Nitrux SB Manager is intended to work exclusively in Nitrux OS, and using this utility in other distributions will break them or not work at all. Please do not open issues regarding this use case; they will be closed._

# Overview

Nitrux SB Manager performs three steps:

1. Generate secure boot keys.
2. Sign your kernel for Secure Boot.
3. Enroll keys directly into the UEFI firmware.

### What SB Manager is

- Minimalistic, focusing on necessary functionality.
- Mostly a GUI utility.
- [100% Free and Open Source Software](#licensing) written entirely in [POSIX-compliant scripting language](https://en.wikipedia.org/wiki/Shell_script#Typical_POSIX_scripting_languages).

### What SB Manager is not

- A package manager.
  - SB Manager does not install new kernels, it only signs them.
- An installer.
  - SB Manager does not handle system or bootloader installation.
- A bootloader.
- A GUI for certificate management.
- A container, virtual machine, Live USB creator, Linux distribution, desktop environment, or "proprietary software."
  - _**Note**: We don't know why anyone would think that, but one can never know, so let's clarify that._

---

### Requirements

- Nitrux 3.7.1+.
> _♦ Information: The utility will work out of the box starting with the mentioned release._


#### Installation

For Nitrux releases where SB Manager is not available by default, do the following:
> _⚠️ Important: To permanently add sb-manager to the root, see our tutorial [Filesystem, Security, Privacy, and Anonymization Features in Nitrux](https://nxos.org/tutorial/filesystem-security-privacy-and-anonymization-features-in-nitrux/)_

```
git clone --depth=1 https://github.com/Nitrux/sb-manager.git $HOME/nuts
sudo cp $HOME/sb-manager/usr/bin/sb-manager /usr/bin
```

# Usage

Run `sb-manager` from the terminal and follow the prompts.
> _♦ Information: The use of this utility requires `pkexec`_

SB Manager does not have any configuration parameters or additional options.

SB Manager is highly automated except for asking the user for permission to perform actions and input to create the OpenSSL certificate and the MOK password.


# Licensing

The repository and its contents are licensed under **BSD-3-Clause**.

# Issues

If you find problems with the contents of this repository, please create an issue.

©2024 Nitrux Latinoamericana S.C.
