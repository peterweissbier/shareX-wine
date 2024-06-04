Run winetricks
Select "Select the default wineprefix"
Select "Install a Windows DLL or component"
Find the latest dotnet version and select it
Close winetricks
Run the ShareX setup file by running wine /path/to/setup.exe
Finally run ShareX from your applications menu.

Troubleshooting & Protips
If the UI looks ugly, change the font to "Open Sans" or whatever you like by going to "Application settings --> Theme" (change MenuFont and ContextMenuFont) and run winecfg from your terminal and change the font DPI by navigating "Graphics --> Screen resolution" to 112 DPI.
If capturing an area or screen crashes the app or gives an error, try using Workflows submenu.
If you are trying to assign shortcuts use xdotool. Example for Ctrl+Print:
xdotool key --window $( xdotool search --limit 1 --all --pid $( pgrep ShareX )) "ctrl+Print"
