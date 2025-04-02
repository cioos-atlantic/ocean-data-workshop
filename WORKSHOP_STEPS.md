
# Data Management Workshop Steps

## Resources for group collaboration

Once you have been assigned to a group, there may be a need to share links or notes from your discussion on how to modify the dataset you are working on. Google docs and other resources for collaboration can be accessed on the wiki page:

https://github.com/cioos-atlantic/ocean-data-workshop/wiki/Workshop-Collaboration

## Metadata management steps

Review the [metadata management](METADATA_MANAGEMENT.md) documentation.

Login to the CIOOS metadata form using your Google account. The CIOOS metadata entry form can be accessed here:
[https://cioos-siooc.github.io/metadata-entry-form/#/en/atlantic](https://cioos-siooc.github.io/metadata-entry-form/#/en/atlantic)

If using your own (or a group member's) dataset, fill in the metadata form using the available metadata you have for your data.

If using the [sample Antigonish Sensor String dataset](SAMPLE_DATA.md) go through the steps of adding the metadata included for this dataste into the metadata form.

*Note* Please add an identifier in brackets at the start of the title in the metadata form. For instance:
* If working solo, then for the title, put in "[Sample] Antigonish sensor string dataset ..."
* If part of a group such as 'Group A', then for the title, put in "[Group A] Antigonish sensor string dataset ..."

## Data management steps

Review the [data management](DATA_MANAGEMENT.md) documentation.

Whether you're using your own (or a group member's) dataset, or if you plan to work on the [sample dataset](sample_data/antigonish_sensorstring_data.csv), the steps below will apply.

Make some of the changes and transformations suggested in the data management documentation on your dataset. Consider things like changing the order of variables, how you can standardize the variables and units to either CF and UDUNITS and/or BODC P01 and P06 vocabularies and what those names and units should be, and how and where to record this type of variable and unit metadata. Also consider whether fields such as the latitude and longitude information, and dates etc. are appropriately standardized, and transform the dataset to be more compliant as needed.
