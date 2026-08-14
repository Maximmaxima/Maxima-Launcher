# Security Policy

## Overview

Security is important for Maxima Launcher, especially because the launcher interacts with Microsoft, Xbox and Minecraft authentication services.

Maxima Launcher is currently under active development.

## Reporting a Security Issue

If you discover a security vulnerability in Maxima Launcher, please report it responsibly.

Please do not publicly disclose security vulnerabilities before they have been reviewed.

You can report security issues through the GitHub repository.

When reporting an issue, include as much information as possible, such as:

- a description of the vulnerability
- steps to reproduce the issue
- the affected Maxima Launcher version
- screenshots or logs if relevant
- the potential security impact

## Microsoft Account Security

Maxima Launcher does not request or store Microsoft account passwords.

Microsoft authentication takes place through Microsoft's official login pages using OAuth 2.0 Authorization Code Flow with PKCE.

Users should never enter their Microsoft password directly into a custom Maxima Launcher window.

## Client Secrets

Maxima Launcher is a public desktop application.

No Microsoft client secret is embedded or distributed with the launcher.

Secrets should never be committed to this repository.

## Authentication Tokens

Authentication tokens must be treated as sensitive information.

Do not:

- publish access tokens
- publish refresh tokens
- publish Xbox Live tokens
- publish XSTS tokens
- publish Minecraft access tokens
- include authentication tokens in screenshots
- commit authentication tokens to GitHub

At the current development stage, Maxima Launcher keeps authentication tokens only in memory for the active launcher session.

## Logs

Logs may contain technical information useful for debugging.

Before publishing launcher logs, users should check that they do not contain:

- authentication tokens
- private account information
- personal file paths they do not want to share
- email addresses
- other sensitive information

## Downloads

Users should only download Maxima Launcher from trusted project sources.

Modified or unofficial builds may contain changes that are not part of the official Maxima Launcher project.

## Dependencies

Maxima Launcher uses third-party libraries and services.

Security issues discovered in dependencies may require Maxima Launcher to update or replace those dependencies.

## Supported Versions

Maxima Launcher is currently under active development.

The latest development version should generally be considered the supported version.

Older development builds may not receive security fixes.

## Responsible Disclosure

Please allow reasonable time for a reported vulnerability to be investigated and fixed before publishing technical details.

## Disclaimer

Maxima Launcher is an unofficial community project.

It is not affiliated with, endorsed by, sponsored by, or associated with Mojang Studios or Microsoft.

Minecraft is a trademark of Microsoft Corporation.
