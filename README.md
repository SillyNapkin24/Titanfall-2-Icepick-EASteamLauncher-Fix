# Titanfall 2 Icepick – EA App / EASteamLauncher Fix

> **Having trouble with IcePick timing out after launching Titanfall 2?**
>
> This community fork fixes a Steam/EA App compatibility issue where Icepick could no longer detect the Titanfall 2 process.

This is an unofficial community compatibility fix for Titanfall 2 Icepick.

## What this fixes

A September 2026 EA App update appears to have changed the parent process used when launching Titanfall 2 through Steam from:

`EASteamProxy`

to:

`EASteamLauncher`

The original Icepick process detection was looking for EASteamProxy, causing Icepick to time out after 60 seconds with:

"Timed out after 60 seconds. Could not find Titanfall 2 process."

If Icepick launches Titanfall 2 but eventually produces this timeout, this build is intended to address that issue.

This build changes the Steam parent-process detection to `EASteamLauncher`

## Tested

Tested successfully with:

- Titanfall 2 Steam version (Sept 2026)
- EA App version 13.796.0.6309
- Icepick successfully injecting into Titanfall 2

## Installation

### Steam users

If you own Titanfall 2 through Steam, leave Icepick's launcher selection set to **Steam**.

The EA App is still used behind the scenes for Steam copies of Titanfall 2. This fix does not change which launcher Icepick should use; it only updates Icepick's detection of the EA/Steam launch process.

1. Back up your existing Icepick installation.
2. Download Titanfall-2-Icepick.exe below.
3. Replace your existing Icepick executable with the downloaded file.
4. Launch Icepick normally.

No Titanfall 2 game files need to be modified.

## Source

This is a fork of the original Titanfall 2 Icepick project by Titanfall Mods.

Only the Steam parent-process detection was changed.

Original project:
https://github.com/Titanfall-Mods/Titanfall-2-Icepick

## Disclaimer

This is an unofficial community build and is not affiliated with or endorsed by the original Icepick developers.

# Titanfall 2 Icepick

This is the launcher for Titanfall 2 that will inject the TTF2SDK.dll into the game, as well as list and manage updates for mods.

## Requirements

 - Visual Studio 2019
 - DotNet Framework 4.6

## Building

 - Update nuget packages
 - Build Solution via Visual Studio

## Third-party Libraries

The Titanfall 2 Icepick makes use of the following third-party libraries:

| Package Name        | URL                                                                  |
|---------------------|----------------------------------------------------------------------|
| Newtonsoft.Json     | https://github.com/JamesNK/Newtonsoft.Json                           |
