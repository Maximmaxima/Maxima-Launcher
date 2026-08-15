<div align="center">
  <img src="logo.png" width="170" alt="Maxima Launcher logo">

# Maxima Launcher

**An unofficial community-developed Minecraft: Java Edition launcher and mod manager.**

Modrinth integration • Isolated profiles • Modloader support • Microsoft authentication • Skin management

</div>

> [!IMPORTANT]
> Maxima Launcher is currently in active development.
>
> Minecraft Java Game Services access for the Maxima Launcher Microsoft application is currently pending review/approval.
>
> Until approval is granted, Microsoft and Xbox authentication may succeed while Minecraft Services returns:
>
> `403 Invalid app registration`

## Overview

Maxima Launcher is a desktop launcher and mod-management application for Minecraft: Java Edition.

The goal is to provide a clean instance-based workflow similar to modern mod launchers while keeping profile files separated and making mods, resource packs, shaders and modpacks easier to manage.

This repository currently serves as the public project and documentation page while the launcher continues development.

## Features

### Profiles and Modloaders

- Separate Minecraft profiles / instances
- Fabric support
- Forge support
- NeoForge support
- Quilt support
- Independent game directories for each profile
- Profile import and management

### Mods and Content

- Modrinth integration
- Install and manage mods
- Resource pack management
- Shader management
- Enable and disable installed content
- Mod version switching
- Update detection and installation
- Project icons and metadata from Modrinth

### Modpacks

- Install Modrinth modpacks
- Import existing profiles and modpacks
- Export profiles as `.mrpack`
- Export profiles as `.zip`

### Minecraft Account Integration

- Microsoft OAuth 2.0 authentication
- Authorization Code Flow with PKCE
- Xbox Live authentication
- XSTS authentication
- Minecraft Java profile integration
- Minecraft username and UUID retrieval
- Minecraft Java skin management

### Interface

- OLED black theme
- Custom accent colors
- Custom Maxima branding
- Modrinth-inspired profile and content management UI

## Profile Structure

Each Maxima Launcher profile uses its own game directory.

A profile may contain folders such as:

```text
profile/
├── config/
├── mods/
├── resourcepacks/
├── shaderpacks/
├── saves/
└── .maxima/
```

This keeps installed content and configuration isolated between profiles.

## Microsoft Authentication

Maxima Launcher uses Microsoft's official OAuth 2.0 authentication system.

The launcher does **not** ask users for their Microsoft password and does not embed a client secret.

Authentication uses:

1. Microsoft OAuth 2.0 Authorization Code Flow with PKCE
2. Xbox Live authentication
3. XSTS authentication
4. Minecraft Java Game Services

For a more detailed explanation, see [AUTHENTICATION.md](AUTHENTICATION.md).

### Microsoft Entra Application ID

`89beebdd-1371-4f33-9956-a128bc979659`

## Minecraft Game Services

Minecraft Java Game Service API access is intended only for functionality requested by the signed-in user, including:

- verifying Minecraft: Java Edition ownership
- retrieving the user's Minecraft Java profile
- retrieving the Minecraft username and UUID
- managing the signed-in user's own Minecraft Java skin

Maxima Launcher does not provide Minecraft access to users who do not own the game.

## Privacy and Security

Maxima Launcher does not collect Microsoft passwords.

Authentication takes place on Microsoft's official login pages.

At the current development stage, authentication tokens are kept only for the active launcher session and are not intentionally stored permanently by Maxima Launcher.

Project documentation:

- [Authentication](AUTHENTICATION.md)
- [Privacy Policy](PRIVACY.md)
- [Security Policy](SECURITY.md)

## Development Status

Maxima Launcher is under active development.

Features, behavior and UI may change while the project evolves.

There is currently no stable public release published through this repository.

## Disclaimer

Maxima Launcher is an unofficial community project.

It is not affiliated with, endorsed by, sponsored by, or associated with Mojang Studios or Microsoft.

Minecraft is a trademark of Microsoft Corporation.
