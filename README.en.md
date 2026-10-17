<img src="media/icon.png" width="96" align="right" alt="">

# mybestlap

[Italiano](README.md)

An overlay for **Assetto Corsa EVO** that shows, while you drive, how the setup in use is doing
against the best one you have tried with the same car on the same track. Every lap is recorded
with the setup it was driven with, so you know which setup gave the fastest lap and where it
gains or loses.

**[Download the latest version](https://github.com/agastal/mybestlap-Release/releases/latest)** ·
[What's new](CHANGELOG.md) · [Guide](https://github.com/agastal/mybestlap-Release/wiki) · [Buy me a coffee](https://www.paypal.com/paypalme/agastalink)

![mybestlap overlay over the track](media/overlay.png)

![The three layouts: column, grid and bar](media/overlay-layout.png)

*Example values (Italian labels). Top left the column, top right the grid, below the bar.*

## Install

1. Download `mybestlap-<version>-setup.exe` from the [latest release](https://github.com/agastal/mybestlap-Release/releases/latest).
2. Run it: it installs for your user, no administrator rights.
3. The icon appears in the notification area, by the clock. Start Assetto Corsa EVO and drive.

Play the game **windowed or borderless full screen**: over exclusive full screen an external
overlay may not show.

Updates come by themselves: when a new version is out the app says so, and *Install update* in the
icon's menu installs it in one click. Settings and laps stay.

## What the overlay shows

| Measure | Notes |
| --- | --- |
| Best setup and its lap | for the car and track in use |
| Live gap to the best lap | point by point along the track; green ahead, red behind |
| Setup in use and lap time | under the gap |
| Tyre and brake temperatures, average and peak | per wheel, per axle or one figure |
| Average and peak speed | of the lap being driven |
| Fuel per lap and per minute | of the last finished lap |

Layout (column, grid, bar), transparency, measures, font and sizes are chosen in **Settings**
(double-click the icon), and the overlay follows while you change them.

## Shortcuts

| Keys | Action |
| --- | --- |
| Ctrl+Shift+F7 | show or hide the overlay |
| Ctrl+Shift+F8 | place the overlay: drag it, double-click to fix it |

They work with the game in front and can be changed in Settings.

## How it knows the setup

- The setup loaded or saved from the game's setup page.
- **Unsaved changes** too: a lap driven with "TEST03 + camber" is a variant of its own. Save it
  under a name later and the laps already driven take that name.
- The setup is the one in force when you leave the pits; fuel does not count.
- Delete a setup in the game and its laps leave the archive.

Only valid laps begun at the line count for the best lap and the gap: the out-lap does not.

## Setup comparison

From the icon's menu, **Setup comparison** opens a page in the browser where you pick car and
track. **Times**: the setups best first, with best lap, median, the three sectors (and what they
gain or lose) and **clean laps**, how many laps were valid and free of slides, off-tracks and
contacts. **Behaviour**: temperatures, speed, fuel and balance (understeer/oversteer); the best
figure of each column is in green.
[More in the guide](https://github.com/agastal/mybestlap-Release/wiki/Setup-comparison).

## Privacy

Everything stays on your PC, in `%LOCALAPPDATA%\mybestlap`. The app reads, read only, the game's
shared memory, its log and its setups folder; it changes nothing in the game. It sends nothing:
its only connection is the update check on this repository, once a day, which can be turned off
in Settings.

## Checking the download

Each release has `SHA256SUMS.txt` and `antivirus.txt` (a Microsoft Defender scan of that setup).
The setup is not code-signed, so Windows may warn you the first time.

```powershell
Get-FileHash mybestlap-<version>-setup.exe -Algorithm SHA256
```

---

*Unofficial community project, not affiliated with Assetto Corsa EVO, Kunos Simulazioni or 505 Games.*
Bundled fonts under the SIL Open Font License: Barlow Condensed, Chakra Petch, JetBrains Mono, IBM Plex Sans.
