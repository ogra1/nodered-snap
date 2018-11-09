# node-red.snap

### Node-RED snap package

Base version of the Node-RED internet of things graphical wiring tool
packaged as an Ubuntu Snap, intended for multiple architectures.

Listens on port 1880 by default.

#### Building

To build locally, modify the snapcraft.yaml as required, and then execute `build_snap.sh`

#### Installing

    snap install node-red

When the snap is running you can view the Node-RED log using

    journalctl -f -u snap.node-red*

You can also stop and restart the application by

    snap disable node-red
    snap enable node-red

Currently the ONLY serial support is for /dev/ttyS0 style ports.
USB serial ports (hot-pluggable) are not supported by Snappy yet.

#### Settings

The **settings.js** and **flows.json** file are located in the `/root/snap/node-red/current/` directory.

The base port can be set by the `$PORT` environment variable, or in the `settings.js` file.
