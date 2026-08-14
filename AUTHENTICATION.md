# Authentication

## Overview

Maxima Launcher uses Microsoft's official authentication system to sign users in to their Microsoft, Xbox and Minecraft accounts.

Maxima Launcher never asks users to enter their Microsoft password directly into the launcher.

Authentication takes place through Microsoft's official sign-in page.

## Authentication Flow

Maxima Launcher uses the following authentication flow:

1. Microsoft OAuth 2.0
2. Authorization Code Flow with PKCE
3. Xbox Live authentication
4. XSTS authentication
5. Minecraft Java Game Services

The general flow is:

```text
Maxima Launcher
      ↓
Microsoft Login
      ↓
Microsoft Access Token
      ↓
Xbox Live User Token
      ↓
XSTS Token
      ↓
Minecraft Access Token
      ↓
Minecraft Java Profile
```

## Microsoft OAuth

Maxima Launcher uses:

- OAuth 2.0 Authorization Code Flow
- PKCE
- System browser authentication
- localhost redirect URI

The Microsoft Entra Application ID used by Maxima Launcher is:

`89beebdd-1371-4f33-9956-a128bc979659`

Maxima Launcher is configured as a public desktop client.

No Microsoft client secret is embedded in the launcher.

## Redirect URI

The application uses a localhost redirect URI for desktop authentication.

Example:

```text
http://localhost
```

A temporary local callback may be used to receive the authentication response from Microsoft.

## Xbox Authentication

After Microsoft authentication succeeds, Maxima Launcher exchanges the Microsoft token for an Xbox Live user token.

The Xbox Live token is then exchanged for an XSTS token.

These tokens are used only as part of Minecraft account authentication.

## Minecraft Authentication

The XSTS token is used to authenticate with Minecraft Java Game Services.

Minecraft API access is used for features such as:

- verifying Minecraft: Java Edition ownership
- retrieving the Minecraft username
- retrieving the Minecraft UUID
- accessing the signed-in user's Minecraft Java profile
- managing the signed-in user's own Minecraft Java skin

Maxima Launcher does not provide Minecraft access to users who do not own the game.

## Minecraft API Approval

Minecraft Java Game Service APIs may require the Maxima Launcher Microsoft Application ID to be reviewed and approved by Microsoft/Mojang.

Until approval is granted, Minecraft Services may return an error such as:

```text
403 Invalid app registration
```

This does not mean that the Microsoft or Xbox login credentials are incorrect.

## Passwords

Maxima Launcher does not:

- request Microsoft passwords
- store Microsoft passwords
- process Microsoft passwords
- send Microsoft passwords to a Maxima Launcher server

Passwords are entered only on Microsoft's official authentication pages.

## Tokens

Authentication tokens are sensitive credentials.

At the current development stage, Maxima Launcher keeps authentication tokens only in memory for the active launcher session.

Tokens are not intentionally written to permanent Maxima Launcher storage.

Closing Maxima Launcher ends the current locally stored authentication session.

## Client Secret

Maxima Launcher does not use a client secret.

Desktop applications are public clients and cannot securely keep a client secret embedded in the application.

## Security

Users should verify that the Microsoft login page is hosted by an official Microsoft domain before entering account credentials.

Users should never enter their Microsoft password into a custom Maxima Launcher text field.

## Third-Party Services

Authentication depends on services operated by:

- Microsoft
- Xbox
- Minecraft / Mojang

Availability of authentication may therefore depend on those external services.

## Disclaimer

Maxima Launcher is an unofficial community project.

It is not affiliated with, endorsed by, sponsored by, or associated with Mojang Studios or Microsoft.

Minecraft is a trademark of Microsoft Corporation.
