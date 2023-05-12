
# Data Management

## Unit conversions

### Latitude and longitude

If the location coordinates in your dataset are in degrees, minutes, seconds format, you can [follow the steps here](LAT_LON_CONVERSION.md) to convert it to the standard decimal degrees format.

### Date and time

First, ensure that any date and/or time columns in your dataset are formatted and recognized as those types in the spreadsheet software that you are using.

Some information about getting your dates recognized properly within Excel can be found [here](https://answers.microsoft.com/en-us/msoffice/forum/all/excel-not-recognizing-dates-properly/2c8c61e6-28e3-480d-a37d-d144414ce1ad).

A number of different dates and times could be present in a given dataset, and all should be shown using standardized values, however the collection date/time will be of particular importance for ensuring interoperability of your data.

Once the collection date and time columns are recognized in the spreadsheet, the next step is to create a combined date and time column. If cell A2 contains the date, and B2 contains the time, the formula for the combined column is simply:

`=A2+B2`

Next, in order to allow for dates to be interoperable, we will need to convert from the time zone used for data collection to the UTC timezone.

### ISO 8601 Dates