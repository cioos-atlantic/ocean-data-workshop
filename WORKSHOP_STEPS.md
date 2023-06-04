
# Data Management Workshop Steps

## Metadata management steps

Review the [metadata management](METADATA_MANAGEMENT.md) documentation.

Login to the CIOOS metadata form using your Google account. The CIOOS metadata entry form can be accessed here:
[https://cioos-siooc.github.io/metadata-entry-form/#/en/atlantic](https://cioos-siooc.github.io/metadata-entry-form/#/en/atlantic)

If using your own (or a group member's) dataset, fill in the metadata form using the available metadata you have for your data.

If using the Wave Buoy [sample metadata](sample_data/wave_buoy_metadata_sample.yaml), go through the steps of adding the metadata from this file into the metadata form.

## Data management steps

Review the [data management](DATA_MANAGEMENT.md) documentation.

Whether you're using your own (or a group member's) dataset, or if you plan to work on the [sample dataset](sample_data/wave_buoy_raw_data_sample.csv), the steps below will apply.

Make some of the changes and transformations suggested in the data management documentation on your dataset. Consider things like changing the order of variables, how you can standardize the variables and units to either CF and UDUNITS and/or BODC P01 and P06 vocabularies and what those names and units should be, and how and where to record this type of variable and unit metadata. Also consider whether fields such as the latitude and longitude information, and dates etc. are appropriately standardized, and transform the dataset to be more compliant as needed.