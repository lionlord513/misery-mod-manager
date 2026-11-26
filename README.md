# MISERY Mod Manager

A portable Windows mod manager for MISERY. Drag in a mod, review its dependencies and load order, then choose **Install**. [Download the latest release](https://github.com/lionlord513/misery-mod-manager/releases/latest)

## Getting started

1. Extract the release ZIP and open **MISERY Mod Manager.exe**.
2. The manager finds MISERY in your Steam libraries. You can also choose the game folder in **Settings**.
3. Open **My mods** to see local mods and the signed-in account’s Workshop subscriptions. Pending downloads and disabled subscriptions appear here too. **Refresh** reads the latest subscription state from Steam.
4. Drop a ZIP, `.miserymod`, mod folder, Unreal container, or MISERY Workshop item link onto the window. You can drop a local mod and its dependencies together in any order.
5. Close MISERY, confirm the install preview, then choose **Play game**.

## Dependencies and load order

For local mods, the manager resolves declared requirements, checks versions, rejects dependency cycles and file ownership conflicts, and writes the loader’s configuration. A clean Lua installation gets UE4SS 4.0.0. Blueprint mods use BPModLoaderMod. Asset replacements retain their authored filenames and Unreal mount priority. Mod creators can provide a GitHub source for automatic dependency downloads. For other dependencies, the preview identifies the package to add.

For Workshop items, Steam supplies the author’s required-item list. The manager can subscribe to the dependencies and apply their local subscription order. **Mods Framework | MF** also needs its author’s one-time setup. After Steam downloads it, select its card and choose **Set up framework**. [Mods Framework instructions](https://steamcommunity.com/sharedfiles/filedetails/?id=3844850850)

## Updates and recovery

The manager checks this repository for updates at startup. When a newer release is available, review the notes and choose **Install update**. The manager verifies the release size and SHA-256 digest, replaces its executable, and reopens. **Settings → Check for updates** runs the same check on demand.

**Activity** records installs, errors and updates. **Settings → Backups** opens the local transaction backups. Mod creators can find an example manifest under **Settings → For mod creators**.

The manager includes the MIT-licensed UE4SS runtime. [Upstream UE4SS release](https://github.com/UE4SS-RE/RE-UE4SS/releases/tag/v4.0.0)

