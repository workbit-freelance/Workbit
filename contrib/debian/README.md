
Debian
====================
This directory contains files used to package WORKBITd/WORKBIT-qt
for Debian-based Linux systems. If you compile WORKBITd/WORKBIT-qt yourself, there are some useful files here.

## WORKBIT: URI support ##


WORKBIT-qt.desktop  (Gnome / Open Desktop)
To install:

	sudo desktop-file-install WORKBIT-qt.desktop
	sudo update-desktop-database

If you build yourself, you will either need to modify the paths in
the .desktop file or copy or symlink your WORKBITqt binary to `/usr/bin`
and the `../../share/pixmaps/WORKBIT128.png` to `/usr/share/pixmaps`

WORKBIT-qt.protocol (KDE)

