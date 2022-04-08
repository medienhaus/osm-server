<img src="./public/favicon.svg" width="70" />

### medienhaus/

Customizable modular free and open-source environment for decentralized, distributed communication and collaboration.

[Website](https://medienhaus.dev/) — [Twitter](https://twitter.com/medienhaus_)

<br>

# medienhaus/osm-server
100% self-hosted OpenStreetMap tile server using [maptiler/tileserver-gl](https://github.com/maptiler/tileserver-gl). The provided styles stem from [openmaptiles/osm-bright-gl-style](https://github.com/openmaptiles/osm-bright-gl-style/), [openmaptiles/maptiler-toner-gl-style](https://github.com/openmaptiles/maptiler-toner-gl-style), and [openmaptiles/maptiler-basic-gl-style](https://github.com/openmaptiles/maptiler-basic-gl-style) respectively; we only modified them to load all resources from local files instead of publicly hosted CDNs.

## Instructions

1. Place `europe.mbtiles` in the project root
2. Run `npm i && node ./fonts/generate.js` to generate the necessary `.pbf` files for all fonts referenced in the provided styles
3. Run `docker run --rm -it -v $(pwd):/data -p 8081:8080 maptiler/tileserver-gl` to start the tile server on port 8081