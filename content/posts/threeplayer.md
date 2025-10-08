+++
title = 'How a three player battle works'
date = 2024-06-03T09:22:57-04:00
draft = false
+++

## How a three player battle works
Because it does not work with the LAN patch.

### What works
Melonds same computer multiplayer works with three player.
But how does one get that working with a container environment?

### The QT build in VNC server
QT the toolkit Melonds uses has this cool feature where you can set how is displays called platform plugins.
There is a platform plugin for VNC.
VNC is a protocol KASM supports.

*note the package for qt in ubuntu that has the vnc plugin is called qt6-qpa-plugins. The snap of melonds work by default*
