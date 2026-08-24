# Waifu Maker

Waifu Maker is a Windows AI companion that shares a virtual room with you. Chat by text or voice, spend time together, and use activities such as **Work Together** while your companion responds with character-aware behaviour and memory.

> [!IMPORTANT]
> Waifu Maker is currently in ** beta**. These builds are intended for  testers and may contain bugs, unfinished behaviour, or breaking changes.

[Download the latest closed-beta release](https://github.com/llmk51ll/waifu-maker-releases/releases/latest)

## What you can do

- Talk with your companion through text and generated voice.
- See her move through and interact with the virtual room.
- Use **Work Together**, including spoken check-ins and a timer-completion chime.
- Build continuity through local long-term memory and recent-chat cloud sync.
- Receive supported updates from inside the installed app.

## Install on Windows

1. Open the [latest release](https://github.com/llmk51ll/waifu-maker-releases/releases/latest).
2. Under **Assets**, download the file named `waifu-maker-setup-<version>.exe`.
3. Run the installer. It installs for the current Windows user and does not require administrator permission.
4. Sign in with Google when prompted to use the online features.

The installer is currently **unsigned**, so Microsoft Defender SmartScreen will warn you. Only continue when the file came from this official repository. Select **More info → Run anyway** for the verified Waifu Maker installer. Do not bypass SmartScreen for a copy from another source.

Files such as `latest.yml` and `.blockmap` are used by the automatic updater; most users do not need to download them.

## Updates

If you already have Waifu Maker 0.3.0 or later installed, the app can notify you when a supported update is available. Follow the in-app steps to download it, then restart the app to install it.

You can also install a newer version manually from the [Releases page](https://github.com/llmk51ll/waifu-maker-releases/releases).

## Privacy summary

Waifu Maker uses both local and online services:

- Long-term Memory V2 is stored locally in SQLite on your computer.
- Signed-in use syncs a recent-chat copy, relationship state, and save state to Firebase. The developer can technically access this cloud copy.
- Chat text is sent through the developer's Cloud Run proxy to Mistral to generate replies.
- Reply text is normally sent through the proxy to ElevenLabs for voice generation, unless a local voice fallback is used.
- Optional current-information search sends the search query through the proxy to Brave Search.
- Local data deletion and cloud data deletion are separate actions under **Account → Data Management**.

Please review the in-app privacy notice before starting your first online chat.

## Current limitations

- Windows x64 only.
- The installer is approximately 905 MB.
- The installer is not code-signed and may trigger SmartScreen or antivirus warnings.
- Voice uses a developer-funded monthly quota. Text chat remains available if that quota is exhausted.
- This is beta software, so visuals, companion behaviour, and memory handling are still being tuned.

## Report a problem

In the app, open **Account → Report a problem**. This prepares diagnostic logs with the app version and operating-system details so they can be included in a bug report.

When reporting an issue, please include:

- What you were doing when it happened.
- What you expected to happen.
- What happened instead.
- Whether restarting the app fixes it.

Do not post private conversations, access tokens, or other sensitive information in a public GitHub issue.

## Releases

| Version | Highlights |
| --- | --- |
| [0.3.1](https://github.com/llmk51ll/waifu-maker-releases/releases/tag/0.3.1) | Improved room positioning, spoken Work Together check-ins, timer chime, mood-aware voice, character-grounded daily life, and memory fixes. |
| [0.3.0](https://github.com/llmk51ll/waifu-maker-releases/releases/tag/0.3.0) | First Windows x64 closed-beta build with the installer, in-app update support, privacy consent, balanced graphics mode, and local Memory V2 controls. |

Full changes and known issues are documented on each release page.

## About this repository

This repository is the official distribution channel for Waifu Maker Windows builds and automatic-update metadata. It contains release binaries and related files; it is not the application source-code repository.
