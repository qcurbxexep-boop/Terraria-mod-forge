# Terraria Mod Forge

A lightweight loader for managing and launching Terraria mods on desktop and mobile. Drop in your mods, pick a profile, and start the game with everything already wired up.

## Features

- Load and enable/disable mods without editing game files
- Profiles for switching between mod setups
- Automatic detection of mod dependencies and load order
- Log output for troubleshooting failed loads
- Desktop and mobile support (Android and iOS)

## Requirements

### Desktop
- Windows 10/11, Linux, or macOS
- Terraria (Steam or GOG install)
- .NET runtime 8.0 or newer

### Mobile
- Android 8.0 or newer, or iOS 15 or newer
- Terraria for mobile (Google Play, App Store, or equivalent)
- Mobile build of Terraria Mod Forge (see below)

## Installation

### Desktop

1. Download the latest release from the [Releases](../../releases) page.
2. Extract the archive to any folder.
3. Run `TerrariaModForge.exe` (or `TerrariaModForge` on Linux/macOS).
4. On first launch, point the loader to your Terraria install directory.

### Android

1. Download `terraria-mod-forge.apk` from the [Releases](../../releases) page.
2. Allow installs from your browser or file manager when prompted.
3. Open the app and grant storage access so it can read your Terraria data folder.
4. Choose your Terraria install folder when asked.

### iOS

1. Install Terraria Mod Forge from TestFlight or the App Store, depending on the release channel.
2. Open the app and select the Terraria app's save/data folder through the Files picker.
3. Mods placed in the loader's **mods** folder will appear in the list.

On iOS, the loader can only manage mods that Terraria's sandbox allows, so some mods may need the desktop version instead.

## Usage

1. Place mod files in the `mods/` folder next to the loader (on mobile, use the **Mods** tab to import them).
2. Open the loader and tick the mods you want enabled.
3. Choose a profile, or create a new one from the **Profiles** menu.
4. Tap or click **Launch** to start Terraria with the selected mods.

## Configuration

Settings are stored in `config.json` on desktop. On mobile, the same options are under **Settings** in the app.

```json
{
  "terrariaPath": "C:/Program Files (x86)/Steam/steamapps/common/Terraria",
  "modsPath": "./mods",
  "logLevel": "info",
  "defaultProfile": "default"
}
