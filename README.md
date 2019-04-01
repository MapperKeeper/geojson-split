# geojson-split

Split properties from a stream of GeoJSON

```sh
$ geojson-split ./test/locations.geojson > ./test/properties.json
```

[GeoJSON](http://geojson.org/) is great.  It is a simple standard format for
encoding a variety of geographic data structures.  Since it is an open specification,
many programs already know how to work with it.  

If you just want to modify the properties (title, description, etc) for different
features, you can do so easily by updating the .geojson file directly.  However,
many features have complex geometries that can overwhelm your text editor.  This
tiny script pulls the properties object from your GeoJSON and streams them to
a new JSON file.

Now, you can edit your GeoJSON properties without needing to load all the geometry
information.

## Next Steps

After modifying your properties, you can join them back to your original GeoJSON
file using [geojson-join](https://www.npmjs.com/package/geojson-join) from [Tom MacWright](https://github.com/tmcw).
