Guide to install LoL with lol-wine and add to Lutris

*Setup LoL via lol-wine and lol-wine-glibc
yay -S lol-wine
yay -S lol-wine-glibc

mkdir Games-Wine
mkdir ~/Games-Wine/LoL

export WINEPREFIX=~/Games-Wine/LoL

export WINEARCH=win32

run /opt/wine-lol/bin/winecfg

add mscvp140.dll

Download LoL installer move to ~/Games-Wine/LoL/drive_c/

then run:

opt/wine-lol/bin/wine ~/Games-Wine/LoL/drive_c/installer-name.exe

DONT launch after install

add to Lutris

Game info:

League of Legends
Runner:

Wine

*Game Options:
Executable: /home/your-user/Games-Wine/LoL/drive_c/Riot Games/League of Legends/LeagueClient.exe
Wine Prefix: ~/Games-Wine/LoL
Prefix Architeture: 32-bit

*Runner Option
Wine Version: Custom
Custom wine executable: /opt/wine-lol/bin/wine

Enable D9VK

Vulkan ICD Loader: select the json from your gpu nvidia or amd
