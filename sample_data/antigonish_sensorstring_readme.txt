
Antigonish Water Quality Data README

Abstract:  The Centre for Marine Applied Research (CMAR) provides high resolution ocean data from around the coast of Nova Scotia through their Coastal Monitoring Program. Through the Water Quality Branch of the program, CMAR collects temperature, dissolved oxygen, and salinity data using sensors deployed on stationary moorings. A typical mooring consists of a line anchored to the sea floor and suspended by a sub-surface buoy, with sensors attached at various depths. Alternatively, sensors may be attached to structures including buoys, docks, or aquaculture equipment. Sensors are deployed for several months, and data are measured every 1 minute to 1 hour. Station locations, summary reports, and data collection methods are available on the CMAR website (https://cmar.ca/coastal-monitoring-program/). Datasets and reports may be revised pending ongoing data collection and analyses. Automated Quality Control tests were applied to the data to identify outlying and unexpected observations. The results of these tests are summarized in the “qc_flag” columns of the dataset. Observations flagged as “Pass” passed all tests, while observations flagged as “Fail” failed at least one test and should be excluded from most analyses. “Suspect/Of Interest” flags highlight unusual events or poor quality data, and “Not Evaluated” flags indicate at least one test was not applied to the observation. Flags should be used as a guide only, and users are responsible for evaluating the data quality prior to use. For technical details on the Quality Control tests, visit the CMAR Data Governance website (https://dempsey-cmar.github.io/cmp-data-governance/pages/cmp_about.html). Other data quality considerations: - Through calibration-validation procedures, CMAR has discovered that the VR2AR temperature sensors typically record 0.5 – 1 °C lower than other temperature sensors. This is not corrected for or flagged in the datasets but may be in the future. - Sensor drift is not flagged in the datasets. - The sensor_depth_at_low_tide_m is an estimate and should be compared to sensor_depth_measured_m when possible. Note the mooring can get “knocked down” by currents or sink from biofouling. Large discrepancies between the estimated depth and the minimum recorded depth are flagged in the column depth_crosscheck_flag. The Coastal Monitoring Program Water Quality data is organized by county. These datasets are very large, typically exceeding the number of rows that can be viewed in Excel. CMAR recommends filtering the data to the waterbody, station, depth, quality control flag, and/or time period of interest before exporting. Take care when exporting data filtered on quality control columns, because the whole row will be filtered (i.e., all other variables measured at that timestamp will also be excluded). If you have accessed any Coastal Monitoring Program data, CMAR would appreciate your feedback: https://forms.gle/AyD7Vi3BpKGe6ueYA. Please acknowledge the Centre for Marine Applied Research in any published material that uses this data. Contact info@cmar.ca for more information.
Dates and times are in UTC

Column information

waterbody
Data type: text
Waterbody in which the station for this deployment is located

station	
Data type: text
Name of the location for this deployment. Deployments at the same station must be within 500 m of defined station coordinates.

coordinates
Format: Degrees minutes seconds
Latitude and longitude of the deployment

deployment range
Data type: text
String describing the instrument deployment and retrieval dates. The format is "YYYY-MMM-DD to YYYY-MMM-DD"

string_configuration
Data type: text
Configuration in which the sensors were deployed. This can be one of six entries: “sub-surface buoy”, “surface buoy”, “attached to gear”, “attached to fixed structure”, “floating dock”, or “unknown”

sensor_type	
Data type: text
Model of the sensor that recorded the measurement

sensor_serial_number
Data type: text	
Unique identifying number for the sensor that recorded the measurement

year
Data type: number

month
Data type: number

day
Data type: number

hour
Data type: number

minute
Data type: number

seconds
Data type: number

depth
Data type: number
Units: metres	
Estimated depth of the sensor at low tide, in metres, based on its position in the sensor string configuration

dissolved oxygen
Data type: number
Units: % saturation
Dissolved oxygen measurement, in units of percent saturation

temperature
Data type: number
Units: F	
Sea water temperature measurement, in degrees Fahrenheit