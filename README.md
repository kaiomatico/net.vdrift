# VDRIFT Flatpak
This is a Flatpak for the Racing Sim VDRIFT
- https://github.com/VDrift/vdrift/
- https://vdrift.net/


# Installation instructions
```
flatpak install flathub org.freedesktop.Platform//20.08 org.freedesktop.Sdk//20.08
git clone --recurse-submodules https://github.com/kaiomatico/net.vdrift.git
cd net.vdrift
sudo apt install subversion
flatpak-builder build-dir net.sourceforge.vdrift --force-clean
flatpak-builder --user --install build-dir net.sourceforge.vdrift --force-clean
flatpak run net.sourceforge.vdrift
```

# Uninstall instructions
```
flatpak uninstall --delete-data net.vdrift
```