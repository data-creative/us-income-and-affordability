## [Developerweek Accelerate Hackathon](http://developerweek.com/hackathon/)

### Usage

View at http://bl.ocks.org/s2t2/cd45dfd8007fcf83fef7, or develop and view locally at http://localhost:8888/.

```` sh
git clone git@gist.github.com:/cd45dfd8007fcf83fef7.git
cd cd45dfd8007fcf83fef7/
python -m SimpleHTTPServer 8888 &
````

### Challenges

#### [Housing & Affordability in San Francisco](http://accelerate.im/challenges/64)
> How to identify and overcome San Francisco’s lack of affordable housing?

What is the affordability of housing in San Francisco, and how does it compare to other citites? [Affordability](http://en.wiktionary.org/wiki/affordability) is measured by "... cost relative to the amount that the purchaser is able to pay."

#### [Renters’ Rights in San Francisco](http://accelerate.im/challenges/65)
> How to improve the relationship of landlords and tenants in San Francisco?

What is the relationship between landlords and tenants?

#### [Landlords & Tenants in San Francisco](http://accelerate.im/challenges/66)
> How to strengthen renters’ rights by connecting renters with the City of San Francisco?

What are renter's rights? What resources are available to renters?

### Datasets

#### Affordability Data

Location affordability data is available from the census via data.gov on three [different](https://www.census.gov/geo/maps-data/data/tiger-cart-boundary.html) [levels](http://censusreporter.org/glossary/#term-cdp):
 1. core-based-statistical-area (like a Designated Market Area (DMA))
 2. county
 3. place

The [Location Affordability Index Data Dictionary](http://lai.locationaffordability.info/lai_data_dictionary.pdf)
applies to each of the three datasets.

COLUMN | SUFFIX | DESCRIPTION
--- | --- | ---
`income_min` | The minimum income for the geography as defined for the household above.
`income_max` | The maximum income for the geography as defined for the household above.
`income` |  The income for the geography as defined for the household above.
`size ` | The household size for geography as defined for the household above.
`workers` |  The number of commuters for the geography as defined for the household above.
`ht` | The modeled housing and transportation costs as a percent of income.
`h` |  The modeled housing costs as a percent of income.
`t` |  The modeled transportation costs as a percent of income.
... | ...

#### 1. [Location Affordability Index: All Core Based Statistical Areas (CBSAs)](http://catalog.data.gov/dataset/location-affordability-index-all-core-based-statistical-areas-cbsas)

There are [943](http://en.wikipedia.org/wiki/List_of_Core_Based_Statistical_Areas) [CBSAs](http://en.wikipedia.org/wiki/Core_Based_Statistical_Area) with identifiers ranging from '10020' to '49780'.

cbsa  | cbsa_name
--- | ---
'10020' | 'Abbeville, LA'
'10100' | 'Aberdeen, SD'
'10140' | 'Aberdeen, WA'
'10180' | 'Abilene, TX'
'10220' | 'Ada, OK'
'10300' | 'Adrian, MI'
'10420' | 'Akron, OH'
'10460' | 'Alamogordo, NM'
'10500' | 'Albany, GA'
'10540' | 'Albany-Lebanon, OR'
'10580' | 'Albany-Schenectady-Troy, NY'
'10620' | 'Albemarle, NC'
'10660' | 'Albert Lea, MN'
'10700' | 'Albertville, AL'
'10740' | 'Albuquerque, NM'
'10760' | 'Alexander City, AL'
'10780' | 'Alexandria, LA'
... | ...
 
#### 2. [Location Affordability Index: All Census Counties](http://catalog.data.gov/dataset/location-affordability-index-all-census-counties)

There are 3,144 counties with identifiers ranging from '01001' to '56045'.

county  | county_name
--- | ---
'01001' | 'Autauga'
'01003' | 'Baldwin'
'01005' | 'Barbour'
'01007' | 'Bibb'
'01009' | 'Blount'
'01011' | 'Bullock'
'01013' | 'Butler'
'01015' | 'Calhoun'
'01017' | 'Chambers'
'01019' | 'Cherokee'
'01021' | 'Chilton'
'01023' | 'Choctaw'
'01025' | 'Clarke'
'01027' | 'Clay'
'01029' | 'Cleburne'
'01031' | 'Coffee'
... | ...

#### 3. [Location Affordability Index: All Census Places](http://catalog.data.gov/dataset/location-affordability-index-all-census-places)

There are 24,011 places with identifiers ranging from '0100100' to '5686737'.

place | place_name
--- | ---
'0100100' | 'Abanda'
'0100124' | 'Abbeville'
'0100460' | 'Adamsville'
'0100484' | 'Addison'
'0100820' | 'Alabaster'
'0100988' | 'Albertville'
'0101132' | 'Alexander City'
'0101180' | 'Alexandria'
'0101228' | 'Aliceville'
'0101396' | 'Allgood'
'0101660' | 'Altoona'
'0101708' | 'Andalusia'
'0101756' | 'Anderson'
'0101852' | 'Anniston'
'0102116' | 'Arab'
'0102260' | 'Ardmore'
... | ...

#### Geography Data

Resources:
 + [CSA Shapes](https://catalog.data.gov/dataset/r2-combined-statistical-area-csa-2013-tiger-line-shapefile)
 + [CBSA Shapes](https://catalog.data.gov/dataset/r2-core-based-statistical-area-cbsa-2013-tiger-line-shapefile)
 + https://www.census.gov/geo/maps-data/data/tiger-cart-boundary.html
 + [Cartographic Boundary Shapefiles - Metropolitan and Micropolitan Statistical Areas and Related Statistical Areas](https://www.census.gov/geo/maps-data/data/cbf/cbf_msa.html)
 + [Cartographic Boundary Shapefiles - Counties](https://www.census.gov/geo/maps-data/data/cbf/cbf_counties.html) -- 500k, 5m, 20m
 + [Cartographic Boundary Shapefiles - Places (Incorporated Places and Census Designated Places)](https://www.census.gov/geo/maps-data/data/cbf/cbf_place.html) -- state by state datasets
 + http://ben.balter.com/2013/06/26/how-to-convert-shapefiles-to-geojson-for-use-on-github/
 + https://github.com/censusreporter/census-api
 + http://www.census.gov/data/developers/data-sets.html
 + http://www.census.gov/data/developers/data-sets/TIGERweb-map-service.html

Manual Process Documentation:

```` sh
cd cb_2013_us_cbsa_5m/
ogr2ogr -f GeoJSON -t_srs crs:84 cb_2013_us_cbsa_5m.geojson cb_2013_us_cbsa_5m.shp
````
