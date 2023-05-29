# Ocean Data Workshop

## Sample data

A sample raw data file will be used during this workshop:
[sample data](sample_data/wsp_wave_buoy_raw.csv)

One objective of the workshop will be to take this CSV file in raw form and transform it into a standards-compliant dataset that follows the Climate and Forecast (CF) Conventions. There are a variety of open source tools that "understand" CF data, including compliance checkers to determine whether your data is compliant with the CF Conventions.

[CF Conventions](https://cfconventions.org)  
[US IOOS Compliance Checker](https://compliance.ioos.us/index.html) [Online, Web-based]

## Metadata
Metadata is data that describes data. It uses structured elements to describe data in a precise way, and provides information about the data that can be used for classifying, organizing, labeling, sorting, or searching it. 

### Metadata Terms (from [University of Pittsburg Library System FAQs](https://pitt.libanswers.com/faq/214800))

A *metadata element* is a field containing a piece of information about the data. For example: 'title', 'author', 'latitude', 'longitude', etcetera.

A *metadata schema* is "a logical plan showing the relationships between metadata elements. It defines the semantics, the syntax, and the optionality of the metadata elements (sometimes called “metadata fields”) that make up the metadata standard."

A *metadata standard* is "a high level document which establishes a common way of structuring and understanding data, and includes principles and implementation issues for utilizing the standard." A standard is a schema that is maintained by a governing body.

A *metadata profile* "describes the use of metadata elements declared in a metadata standard and/or schema for a specific application or use-case. It adds rules and guidelines on the use of the elements, identifies element obligations and constraints (e.g. controlled vocabularies, name authorities, and encoding schemes), and provides comments and examples to assist in the understanding of the elements. An application profile may include metadata elements integrated from one or more metadata standards/schema. This allows it to meet the needs of a specific application or use-case."

### ISO 19115
Most international ocean observing systems use the [ISO 19115 Geographic information metadata standard](https://www.iso.org/standard/53798.html), and extend the ISO19115 schema for use in their regions. 

ISO 19115 is made up from three documents:
* ISO 19115-1 defines the core standard
* ISO 19115-2 is an extension for data acquisition and processing
* ISO 19115-3 defines the XML schema implementation

For more information about the ISO 19115 standard and how it has been implemented across different regions and organizations globally, see the [Research Data Alliance (RDA) metadata standards page](https://rdamsc.bath.ac.uk/msc/m22).

## Controlled Vocabularies

### NERC Vocabulary Server (NVS)

"The NVS gives access to standardised and hierarchically-organized vocabularies. It is managed by the British Oceanographic Data Centre at the National Oceanography Centre (NOC) in Liverpool and Southampton, and receives funding from the Natural Environment Research Council (NERC) in the United Kingdom." [Access the NERC Vocabulary Server here.](http://vocab.nerc.ac.uk).

### Global Change Master Directory Keywords

"Global Change Master Directory (GCMD) Keywords are a hierarchical set of controlled Earth Science vocabularies that help ensure Earth science data, services, and variables are described in a consistent and comprehensive manner and allow for the precise searching of metadata and subsequent retrieval of data, services, and variables. Initiated over twenty years ago, GCMD Keywords are periodically analyzed for relevancy and will continue to be refined and expanded in response to user needs." [Access the Global Change Master Directory Keywords here.](https://www.earthdata.nasa.gov/learn/find-data/idn/gcmd-keywords)

### CF Standard Names

The Climate and Forecast Conventions include a standard name table that defines vocabularies to identify physical quantities. [Access the Standard Name Table here.](https://cfconventions.org/Data/cf-standard-names/current/build/cf-standard-name-table.html)

If none of the available Standard Names accurately describe the variable or data within your dataset, it is possible to create a new name. Refer to the [Guidelines for Construction of CF Standard Names](http://cfconventions.org/Data/cf-standard-names/docs/guidelines.html) for information on how these Standard Names are constructred, and how new names might be derived following these conventions.
