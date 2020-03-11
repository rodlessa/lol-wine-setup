# Guide to install LoL with lol-wine and add to Lutris, based on [u/ridethenuke from reddit](https://old.reddit.com/r/leagueoflinux/comments/bx0y2s/success_latest_arch_linux_winelol_patch_911/)

## Setup LoL via lol-wine and lol-wine-glibc
yay -S wine-lol

yay -S wine-lol-glibc

## Create folders and setup Wine

mkdir Games-Wine

mkdir ~/Games-Wine/LoL

export WINEPREFIX=~/Games-Wine/LoL

export WINEARCH=win32

### Run

/opt/wine-lol/bin/winecfg

add mscvp140.dll

## Download LoL installer move to ~/Games-Wine/LoL/drive_c/
then run:

/opt/wine-lol/bin/wine ~/Games-Wine/LoL/drive_c/installer-name.exe

## DONT launch after install

### Add to Lutris

Game info:

League of Legends
Runner:

Wine

## Game Options:
Executable: /home/your-user/Games-Wine/LoL/drive_c/Riot Games/League of Legends/LeagueClient.exe

Wine Prefix: ~/Games-Wine/LoL

Prefix Architeture: 32-bit

## Runner Option
Wine Version: Custom

Custom wine executable: /opt/wine-lol/bin/wine

Enable D9VK

Vulkan ICD Loader: select the json from your gpu nvidia or amd

## lib32 packages

Sometimes league wont work without some packages, thanks to /u/So_Romii from r/leagueoflinux i found the i needed 2 libs after a fresh Arch install:
' sudo pacman -S lib32-vulkan-validation-layers lib32-sdl '
