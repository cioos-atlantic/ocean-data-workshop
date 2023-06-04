
# Data Management
For simplicity, it is recommended that you use Excel, Google sheets, or an equivalent spreadsheet program to open and manipulate your dataset, and to save your final dataset in CSV (Comma Separated Value) format.

## 1: Rows / Columns
Best practice is to have one column for each unique variable. The variable name should be the header for the column that contains the data. You will also want to consider whether every variable in your dataset should be published or made available. Many datasets include information about calibration coefficients, error parameters, and similar information which most users will not need or be interested in. There is also a recommended order for the columns. Typically the following order is recommended: platform_ID, time, latitude, longitude, depth/height (if applicable), and variables. Below is an example of what properly ordered rows and columns might look like:

| platform_ID | time | latitude | longitude | wind_spd (m s-1) | surface_temperature (C) |
| ----------- | -------------------- | -------- | -------- | ---------------- | ------------------------- |
| smb_buoy | 2014-09-16T10:05:03Z | 49.13287 | -58.2628 | 5.2 | 10.1 |
| smb_buoy | 2014-09-16T10:15:22Z | 49.13287 | -58.2628 | 5.3 | 10.1 |
| smb_buoy | 2014-09-16T10:25:17Z | 49.13287 | -58.2628 | 5.1 | 10.1 |

## 2: Date and Time

### ISO 8601 Dates
ISO 8601 is an international standard for the worldwide exchange of date- and time-related data, and is based on a 24-hour clock. The format is: `YYYY-MM-DDThh:mm:ssZ`. The `Z` indicates UTC time, and `T` indicates the division between date and time. 

For timezones other than UTC, use + or - followed by the number of hours to shift UTC, e.g. YYYY-MM-DDThh:mm:ss-0400.

For more information about ISO 8601 dates, see the [Wikipedia page](https://en.wikipedia.org/wiki/ISO_8601).

### Spreadsheet Date formats

Excel and Google Sheets unfortunately do not yet have simple methods for generating ISO8601-formatted dates from their internal date and time formats. However, they can be made to format the dates in a somewhat similar way, which will help ease the conversion in future when integrating the data into an ocean data repository while still allowing for the date and time objects to be handled appropriately while working in the spreadsheet environment.

First, ensure that any date and/or time columns in your dataset are formatted and recognized as those types in the spreadsheet software that you are using.

Some information about getting your dates recognized properly within Excel can be found [here](https://answers.microsoft.com/en-us/msoffice/forum/all/excel-not-recognizing-dates-properly/2c8c61e6-28e3-480d-a37d-d144414ce1ad).

A number of different dates and times could be present in a given dataset, and all should be shown using standardized values, however the collection date/time will be of particular importance for ensuring interoperability of your data.

Next, in order to allow for dates to be interoperable, we will need to convert from the time zone used for data collection to the Coordinated Universal Time (UTC) timezone. [Convert Time Zones in Excel and Google Sheets](https://www.automateexcel.com/formulas/convert-time-zones/) provides examples on how to complete this conversion. Once all times in your time column are converted to UTC, add text such as "(UTC)" to your time column header to retain this metadata about the timezone used.

For date columns that have no time component, format the date as ISO by selecting the cells to format, right clicking, and using the YYYY-MM-DD format option.

Once this is complete, the next step is to create a combined date and time column. If cell A2 contains the date, and B2 contains the time, the formula for the combined column is simply:

`=A2+B2`

This will show the date/time as YYYY-MM-DD hh:mm:ss, and since the time is now in UTC, only minor changes will be needed in future to convert this to compliant ISO 8601 formatted dates.

## 3: Latitude and Longitude
If the location coordinates in your dataset are in degrees, minutes, seconds format, you can [follow the steps here](LAT_LON_CONVERSION.md) to convert it to the standard decimal degrees format.

## 4: Variable Names
To enable interoperability, it is important that all users utilize common names to describe the same variables. These are defined in *Controlled Vocabularies*, such as those listed below. For this step, apply a standard name from the Climate and Forecast Convetions Standard Name Table (see links below).

### Controlled Vocabularies

**CF Standard Names**: The Climate and Forecast (CF) Conventions include a standard name table that defines vocabularies to identify physical quantities. [Access the Standard Name Table here.](https://cfconventions.org/Data/cf-standard-names/current/build/cf-standard-name-table.html) If none of the available Standard Names accurately describe the variable or data within your dataset, it is possible to create a new name. Refer to the [Guidelines for Construction of CF Standard Names](http://cfconventions.org/Data/cf-standard-names/docs/guidelines.html) for information on how these Standard Names are constructred, and how new names might be derived following these conventions.

**NERC Vocabulary Server (NVS)**: "The NVS gives access to standardised and hierarchically-organized vocabularies. It is managed by the British Oceanographic Data Centre at the National Oceanography Centre (NOC) in Liverpool and Southampton, and receives funding from the Natural Environment Research Council (NERC) in the United Kingdom." [Access the NERC Vocabulary Server here.](http://vocab.nerc.ac.uk). See the NVS collections list [here](https://vocab.nerc.ac.uk/collection/)  for all the different standard vocabularies available on the NVS.

**BODC P01 Vocabulary**: The P01 vocabulary defined by BODC fulfills a similar role to the CF standard names, but with additional detail in some cases, and the NVS gives some information about crosswalks between the two vocabularies. Check with the ocean observing system or other organization that you plan to submit your data to about which of BODC P01 or CF names is preferred. Typically North American systems will rely on CF names while many EU systems use BODC terms. CIOOS standardizes on CF, but since the Government of Canada often uses BODC terms, we sometimes support both. [Access the BODC P01 search via NVS here.](https://vocab.nerc.ac.uk/search_nvs/P01/)

**Global Change Master Directory Keywords**: "Global Change Master Directory (GCMD) Keywords are a hierarchical set of controlled Earth Science vocabularies that help ensure Earth science data, services, and variables are described in a consistent and comprehensive manner and allow for the precise searching of metadata and subsequent retrieval of data, services, and variables. Initiated over twenty years ago, GCMD Keywords are periodically analyzed for relevancy and will continue to be refined and expanded in response to user needs." [Access the Global Change Master Directory Keywords here.](https://www.earthdata.nasa.gov/learn/find-data/idn/gcmd-keywords)

## 5: Units
For each variable, it is necessary to define an applicable unit which is defined in the header for the column, such as `wind_spd (m s-1)`. 

The Climate and Forecast Conventions defines a 'canonical unit' for each variable, which is necessary for compliance with this standard. Your variable must be either 1) in the canonical unit (e.g., Kelvin), or 2) in a format that is easily convertible to this unit (e.g., Celsius). As with variable names, it is important to use common names for units. You can explore this vocabulary in the [UDUNITS2 Database](https://ncics.org/portfolio/other-resources/udunits2/). In most cases, there is software that will perform the conversion for you.

As with standard variable names, BODC has also defined units, using the P06 vocabulary. Depending on your region you may consider using P06 units instead of, or in addition to UDUNITS. You can search for appropriate units for the variables in your dataset using the [BODC P06 search on NVS.](https://vocab.nerc.ac.uk/search_nvs/P06/)
