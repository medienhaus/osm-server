<img src="./public/favicon.svg" width="70" />

### medienhaus/

Customizable, modular, free and open-source environment for decentralized, distributed communication and collaboration.

[Website](https://medienhaus.dev/) — [Fediverse](https://chaos.social/@medienhaus)

<br>

# medienhaus/osm-server
100% self-hosted OpenStreetMap tile server using [maptiler/tileserver-gl](https://github.com/maptiler/tileserver-gl). The provided styles stem from [openmaptiles/osm-bright-gl-style](https://github.com/openmaptiles/osm-bright-gl-style/), [openmaptiles/maptiler-toner-gl-style](https://github.com/openmaptiles/maptiler-toner-gl-style), and [openmaptiles/maptiler-basic-gl-style](https://github.com/openmaptiles/maptiler-basic-gl-style) respectively; we only modified them to load all resources from local files instead of publicly hosted CDNs.

## Instructions

This repository is only providing the structure for running the tile server. It assumes that you have placed a `planet.mbtiles` file in the root directory of the project. If you want to know more about generating such a file (or smaller variants that only include certain parts of the planet) check out the [onthegomap/planetiler](https://github.com/onthegomap/planetiler) repository.

1. Place `planet.mbtiles` in the project root
2. Run `npm i && node ./fonts/generate.js` to generate the necessary `.pbf` files for all fonts referenced in the provided styles
3. Run `docker-compose up` to start the tile server on port 8081
