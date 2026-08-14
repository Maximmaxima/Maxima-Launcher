# Maxima Launcher

Maxima Launcher is an unofficial community-developed desktop launcher and mod manager for Minecraft: Java Edition.

The project is currently in active development.

## Features

- Separate Minecraft profiles / instances
- Fabric, Forge, NeoForge and Quilt support
- Modrinth integration
- Install and manage mods
- Resource pack management
- Shader management
- Modrinth modpack installation and import
- Modpack export as `.mrpack` and `.zip`
- Mod version switching and updates
- Microsoft account authentication
- Minecraft Java profile integration
- Minecraft Java skin management
- Customizable accent colors and OLED dark mode

## Microsoft Authentication

Maxima Launcher uses Microsoft's official OAuth 2.0 authentication system.

Authentication is performed using:

- Authorization Code Flow
- PKCE
- Microsoft Identity Platform
- Xbox Live authentication
- XSTS authentication
- Minecraft Java Game Services

The launcher does **not** ask users for their Microsoft password.

No client secret is embedded or stored in the application.

### Microsoft Entra Application ID

`89beebdd-1371-4f33-9956-a128bc979659`

## Minecraft Game Services

Minecraft Java Game Service API access is used only for functionality requested by the signed-in user, including:

- authenticating the Minecraft account
- verifying Minecraft: Java Edition ownership
- retrieving the user's Minecraft Java profile
- retrieving the Minecraft username and UUID
- managing the user's own Minecraft Java skin

Maxima Launcher does not provide access to Minecraft for users who do not own the game.

## Mod Management

Each Maxima Launcher profile has its own isolated game directory containing, for example:

- `mods/`
- `config/`
- `resourcepacks/`
- `shaderpacks/`
- `saves/`

Mods and other content can be installed using the Modrinth API.

## Privacy

Maxima Launcher does not collect Microsoft passwords.

Authentication takes place on Microsoft's official login page.

Authentication tokens are used only to perform functions requested by the signed-in user.

At the current development stage, authentication tokens are kept only for the active launcher session and are not permanently stored by Maxima Launcher.

## Disclaimer

Maxima Launcher is an unofficial community project.

It is not affiliated with, endorsed by, sponsored by, or associated with Mojang Studios or Microsoft.

Minecraft is a trademark of Microsoft Corporation.

## Development Status

Maxima Launcher is currently under active development.

Features and behavior may change as development continues.
