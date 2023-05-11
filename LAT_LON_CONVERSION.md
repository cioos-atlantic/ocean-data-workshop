
# Converting lat/long data to decimal degrees

## Web-based conversion tool

Try converting the point
44° 42′ 0″ N, 63° 38′ 0″ W
from degrees, minutes, seconds format to decimal degress using the web-based conversion tool here:
https://www.fcc.gov/media/radio/dms-decimal

## Converting a column of data in Excel

Given a column that looks like:

| Position |
| -- |
| 44°42′0″N, 63°38′0″W |
| ... |

First, split this into separate columns, 

| Position | N_degrees | N_minutes | N_seconds | W_degrees | W_minutes | W_seconds | latitude | longitude |
| - | - | - | - | - | - | - | - | - |
| 44°42′0″N, 63°38′0″W | 44 | 42 | 0 | 63 | 38 | 0 |  |  |
| ... | | | | | | | | |

Now, for the latitude column, apply the following formula to all data cells in the column (subsituting Excel letters for the column names as needed):

`=N_degrees+(N_minutes/60)+(N_seconds/3600)`

For the longitude column, apply the following formula to all data cells in the column:

`=W_degrees+(W_minutes/60)+(W_seconds/3600)`

