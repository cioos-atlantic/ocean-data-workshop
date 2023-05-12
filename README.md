# Ocean Data Workshop

## Sample data

A sample raw data file will be used during this workshop:
[sample data](sample_data/wsp_wave_buoy_raw.csv)

One objective of the workshop will be to take this CSV file in raw form and transform it into a standards-compliant dataset, following the CF conventions.
[CF conventions](https://cfconventions.org)

### ISO 19115 Metadata

Most international ocean observing systems use the [ISO 19115 Geograophic information metadata standard](https://www.iso.org/standard/53798.html), and extend the ISO19115 schema for use in their regions. 

ISO 19115 is made up from three documents:
* ISO19115-1 defines the core standard
* ISO19115-2 is an extension for data acquisition and processing
* ISO19115-3 defines the XML schema implementation

For more information about the ISO 19115 standard and how it has been implemented across different regions and organizations globally, see the [Research Data Alliance (RDA) metadata standards page](https://rdamsc.bath.ac.uk/msc/m22).

## Metadata entry tools

### CIOOS metadata entry form

The CIOOS metadata entry form can be accessed here:
https://cioos-siooc.github.io/metadata-entry-form/#/en/region-select

## Unit conversions

### Latitude and longitude

If the location coordinates in your dataset are in degrees, minutes, seconds format, you can [follow the steps here](LAT_LON_CONVERSION.md) to convert it to the standard decimal degrees format.

### Date and time

First, ensure that any date and/or time columns in your dataset are formatted and recognized as those types in the spreadsheet software that you are using.

Some information about getting your dates recognized properly within Excel can be found [here](https://answers.microsoft.com/en-us/msoffice/forum/all/excel-not-recognizing-dates-properly/2c8c61e6-28e3-480d-a37d-d144414ce1ad).

A number of different dates and times could be present in a given dataset, and all should be shown using standardized values, however the collection date/time will be of particular importance for ensuring interoperability of your data.

Once the collection date and time columns are recognized in the spreadsheet, the next step is to create a combined date and time column. If cell A2 contains the date, and B2 contains the time, the formula for the combined column is simply:

`=A2+B2`

Next, we will need to convert from the to UTC time

