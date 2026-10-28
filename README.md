# Forza Horizon 2 - Extra Options
A quality-of-life mod for the Xbox One version of Forza Horizon 2 that adds several tweaks to the game.

# WARNING
An individual or group of people is trying to use Forza Horizon 2 and the mod's name to perform a scan that adds a keylogger to your computer. There is **NO** "All-In-One" installation tutorial and anything that requires you to insert and run things on your PowerShell is a **scam.**

# Features
 - Built-in mod loader with addon and hooking support.
 - Change your car anywhere.
 - "Jump to Manufacturer" on car and rim menus.
 - All one-off races from online available offline.
 - Autodrive (as seen in Forza Horizon 6).
 - Drift Camera (as seen in Forza Horizon 4/5/6).
 - Ability to rev your engine in the engine swap menu.
 - FOV sliders for every camera type.
 - Roof toggle for supported cars during free-roam.
 - Lights, hazards, and turn-signal toggles for all cars.
 - New rim style category with all stock rims.
 - Custom spawn locations.
 - Customizable pause map zoom (optional, off by default).
 - "mediapc" modding folder support.
 - Native keyboard & mouse (optional, off by default).
 - Custom radio station with your own MP3s (optional, off by default).
 - Custom language packs with their own fonts and voice subtitles (optional, off by default).
 
# Enhancements
 - Skip developer opening videos.
 - No repeated "controller disconnected" pause without a pad (optional, off by default).
 - All DLC packs properly unlocked.
 - VIP status & "Treasure Map" unlocks.
 - Toggle for 4K liveries w/ enhanced sampling.
 - Sharper garage car pictures (optional, off by default).
 - Unrestricted Photo Mode.
 - Quick car scan in photo mode, ported from Forza Horizon 6 (optional, off by default).
 - Smooth menus: menus, replays and photo mode at up to 60 FPS instead of 30 (optional, off by default).
 - "Return to Garage" button in the pause menu.
 - Exit Game in the pause menu (optional, off by default).
 - Time of day and weather for the open world from a World tile in the pause menu (optional, off by default).
 - Aero tuning without equipping Forza Aero parts.
 - New rim style category with all aftermarket rims.
 - Toggle for having the minimap follow the orbit camera.
 - Bypass for Azimuth's save data checks.
 - Custom Gamerpic support.
 - FPS counter and performance log (optional, off by default).

# Installation

The installation is different depending on the translation layer you're using.

Azimuth:

 - Extract all the 3 files from the "Azimuth" folder in this ZIP to Azimuth's main folder where "Azimuth.exe" is located.

Mezcal:

 - Extract all the 4 files from the "Mezcal" folder in this ZIP to "Forza Horizon 2\Mount" which is where "forza_durango_release_final.exe" is located.

Note: Add this command if you're running Linux and using Wine: `WINEDLLOVERRIDES="winmm.dll=n,b" %command%`
More information on Linux support here: https://github.com/RokkuDayo/ForzaHorizon2_ExtraOptions/pull/35#issuecomment-6233015259

# Information

Most of the features can now be toggled and tweaked inside the game itself through the native menus.

### Treasure Map
The treasure map is disabled by default. Open the INI and set "UnlockTreasureMap" to 1 if you wish to have it.

### Autodrive
Autodrive is engaged by pressing D-Pad Down on a controller or F2 on a keyboard.

### Keyboard & Mouse
Off by default. Add this to `FH2_ExtraOptions.ini` to turn it on (Azimuth 1.0.2):
```ini
[KeyboardMouse]
Enabled=1
```
Keys answer the game's own input actions, so no virtual controller is involved and a pad keeps working. `Mode=Auto` (default) follows the last used device, `KBM` uses only the keyboard and mouse, and `PAD` leaves the gamepad path untouched.

Default keys follow the PC Forza titles: W/S throttle and brake, A/D steering, Space handbrake, E/Q gear up/down, Left Shift clutch, Tab camera, R rewind, Down or B look back, Enter/F/X activate, P photo mode, Left/Right radio, M map, Esc pause. In menus: Enter confirm, Esc back, arrow keys, Q/E tabs, X and Y buttons, Page Up/Down triggers, and Numpad 8/2/4/6 as the D-pad.

Every action above can be rebound with its name (`Throttle`, `Brake`, `SteerLeft`, `SteerRight`, `Handbrake`, `ShiftUp`, `ShiftDown`, `Clutch`, `Camera`, `Rewind`, `LookBack`, `Activate`, `PhotoMode`, `RadioPrevious`, `RadioNext`, `Map`, `Pause`, `Confirm`, `Back`, `Up`, `Down`, `Left`, `Right`, `TabLeft`, `TabRight`, `MenuX`, `MenuY`, `MenuLeftTrigger`, `MenuRightTrigger`, `DPadUp`, `DPadDown`, `DPadLeft`, `DPadRight`), up to three keys each, for example `Throttle=W,Up`. One key cannot drive two actions of the same group (driving or menus); such an INI is refused.

| Key | Default | Meaning |
| --- | --- | --- |
| `MouseLook` | 1 | The mouse turns the driving look camera. |
| `MouseLookPitch` | 0 | The mouse also looks up and down. |
| `InvertMouseY` | 0 | Inverts up/down mouse look. |
| `MouseCapture` | 1 | Keeps the mouse inside the window while driving. |
| `MouseSensitivity` | 80 | Mouse look speed (1-2000). |
| `MouseReturnDelay` | 1200 | Milliseconds before the look camera re-centres (0-60000). |
| `MouseReturnSpeed` | 240 | Re-centring speed (10-3600). |
| `SteeringSpeed` | 100 | Keyboard steering speed in percent (25-400). |
| `InvertSteering` | 0 | Swaps keyboard steering directions. |
| `Escape` | 1 | Esc pauses and goes back in menus. |
| `MenuCursor` | 1 | Mouse pointer in menus, the map, photo mode and the car viewer. |
| `CursorSize` | 250 | Pointer size in percent (50-800). |
| `MapCursorSpeed` | 400 | Map cursor speed in percent (50-800). |
| `MenuArrows` | Stick | Arrow keys act as the left stick (`Stick`) or the D-pad (`DPad`) in menus. |
| `Trace` | 0 | Logs every key and mouse event (diagnostics). |

With keyboard & mouse on and no pad attached, the game never pauses for a missing controller (see Controller-Missing Pause).

With keyboard & mouse on, the pause menu's Settings page also gets a **KEYBOARD & MOUSE** tile next to Controls. It opens its own page with the main options (input mode, mouse look, mouse look up/down, invert mouse Y, mouse sensitivity, keyboard steering speed, menu pointer, cursor size, map cursor speed) and one row per action. To rebind an action, choose its row (Enter, or Left/Right), then press the new key: Esc cancels, Backspace or Delete clears it, and a key already used by another action of the same group is refused. The Reset Key Bindings row restores the default keys, and the page's Reset to Default restores the options. Every change is written to `[KeyboardMouse]` in `FH2_ExtraOptions.ini` and applies at once.

### Controller-Missing Pause
Off by default. Without a paired pad (for example playing with a keyboard, or with a pad the game never paired to your profile), the game's "controller lost" rule pauses again every time the pause menu is closed. With this on, it pauses only when a pad that was connected is actually unplugged:
```ini
[Frontend]
PauseOnlyOnControllerUnplug=1
```
Esc, Menu and every other way of pausing work as before.

### Custom Radio Station
Off by default. Put MP3 files in a `Music` folder beside `FH2_ExtraOptions.ini` and add:
```ini
[CustomRadio]
Enabled=1
```
The files play in folder order as an extra station on the game's own radio, so the in-game radio volume, ducking, pausing and station banner all apply. MP3s are decoded by Windows.

| Key | Default | Meaning |
| --- | --- | --- |
| `Enabled` | 0 | Adds the station. |
| `Folder` | Music | The MP3 folder, beside the mod or an absolute path. |
| `Name` | MY MUSIC | The station name shown in game. |
| `Volume` | 100 | Station volume in percent (0-400). |
| `UnlockAllStations` | 0 | All stations are available regardless of progression (also works with `Enabled=0`). |
| `PcmDecode` | 1 | 0 hands the MP3s to the game's FMOD decoder instead. |

Keys are in `[Bindings]`: `RadioStation` tunes to the station (F9), `RadioNext` skips to the next track (F7) and `RadioRestart` restarts the track, or goes to the previous one within 3 seconds of its start (F6). Their Xbox bindings are `None` by default.

### Quick Car Scan
Off by default. A port of Forza Horizon 6's quick car scan: RB in photo mode credits the cars in view to the photo collection without taking a picture:
```ini
[PhotoMode]
QuickCarScan=1
```
RB (shown as "Scan cars" in the help bar) opens the game's own photo analysis for the current camera: the same car detection, payout and "Cars photographed" result as after a real photo, but nothing is captured or saved. It answers RB only in the camera and hidden-UI views; RB keeps its usual job in the effects panel and before saving.

### Car Previews
Off by default. The pictures of your own cars in My Cars and the car strip are rendered at the console's 816x459 (and 192x108), which looks soft at 1440p and 4K. Set a scale in `FH2_ExtraOptions.ini`:
```ini
[Graphics]
CarPreviewScale=2   ; 1 (default) = console size, 2-4 = that many times larger
```
2 is pixel for pixel in the My Cars panel at 2160p. It applies to pictures the game makes after startup (a car bought, painted or upgraded). To redraw the pictures you already have, press F8 (`[Bindings]` `RebuildCarPreviews`): every car with a saved picture is rendered again through the game's own background save. Stock cars use the game's packaged pictures and are not affected. Larger scales make the save larger (2 has four times the pixels).

### FPS Counter
Off by default. Put `fh2-monitor.dll` in a `monitor` folder beside `FH2_ExtraOptions.ini` (Azimuth 1.0.2) and add:
```ini
[Monitor]
ShowFps=1   ; 0 off, 1 FPS, 2 FPS with frame times
PerfLog=0   ; 1 writes fh2-perf.csv beside the INI
```
`ShowFps=1` shows the FPS, GPU load and video memory in the top-right corner. `ShowFps=2` adds the frame time, the 1% low and the GPU frame time. `PerfLog=1` appends one line per second to `fh2-perf.csv`: FPS, average, 99th percentile and longest frame times, the 1% low and the GPU frame time. The counter is drawn by the game's own swap chain on its presenting queue and follows HDR brightness.

### Map Zoom
Off by default. The pause map always opens at its farthest zoom-out (2500 m on the mainland, 1100 m on Storm Island). These set where it opens and how far it can zoom out, in percent of the game's own distances:
```ini
[Frontend]
MapStartZoom=150        ; opens at 150% of the game's distance (25-400, default 100)
MapMaxZoomOut=225       ; can zoom out to 225% (100-400, default 100)
MapIslandStartZoom=100  ; the same for Storm Island
MapIslandMaxZoomOut=175
```
Zooming keeps the game's speed in metres per second, and panning keeps its speed at a given distance. The island has its own values because its map texture ends close to the island. With all four at 100 nothing is changed.

### Exit Game
Off by default. The game has no way to quit from its menus. With this on, the pause menu's Home tab gets an Exit Game tile (the Quit icon, a caption in the game's language) beside Online Road Trip, which becomes a square tile, and choosing it closes the game:
```ini
[Frontend]
ExitGame=1
```

### Time of Day and Weather
Off by default. With this on, the pause menu's Settings page gets a World tile under Team Credits. It opens a World page with two rows that apply at once in the open world:
 - Time of Day: Default, Sunrise, Midday, Sunset, Midnight. A chosen time stops the clock there.
 - Weather: Default, Clear, Wet, Rain, Storm.

Default is the game's own time and weather; nothing is overridden. The choices are kept in the INI and applied again on the next start:
```ini
[Frontend]
WorldMenu=1

[World]
TimeOfDay=game
Weather=game
```
TimeOfDay takes game, sunrise, midday, sunset or midnight; Weather takes game, sunny, wet, rain or storm. The [World] values are used only while WorldMenu is 1.

### Smooth Menus
Off by default. The game's render scenarios run menus, replays and photo mode at 30 FPS, as on the console. This raises them to 60:
```ini
[Graphics]
SmoothMenus=1
```
Scenarios that already run at 60 (driving) are unchanged, and the frame rate is still limited by Azimuth's own frame rate setting: at 30 FPS in Azimuth nothing changes. The game reads the scenarios at startup, so restart the game after changing it.

### Custom Languages and Fonts
Off by default. A language pack plays the game in a language it does not ship, with its own fonts and subtitles for the spoken lines, and leaves the game's archives untouched. The pack takes over one of the game's language slots:
```ini
[Language]
Custom=uk   ; the pack in <game>\Mount\languages\uk\ (letters, digits, - and _)
```
Then choose the slot's language (for the Ukrainian pack: Russian, `ru-RU`) in the Azimuth launcher. Other slots keep the game's own languages.

The pack holds only the game files it changes, laid out like `mediaoverride`: an entry `media\X.zip\a\b` goes to `languages\<id>\X\a\b` (or the pack ships a whole `X.zip`), a loose `media\a\b` to `languages\<id>\a\b`. It is mounted over the game's media below `mediaoverride` and above `mediapc`, so `mediaoverride` > language pack > `mediapc` > mods > original files.
```text
Mount\languages\uk\
  language.ini
  stripped\stringtables\RU\*.str                 ; media\stripped\stringtables\RU.zip
  stripped\stringtables\RU\VoiceSubtitles.str    ; optional: voice subtitles
  ui\Fonts\Anthem_A.vfont ... verdana.vfont      ; media\ui\Fonts.zip: the pack's fonts
  cars\<car>\Cinematics\*_subtitles_RU.xml       ; loose files keep their path
```
`language.ini` names the pack and the slot it takes over (save it as UTF-16 when the name is not plain ASCII):
```ini
[Language]
Name=Українська
Slot=ru-RU   ; en-US, en-GB, de-DE, fr-FR, it-IT, es-ES, es-MX, pt-BR, pl-PL, ru-RU, ja-JP, ko-KR, zh-TW, zh-HK, nl-NL, cs-CZ or hu-HU
```
A pack without `language.ini` or with an unknown slot is logged and left off.

**Fonts.** Extra Options ships no fonts; it lets a pack bring them. A `.vfont` in the pack's `ui\Fonts\` replaces the game's font of the same name from `media\ui\Fonts.zip` through the same mount, for all text the game draws with it. The game picks its fonts per language in `Fonts.zip\fontsettings.xml`, which a pack can replace the same way. The pack is mounted whatever language the launcher runs, so its fonts apply to every language: keep the game's glyphs in them.

**Cyrillic.** The game's fonts cover Russian, but only partly:
- `Anthem_A`-`Anthem_D`, the game's UI fonts, have Latin glyphs plus `Ё ё` and no other Cyrillic.
- For the `RU` language `fontsettings.xml` adds `verdana.vfont` as their fallback. It has the 66 Russian letters, so Russian letters fall back to Verdana.
- None of them has the Ukrainian `Є є І і Ї ї Ґ ґ`, nor the Belarusian `Ў ў`, the Serbian/Macedonian `Ђ Ј Љ Њ Ћ Џ ...`, the Kazakh letters and so on. Those characters are missing from the text.
- For apostrophes, the fonts have `'` (U+0027) and `’` (U+2019), but not `ʼ` (U+02BC), so a translation uses `’`.

A Cyrillic-script language therefore reuses the `ru-RU` slot. That slot already loads the Cyrillic fallback for every UI font and has Russian voice audio and subtitles to replace. The pack then ships the fonts with its extra letters. The Ukrainian pack ships `Anthem_A`-`Anthem_D` with the full Cyrillic set added (320 glyphs instead of 248, so text keeps the game's typeface) and `verdana` with the 8 Ukrainian letters added. In other slots (`*` in `fontsettings.xml`) the game loads no Cyrillic font at all, so a pack there must bring complete fonts or its own `fontsettings.xml`.

**Voice subtitles.** The game shows no subtitles for many spoken lines (Ben, Ashley, ANNA). A pack can add them in `stripped\stringtables\<archive>\VoiceSubtitles.str`, a game string table (LSB2), loose or as a stored (uncompressed) entry of `<archive>.zip`:
- The row id is the last path component of the voice event, and its text is shown in the game's subtitle box while the line plays.
- An optional `<id>~t` row gives the line's length in seconds. Lines are shown for that time plus 0.6 s, at least 2 s and at most 60 s, or 3.6 s without the row.
- The display time follows the system clock, not the frame rate.

Voice subtitles are installed only when the launcher runs the game in the pack's slot. On Mezcal, the Windows locale counts as that choice.

`tools/make_language_pack.py` builds a pack from a translation mod's replacement archives. It compares them with the original media and keeps only what changed. The Ukrainian pack is 389 changed files (about 14 MB, fonts and voice subtitles included) instead of whole replaced archives.

### Drift Camera
The drift camera can be toggled and tweaked in the HUD settings inside the game.
Cockpit drift camera is enabled by default.

### Vehicle Lights
Lights can be toggled by clicking the right-stick.

Hazards can be toggled by tapping D-Pad Up.

Turn signals can be engaged by holding D-Pad Left/Right for 1 second; They will de-engage once a turn is made and the steering is centered.

Note: Some cars have glitched turn signals. More info at the [mod's Wiki page.](https://github.com/RokkuDayo/ForzaHorizon2_ExtraOptions/wiki/4.-Oddities)

### Roofs
Roofs can be toggled by pressing and holding the right-stick for 3 seconds while stationary.

# Custom gamerpic 
You can edit the "Gamerpic.png" image located where you extracted the mod files to with any image you like and it will be used as your avatar in-game.
The maximum dimensions supported are 2048x2048 and the image must weight less than 16 megabytes.

# AI Usage Disclosure
Codex was used in this project to create the DLL. The actual research was done manually, mostly based on things I already toyed with in the other titles from the series, but I don't yet have the C language knowledge to code something like this fully from scratch (I was initially editing the raw executable). Leaving this here as I believe people have the right to know.
