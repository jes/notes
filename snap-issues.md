# Snap issues

Issues with Snaps on Ubuntu 24.04 LTS:

 * Kdenlive can't render a project, stuck at "Waiting..." forever, has existed since at least 2021: https://forum.snapcraft.io/t/kdenlive-cannot-render-any-projects-stuck-in-waiting/26689 - remove and reinstall with `--classic` to get it to work
 * Inkscape gcodetools can't write into my home directory, the only way I managed to get gcode out of it is because I realised it *can* write to `/home/jes/snap/inkscape/common` - but then I can't load the gcode into FreeCAD because FreeCAD can't *read* `/home/jes/snap/inkscape/common` - so I have to manually copy the file somewhere else first
 * "Recent files" in file dialogs seems to be inconsistent, like some Snaps have a separate store of recent files that is not connected to my main Gnome one