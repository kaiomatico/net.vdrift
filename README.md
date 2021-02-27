# Updated TORCS Flatpak
I updated the Flatpak SDK and freeglut and added the debian >gcc7 fix to the TORCS flatpak. Original forked from here: 
- https://github.com/flathub/net.sourceforge.torcs
- https://flathub.org/apps/details/net.sourceforge.torcs

# Installation instructions
```
flatpak install flathub org.freedesktop.Platform//20.08 org.freedesktop.Sdk//20.08
git clone --recurse-submodules https://github.com/kaiomatico/net.sourceforge.torcs.git
cd net.sourceforge.torcs
flatpak-builder build-dir net.sourceforge.torcs.json --force-clean
flatpak-builder --user --install build-dir net.sourceforge.torcs.json --force-clean
flatpak run net.sourceforge.torcs
```

# Uninstall instructions
```
flatpak uninstall --delete-data net.sourceforge.torcs
```

# Notes
Fullscreen does not work properly, so just run it in windowed mode and increase the resolution. I have tried different patches and plib versions but was not able to fix it.