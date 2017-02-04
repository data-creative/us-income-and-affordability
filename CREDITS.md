# Credits, Notes, and Reference

## Converting from old Gist

  + [Old Repo (gist)](https://gist.github.com/s2t2/cd45dfd8007fcf83fef7)
  + [How to merge with old repo](http://stackoverflow.com/questions/37937984/git-refusing-to-merge-unrelated-histories)
  + [How to reset to previous commit](http://stackoverflow.com/questions/17667023/git-how-to-reset-origin-master-to-a-commit)

## Affordability Data

See the [data dictionary](/DICTIONARY.md).

## Geography Data

  + [CSA Shapes](https://catalog.data.gov/dataset/r2-combined-statistical-area-csa-2013-tiger-line-shapefile)
  + [CBSA Shapes](https://catalog.data.gov/dataset/r2-core-based-statistical-area-cbsa-2013-tiger-line-shapefile)
  + https://www.census.gov/geo/maps-data/data/tiger-cart-boundary.html
  + [Cartographic Boundary Shapefiles - Metropolitan and Micropolitan Statistical Areas and Related Statistical Areas](https://www.census.gov/geo/maps-data/data/cbf/cbf_msa.html) -- 500k, 5m, 20m
  + [Cartographic Boundary Shapefiles - Counties](https://www.census.gov/geo/maps-data/data/cbf/cbf_counties.html) -- 500k, 5m, 20m
  + [Cartographic Boundary Shapefiles - Places (Incorporated Places and Census Designated Places)](https://www.census.gov/geo/maps-data/data/cbf/cbf_place.html) -- state by state datasets
  + http://ben.balter.com/2013/06/26/how-to-convert-shapefiles-to-geojson-for-use-on-github/
  + https://github.com/censusreporter/census-api
  + http://www.census.gov/data/developers/data-sets.html
  + http://www.census.gov/data/developers/data-sets/TIGERweb-map-service.html

Shapefile to GeoJSON conversion process:

```` sh
brew install gdal
````

```` sh
cd cb_2013_us_cbsa_5m/
ogr2ogr -f GeoJSON -t_srs crs:84 cb_2013_us_cbsa_5m.geojson cb_2013_us_cbsa_5m.shp
````

```` sh
cd cb_2013_us_county_5m/
ogr2ogr -f GeoJSON -t_srs crs:84 cb_2013_us_county_5m.geojson cb_2013_us_county_5m.shp
````

## Mapping

 + http://gis.stackexchange.com/a/70557
 + http://bsumm.net/2013/03/31/analyzing-mbostocks-queue-js.html
 + https://github.com/mbostock/queue
 + http://bl.ocks.org/mbostock/4060606
 + https://github.com/mbostock/d3/wiki/Arrays#d3_map

> NOTE: It is not methodologically sound to aggregate measures across household types (i.e. to calculate the mean or median of all household types within a given geography).
