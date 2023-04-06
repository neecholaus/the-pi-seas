# the-pi-seas :anchor:

## What does each container do?
#### `plex-media-server`
Runs Plex, which provides a service for streaming files and media through your browser or other compatible devices.

Access via port `32400` and the path `/web`, (when in a browser).

#### `filebrowser`
Provides a clean interface, accessible via browser, for managing the filesystem mounted in the docker override file.

The main directory holding all media files should be mounted to `/srv`.

Access via port `8080`.

#### `vpn`
Provides an isolated VPN network, which blocks all internet traffic should the connection drop.

Currently configured for Mullvad usage, but the underlying container, [gluetun](https://github.com/qdm12/gluetun), supports many others.

#### `transmission`
Provides a torrent client, which uses the network of the vpn container.

Access via port `9091`.
