
# Data Management
For simplicity, it is recommended that you use Excel or an equivalent spreadsheet program to open and manipulate your dataset, and to save your dataset in CSV (Comma Separated Value) format.

## 1: Rows / Columns
Best practice is to have one column for each unique variable. The variable name should be the header for the column that contains the data. You will also want to consider whether every variable in your dataset should be published or made available. Many datasets include information about calibration coefficients, error parameters, and similar information which most users will not need or be interested in. There is also a recommended order for the columns. Typically the following order is recommended: platform_ID, time, latitude, longitude, depth/height (if applicable), latitude, longitude, and variables. Below is an example of what properly ordered rows and columns might look like:

| platform_ID | time | latitude | longitude | wind_spd (m s-1) | surface_temperature (C) |
| ----------- | -------------------- | -------- | -------- | ---------------- | ------------------------- |
| smb_buoy | 2014-09-16T10:05:03Z | 49.13287 | -58.2628 | 5.2 | 10.1 |
| smb_buoy | 2014-09-16T10:15:22Z | 49.13287 | -58.2628 | 5.3 | 10.1 |
| smb_buoy | 2014-09-16T10:25:17Z | 49.13287 | -58.2628 | 5.1 | 10.1 |

## 2: Date and Time
First, ensure that any date and/or time columns in your dataset are formatted and recognized as those types in the spreadsheet software that you are using.

Some information about getting your dates recognized properly within Excel can be found [here](https://answers.microsoft.com/en-us/msoffice/forum/all/excel-not-recognizing-dates-properly/2c8c61e6-28e3-480d-a37d-d144414ce1ad).

A number of different dates and times could be present in a given dataset, and all should be shown using standardized values, however the collection date/time will be of particular importance for ensuring interoperability of your data.

Next, in order to allow for dates to be interoperable, we will need to convert from the time zone used for data collection to the Coordinated Universal Time (UTC) timezone. [Convert Time Zones in Excel and Google Sheets](https://www.automateexcel.com/formulas/convert-time-zones/) provides examples on how to complete this conversion.

Once this is complete, the next step is to create a combined date and time column. If cell A2 contains the date, and B2 contains the time, the formula for the combined column is simply:

`=A2+B2`

### ISO 8601 Dates
ISO 8601 is an international standard for the worldwide exchange of date- and time-related data, and is based on a 24-hour clock. The format is: `YYYY-MM-DDThh:mm:ssZ`. The `Z` indicates UTC time, and `T` indicates the division between date and time.

## 3: Latitude and Longitude
If the location coordinates in your dataset are in degrees, minutes, seconds format, you can [follow the steps here](LAT_LON_CONVERSION.md) to convert it to the standard decimal degrees format.

## 4: Variable Names
To enable interoperability, it is important that all users utilize common names to describe the same variables. These are defined in *Controlled Vocabularies*, such as those listed below. For this step, apply a standard name from the Climate and Forecast Convetions Standard Name Table (see links below).

### Controlled Vocabularies

**CF Standard Names**: The Climate and Forecast Conventions include a standard name table that defines vocabularies to identify physical quantities. [Access the Standard Name Table here.](https://cfconventions.org/Data/cf-standard-names/current/build/cf-standard-name-table.html) If none of the available Standard Names accurately describe the variable or data within your dataset, it is possible to create a new name. Refer to the [Guidelines for Construction of CF Standard Names](http://cfconventions.org/Data/cf-standard-names/docs/guidelines.html) for information on how these Standard Names are constructred, and how new names might be derived following these conventions.

**NERC Vocabulary Server (NVS)**: "The NVS gives access to standardised and hierarchically-organized vocabularies. It is managed by the British Oceanographic Data Centre at the National Oceanography Centre (NOC) in Liverpool and Southampton, and receives funding from the Natural Environment Research Council (NERC) in the United Kingdom." [Access the NERC Vocabulary Server here.](http://vocab.nerc.ac.uk).

**Global Change Master Directory Keywords**: "Global Change Master Directory (GCMD) Keywords are a hierarchical set of controlled Earth Science vocabularies that help ensure Earth science data, services, and variables are described in a consistent and comprehensive manner and allow for the precise searching of metadata and subsequent retrieval of data, services, and variables. Initiated over twenty years ago, GCMD Keywords are periodically analyzed for relevancy and will continue to be refined and expanded in response to user needs." [Access the Global Change Master Directory Keywords here.](https://www.earthdata.nasa.gov/learn/find-data/idn/gcmd-keywords)

## 5: Units
For each variable, it is necessary to define an applicable unit which is defined in the header for the column, such as `wind_spd (m s-1)`. 

The Climate and Forecast Conventions defines a 'canonical unit' for each variable, which is necessary for compliance with this standard. Your variable must be either 1) in the canonical unit (e.g., Kelvin), or 2) in a format that is easily convertible to this unit (e.g., Celsius). As with variable names, it is important to use common names for units. You can explore this vocabulary in the [UDUNITS2 Database](https://ncics.org/portfolio/other-resources/udunits2/).

In most cases, there is software that will perform the conversion for you. However in some cases, it may be necessary to derive the conversion manually. In this situation, it is recommended to create an additional column with the new (derived) unit. To prevent this, it is recommended to consider the units when initially collecting the data to ensure compliance with the CF Conventions.
