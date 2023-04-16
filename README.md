# Keyboard tweaks

## Keyboard layout

    altgr intl knirch

A small variation on the international keymap, which places the swedish umlauts
on a, e and o. 

### Building

To compile and install, use [Microsoft Keyboard Layout Creator][msklc]. Not available through winget.

It requires .NET Framework 3.5 to be installed. Start `powershell` with administrator privileges.

```ps
    Enable-WindowsOptionalFeature -Online -FeatureName "NetFx3"
```

Open MSKLC and load the layout. Under `project` run `Build DLL and Setup Package`.

Open the directory created, install the layout via `setup`.

[msklc]: https://www.microsoft.com/en-us/download/details.aspx?id=102134

### Using

For me it gets installed as a extra keyboard layout on English (United States).

#### Windows 10

It's not possible to switch to that layout via `win + space`, but with `alt + left shift` hotkey it will cycle through the languages, and appear stuck when cycling through a language with multiple layouts.

Recommended is to set up a language with only one layout so that the normal switcher reports the correct keyboard, probably?

##### Rabbit-hole

The `alt + left shift` was found under one of those links in the control panel. 

Windows has lots of odd ways of getting to certain configuration windows.

`control /Name Microsoft.Language`
`control /name Microsoft.RegionalAndLanguageOptions`
`rundll32.exe Shell32.dll,Control_RunDLL "input.dll,,{C07337D3-DB2C-4D0B-9A93-B722A6C106E2}"`
`rundll32.exe Shell32.dll,Control_RunDLL "input.dll,,{C07337D3-DB2C-4D0B-9A93-B722A6C106E2}{HOTKEYS}"`

randomly picked up somewhere; Try Windows Key + R, and enter ms-settings:privacy-webcam –
SO THERE ARE EVEN MORE WAYS?!



"Text Services and Input Languages"
Language Bar
Advanced Key Settings
"Input language hot keys"
"Advanced Key Settings"

Windows 11:
Time & language > Typing > Advanced keyboard settings
* Language bar options
* Input language hot keys


Old style config window:

"Text Services and Input Languages"

Tabs:
"Language Bar"
"Advanced Key Settings"


win11:
Control /Name Microsoft.Language :: Time & language > Language & region
in here, click on Typing, then "Advanced keyboard settings", then on "Language bar options" or "Input language hot keys".
this leads to the rundll thing.





Control /Name Microsoft.Language  gets you to the same destination as "Language Preferences"

in there you can tweak your languages, or click on Keyboard, clicking on that gives you more
links, like; Language bar options, which opens the old style window mentioned above
and "Input language hot keys" which opens the same, but on the tab "Advanced Key Settings"

most settings in here doesnt seem to do anything on windows 10, at least
when it comes to the language bar settings.

"Override for default input method"
Use language list (recommended)
or pick the keyboard layout.


go to language preferences


control /name Microsoft.RegionalAndLanguageOptions
control /name Microsoft.Language




how people find these are a complete mystery to me.. but.. hey, that's one way of finding your way to that setting if it tickles your fancy


but now I'm super frustrated as to how people know this magical incantation to begin with.. how? and how is {HOTKEYS} magically found as well? .... 

seems good as well: https://learn.microsoft.com/en-us/windows/win32/shell/executing-control-panel-items




### Crap

    WARNING: ^ (U+005e) is already defined more than once on the keyboard (on VK_6, ShiftState 'Ctl+Alt' and VK_6, ShiftState 'Shift').
    WARNING: ö (U+00f6) is already defined more than once on the keyboard (on VK_P, ShiftState 'Ctl+Alt' and VK_O, ShiftState 'Ctl+Alt').
    WARNING: Ö (U+00d6) is already defined more than once on the keyboard (on VK_P, ShiftState 'Shift+Ctl+Alt' and VK_O, ShiftState 'Shift+Ctl+Alt').
    WARNING: ä (U+00e4) is already defined more than once on the keyboard (on VK_Q, ShiftState 'Ctl+Alt' and VK_E, ShiftState 'Ctl+Alt').
    WARNING: Ä (U+00c4) is already defined more than once on the keyboard (on VK_Q, ShiftState 'Shift+Ctl+Alt' and VK_E, ShiftState 'Shift+Ctl+Alt').
    WARNING: å (U+00e5) is already defined more than once on the keyboard (on VK_W, ShiftState 'Ctl+Alt' and VK_A, ShiftState 'Ctl+Alt').
    WARNING: Å (U+00c5) is already defined more than once on the keyboard (on VK_W, ShiftState 'Shift+Ctl+Alt' and VK_A, ShiftState 'Shift+Ctl+Alt').
    WARNING: ` (U+0060) is already defined more than once on the keyboard (on VK_OEM_3, ShiftState 'Ctl+Alt' and VK_OEM_3, ShiftState 'Base').
    WARNING: ~ (U+007e) is already defined more than once on the keyboard (on VK_OEM_3, ShiftState 'Shift+Ctl+Alt' and VK_OEM_3, ShiftState 'Shift').
    WARNING: ' (U+0027) is already defined more than once on the keyboard (on VK_OEM_7, ShiftState 'Ctl+Alt' and VK_OEM_7, ShiftState 'Base').
    WARNING: " (U+0022) is already defined more than once on the keyboard (on VK_OEM_7, ShiftState 'Shift+Ctl+Alt' and VK_OEM_7, ShiftState 'Shift').

it's a bit crap


caps lock as control

install sharpkeys;
winget install -e RandyRants.SharpKeys

https://github.com/randyrants/sharpkeys/

Special: Caps Lock (00_3a) -> Special: Left Ctrl (00_1d)

see more details at : https://renenyffenegger.ch/notes/Windows/registry/tree/HKEY_LOCAL_MACHINE/System/CurrentControlSet/Control/Keyboard-Layout/index

dual function ctrl key

DualCTRL-Esc.ahk

Tap for Escape, hold for left ctrl

lifted from ;http://www.autohotkey.com/board/topic/103174-dual-function-control-key/
other variants can be found at https://vim.fandom.com/wiki/Map_caps_lock_to_escape_in_Windows


Microsoft Visual Studio Code (User)    XP9KHM4BK9FZ7Q                         1.77.3                            msstore
Microsoft Update Health Tools          {89581302-705F-42C5-99B0-E368A845DAD5} 3.70.0.0
PS C:\Users\knirc> winget search ahk
Name       Id                    Version   Match        Source
--------------------------------------------------------------
AutoHotkey Lexikos.AutoHotkey    1.1.36.01 Moniker: ahk winget
AutoHotkey AutoHotkey.AutoHotkey 2.0.2     Moniker: ahk winget
Switch     ahkohd.switch         1.0.23                 winget
PS C:\Users\knirc> winget install -e autohotkey.autohotkey
No package found matching input criteria.
PS C:\Users\knirc> winget install -e AutoHotkey.AutoHotkey
Found AutoHotkey [AutoHotkey.AutoHotkey] Version 2.0.2
This application is licensed to you by its owner.
Microsoft is not responsible for, nor does it grant any licenses to, third-party packages.
This package requires an install location
Specify the install root: An unexpected error occurred while executing the command:
0x8a150042 : Error reading input in prompt
PS C:\Users\knirc> winget install -e Lexikos.AutoHotkey
Found AutoHotkey [Lexikos.AutoHotkey] Version 1.1.36.01
This application is licensed to you by its owner.
Microsoft is not responsible for, nor does it grant any licenses to, third-party packages.
Downloading https://github.com/Lexikos/AutoHotkey_L/releases/download/v1.1.36.01/AutoHotkey_1.1.36.01_setup.exe
  ██████████████████████████████  3.19 MB / 3.19 MB
Successfully verified installer hash
Starting package install...
Successfully installed
PS C:\Users\knirc>

so I mean... wot..

didnt care to update the script currently to work in ahk2, as that one asked me
a weird question.. 

shrug


