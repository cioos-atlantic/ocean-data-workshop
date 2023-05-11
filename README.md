# Ocean Data Workshop

## Sample data

A sample raw data file will be used during this workshop:
[sample data](sample_data/wsp_wave_buoy_raw.csv)

One objective of the workshop will be to take this CSV file in raw form and transform it into a standards-compliant dataset that follows the Climate and Forecast (CF) Conventions. There are a variety of open source tools that "understand" CF data, including compliance checkers to determine whether your data is compliant with the CF Conventions.

[CF Conventions](https://cfconventions.org)
[US IOOS Compliance Checker](https://compliance.ioos.us/index.html) [Online, Web-based]


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

### ISO 8601 Dates



## Controlled Vocabularies

### NERC Vocabulary Server (NVS)

"The NVS gives access to standardised and hierarchically-organized vocabularies. It is managed by the British Oceanographic Data Centre at the National Oceanography Centre (NOC) in Liverpool and Southampton, and receives funding from the Natural Environment Research Council (NERC) in the United Kingdom." [Access the NERC Vocabulary Server here.](http://vocab.nerc.ac.uk).

### Global Change Master Directory Keywords

"Global Change Master Directory (GCMD) Keywords are a hierarchical set of controlled Earth Science vocabularies that help ensure Earth science data, services, and variables are described in a consistent and comprehensive manner and allow for the precise searching of metadata and subsequent retrieval of data, services, and variables. Initiated over twenty years ago, GCMD Keywords are periodically analyzed for relevancy and will continue to be refined and expanded in response to user needs." [Access the Global Change Master Directory Keywords here.](https://www.earthdata.nasa.gov/learn/find-data/idn/gcmd-keywords)

### CF Standard Names

The Climate and Forecast Conventions include a standard name table that defines vocabularies to identify physical quantities. [Access the Standard Name Table here.](https://cfconventions.org/Data/cf-standard-names/current/build/cf-standard-name-table.html)

If none of the available Standard Names accurately describe the variable or data within your dataset, it is possible to create a new name. Refer to the [Guidelines for Construction of CF Standard Names](http://cfconventions.org/Data/cf-standard-names/docs/guidelines.html) for information on how these Standard Names are constructred, and how new names might be derived following these conventions.
