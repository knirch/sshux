altgr intl knirch

my windows keyboard mappings that allow me to use
swedish characters on an english keyboard layout.

use https://www.microsoft.com/en-us/download/details.aspx?id=102134
Microsoft Keyboard Layout Creator (MSKLC) Version 1.4

(not available through winget sadly)

requires .NET framework version 3.5

Open PowerShell as an administrator and run the following command: Enable-WindowsOptionalFeature -Online -FeatureName "NetFx3" This will automatically download, install and enable.NET Framework 3.5 on your PC. Download and install.NET


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

