# SubnauticaWatcher Mod

[![Build status](https://ci.appveyor.com/api/projects/status/3r9gd5tsnw7e0uah/branch/master?svg=true)](https://ci.appveyor.com/project/MartinSGill/subnauticawatcher/branch/master)
[![GitHub license](https://img.shields.io/github/license/mashape/apistatus.svg?style=flat)](http://opensource.org/licenses/MIT)
[![GitHub release](https://img.shields.io/badge/Current%20Release-v0.9-blue.svg?style=flat)](https://github.com/MartinSGill/SubnauticaWatcher/releases/tag/0.9.5)

## Purpose

This mod adds a "live" map to the [Subnautica][2] game. This can be considered a spoiler for the game.

Should the Subnautica development team ever add an auto-map or ingame map feature, this mod will be obsoleted.

## Motivation

I tend to get lost a lot in Subnautica. Exploring is great fun, but once I've found something, once I know where something is, I really want to be able to find it again. Beacons help a great deal, but for some things, like resources, when I don't have a beacon available or when I simply want to know which way to turn to get to a biome a map is invaluable.

If I were really trapped on 4546B I'd definitely be drawing a map, pinning it to wall in my cyclops, or drawing it in AlterraPaint on my PDA.

This mod is my personal answer to not having an in-game map. I'm making it available as I'm sure there must be at least one other person that would like an in-game (ish) map.

## Features

Check out the [List of Features](docs/features.md).

## Change Log

* v0.4 - Day / Night indicator
* v0.5 - Leviathan Spawns now in their own layer.
* v0.6 - Now able to automatically switch to correct base layer (e.g. Lost River, Lava Zone)
* v0.7 - Installer now handles cases where Subnautica is not in the default Steam library.
* v0.8 - New and updated biome layers
* v0.9 - Player view direction now indicated on map

![Mod in Use](docs/images/mod-example-overlay.png "Mod In Use")

## Installation

The instructions below should work for experienced users. If you're struggling with the installation, take a look at the [The Really Detailed Installation Guide](docs/installation.md)

__Warning:__ While attempts have been made to ensure this mod does not interfere with other mods, this cannot
be guaranteed.

__Warning:__ Only works on __Experimental__ branch.

__Warning:__ You may need to repeat steps 4 to 6 whenever Steam updates Subnautica.

1. Download the latest Release zip
2. Extract the zip into your Subnautica installation folder, (usually `Steam\steamapps\common\Subnautica`)
3. Unless updating, or unless you have another mod installed it should not normally require overwriting of anything.
4. In your `Steam\steamapps\common\Subnautica\SubnauticaWatcherInstaller` folder run `SubnauticaWatcherInstaller.exe`
5. Click the "Install" button.
6. Check for errors, then exit `SubnauticaWatcherInstaller.exe`.

## Usage

1. Run Subnautica as usual
2. Open Steam Overlay (usually by pressing "shift-tab")
3. Select "Web Browser"
4. Enter the URL: http://localhost:63030

## Troubleshooting

### Untrusted Publisher / Application

If you receive this warning from Windows, it's because this application isn't signed.

If you decide you want to trust this program, or you've read the source code and assured yourself it's benign, then you can [run the program anyway][1].

### My install is not detected!

The installer should correctly find Subnautica in almost all cases.
One edge case where it fails to correctly detect your install location is if you've moved your install.

For example you installed Subnautica in the default location, then moved or re-installed it on a different drive.

The problem is that the default/old installation folder (usually `c:\program files (x86)\steam\steamapps\common\Subnautica`) still exists.

Please delete or rename this folder and try installing again.

### Steam -102 Error

It's been reported that sometimes you get an error from Steam when typing the full URL into the Overlay Browser. Using merely localhost:63030 without the protocol part (http://) appears to work around this issue.

### Logs

As of version 0.3.0 the installer creates logs to help with error reporting and resolving issues.

You can find the logs in `Steam\steamapps\common\Subnautica\SubnauticaWatcherInstaller\Logs\{date}.log`

### Restore Subnautica to pristine state

1. Delete folder `Steam\steamapps\common\Subnautica\Subnautica_Data\Managed`
2. This will remove not only this mod, but every single other mod/tools/change you've made to this folder.
3. Open Steam
4. Find Saubnautica in your games list
5. Right-click and Select 'Properties'
6. On the 'Local Files' tab click on 'Verify Integrity of Game Files...'

This will cause steam to re-download all files that might have been changed by this mod, or other programs/mods.

[1]:https://www.pcworld.com/article/3197443/windows/how-to-get-past-windows-defender-smartscreen-in-windows-10.html
[2]:https://store.steampowered.com/app/264710/Subnautica/
