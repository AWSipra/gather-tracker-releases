# Gather Tracker releases

Downloads for **Gather Tracker**, a desktop shopping-list helper for survival-crafting games
(Grounded 2 first), for Windows and Mac. The app's source code is private; this repository only
hosts releases.

## Install on Windows

1. Open [the latest release](https://github.com/AWSipra/gather-tracker-releases/releases/latest).
2. Download `GatherTracker-Setup-<version>.exe` and run it. It installs for your Windows user only
   (no admin rights needed) into `%LOCALAPPDATA%\Programs\GatherTracker`.
3. The installer isn't code-signed, so Windows SmartScreen may say "Windows protected your PC".
   Choose **More info**, then **Run anyway**.

## Install on Mac (Apple Silicon: M1 or newer)

1. Open [the latest release](https://github.com/AWSipra/gather-tracker-releases/releases/latest)
   and download `GatherTracker-<version>-mac.zip`. Safari usually unzips it for you; otherwise
   double-click the zip in Downloads.
2. Drag **GatherTracker** into your **Applications** folder.
3. Open it. The app isn't signed by Apple (it's a hobby project), so the first time macOS blocks
   it. To allow it:
   - Open **System Settings ▸ Privacy & Security**, scroll down to the message about
     GatherTracker, click **Open Anyway**, then confirm with your password or Touch ID.
   - If macOS instead says the app "is damaged and can't be opened", it isn't: that's how macOS
     treats unsigned downloads. Open **Terminal** and run this once, then open the app again:

     ```
     xattr -dr com.apple.quarantine /Applications/GatherTracker.app
     ```
4. You only need to do this once. Updates installed from inside the app open normally.

Intel Macs aren't supported yet.

## First start

The app asks for a contact email in Settings before it downloads anything from the wiki: the wiki
asks tools like this one to identify themselves. It's only sent in the request headers to the
wiki. Then press **Download item list** on the first screen (Data ▸ Refresh later picks up wiki
changes).

## Updates

The app checks this repository for a newer release when it starts (you can turn that off in
Settings) and installs it with one click: it downloads the file for your system, checks it against
the release's `.sha256` file, closes, installs and reopens. Your lists and downloaded wiki data are
never touched by installs, updates or uninstalls. They live in:

- Windows: `%LOCALAPPDATA%\GatherTracker`
- Mac: `~/Library/Application Support/GatherTracker`

## Credits

Item data comes from community wikis such as <https://grounded.wiki.gg>, licensed
CC BY-SA 4.0. The app downloads it on your machine and shows the source link for every item.
