# Gather Tracker releases

Installers for **Gather Tracker**, a Windows desktop shopping-list helper for survival-crafting
games (Grounded 2 first). The app's source code is private; this repository only hosts releases.

## Install

1. Open [the latest release](https://github.com/AWSipra/gather-tracker-releases/releases/latest).
2. Download `GatherTracker-Setup-<version>.exe` and run it. It installs for your Windows user only
   (no admin rights needed) into `%LOCALAPPDATA%\Programs\GatherTracker`.
3. The installer isn't code-signed yet, so Windows SmartScreen may say "Windows protected your PC".
   Choose **More info**, then **Run anyway**.

## Updates

The app checks this repository for a newer release when it starts (you can turn that off in
Settings) and installs it with one click. Your lists and downloaded wiki data live in
`%LOCALAPPDATA%\GatherTracker` and are never touched by installs, updates or uninstalls.

Each release also has a `.sha256` file; the app checks the download against it before installing.

## Credits

Item data comes from community wikis such as <https://grounded.wiki.gg>, licensed
CC BY-SA 4.0. The app downloads it on your machine and shows the source link for every item.