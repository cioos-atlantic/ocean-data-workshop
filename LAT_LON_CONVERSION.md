
# Converting lat/long data to decimal degrees

## Web-based conversion tool

Try converting the point
44° 42′ 0″ N, 63° 38′ 0″ W
from degrees, minutes, seconds format to decimal degress using the web-based conversion tool here:
https://www.fcc.gov/media/radio/dms-decimal

## Converting a column of data 

Given a column that looks like:

| Position |
| -- |
| 44° 42' 0" N, 63° 38' 0" W |
| ... |

You can copy all the data from this column into the following batch conversion tool to convert to degrees, minutes, seconds format:

https://rechneronline.de/geo-coordinates/batch.php

Once converted, you will get the latitude and longitudes separated by a space:

44.7 -63.633333
...

Paste this list of data into your spreadsheet:

| Position | lat_long |
| - | - |
| 44° 42' 0" N, 63° 38' 0" W | 44.7 -63.633333 |
| ... |

Next, create separate latitude and longitude columns. For the latitude column, enter the formula:

`=LEFT(B2,FIND(" ",B2,1)-1)`

Where 'B' can be replaced with the column letter for the 'lat_long' column, and fill this formula down all cells in the column.

Similarly for longitude, use the formula:

`=RIGHT(B2,LEN(B2)-SEARCH(" ",B2,1))`

Replacing 'B' for the correct column letter and filling down as in the latitude case.