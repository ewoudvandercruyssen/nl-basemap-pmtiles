# nl-basemap-pmtiles

Vector basemap of the Netherlands in [PMTiles](https://docs.protomaps.com/pmtiles/) format (Protomaps basemap schema, MVT, zoom 0–10).

| File | Zoom | Size |
|---|---|---|
| `nl-z10-test.pmtiles` | 0–10 | 31.9 MB |

## URL

Served via GitHub Pages (supports HTTP range requests and CORS):

```
https://ewoudvandercruyssen.github.io/nl-basemap-pmtiles/nl-z10-test.pmtiles
```

Preview: https://pmtiles.io/?url=https://ewoudvandercruyssen.github.io/nl-basemap-pmtiles/nl-z10-test.pmtiles

## MapLibre GL JS

```js
const protocol = new pmtiles.Protocol();
maplibregl.addProtocol("pmtiles", protocol.tile);

map.addSource("nl", {
  type: "vector",
  url: "pmtiles://https://ewoudvandercruyssen.github.io/nl-basemap-pmtiles/nl-z10-test.pmtiles",
  attribution: "© OpenStreetMap"
});
```

Note: the `buildings` layer starts at zoom 11, so it is empty in this z0–10 extract.

## License

Map data © [OpenStreetMap](https://www.openstreetmap.org/copyright) contributors, ODbL.
