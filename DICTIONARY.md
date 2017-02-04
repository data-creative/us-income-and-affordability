# Data Dictionary

## Affordability Data

Location affordability data is available from the census via data.gov on three [different](https://www.census.gov/geo/maps-data/data/tiger-cart-boundary.html) [levels](http://censusreporter.org/glossary/#term-cdp):
 1. core-based-statistical-area (like a Designated Market Area (DMA))
 2. county
 3. place

The [Location Affordability Index Data Dictionary](http://lai.locationaffordability.info/lai_data_dictionary.pdf) applies to each of the three datasets.

It defines eight types of households.

COLUMN PREFIX | HOUSEHOLD TYPE | SIZE OF HH | INCOME | # COMMUTERS
--- | --- | --- | --- | ---
hh_type1_ | Median-Income | Family | 4 Median Income for Region | 2
hh_type2_ | Very Low-Income | Individual | 1 National Poverty Line | 1
hh_type3_ | Working Individual | 1 | 50% of Median Income for Region | 1
hh_type4_ | Single Professional | 1 | 135% of Median Income for Region | 1
hh_type5_ | Retired Couple | 2 | 80% of Median Income for Region | 0
hh_type6_ | Single-Parent Family | 3 | 50% of Median Income for Region | 1
hh_type7_ | Moderate-Income Family | 3 | 80% of Median Income for Region | 1
hh_type8_ | Dual-Professional Family | 4 | 150% of Median Income for Region | 2

It defines at least the following metrics for each type of household, and provides measures of each.

COLUMN SUFFIX | DESCRIPTION
--- | ---
`income_min` | The minimum income for the geography as defined for the household above.
`income_max` | The maximum income for the geography as defined for the household above.
`income` |  The income for the geography as defined for the household above.
`size ` | The household size for geography as defined for the household above.
`workers` |  The number of commuters for the geography as defined for the household above.
`ht` | The modeled housing and transportation costs as a percent of income.
`h` |  The modeled housing costs as a percent of income.
`t` |  The modeled transportation costs as a percent of income.
... | ... and more


### By CBSA

[Location Affordability Index: All Core Based Statistical Areas (CBSAs)](http://catalog.data.gov/dataset/location-affordability-index-all-core-based-statistical-areas-cbsas)

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

### By County

[Location Affordability Index: All Census Counties](http://catalog.data.gov/dataset/location-affordability-index-all-census-counties)

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

### By Place

[Location Affordability Index: All Census Places](http://catalog.data.gov/dataset/location-affordability-index-all-census-places)

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
