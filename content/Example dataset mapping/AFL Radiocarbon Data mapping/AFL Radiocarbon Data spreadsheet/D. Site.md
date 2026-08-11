---
best_matched_column: "[[site_name]]"
aliases:
  - D.
date created: Friday, September 26th 2025, 12:46:49 pm
example_data:
  - Neustadt LA 156
  - Hemmor
  - Trørød
publish: true
---
> [!info] The Site column 
> Contains the names of the archaeological sites which contributed samples to the project. 
>  Therefore, it is a good match for [[site_name]], which is a part of [[tbl_sites]]. 

![[Radiocarbon data column D.png]]
# sites
 - [ ] create and fill in a sheet called **sites** in the [radiocarbon_Glykou_etal_2021_input.xlsx spreadsheet]([radiocarbon_Glykou_etal_2021_input.xlsx](https://umeauniversity.sharepoint.com/:x:/r/sites/SEAD72/Shared%20Documents/Task%20force%20-%20System%20analysis%20of%20radiocarbon%20data/Datasets/AFL/input-data/radiocarbon_Glykou_etal_2021_input.xlsx?d=w34fa6e11a37c4afe9398f92ea68bd11c&csf=1&web=1&e=LaDqOd)) with the following columns
 - **system_id** This column is filled incrementally, starting with 1 and is used during the import process to keep track of the data in this sheet, and to cross-reference its connections to the other sheets.
 - **altitude** *This data set has no altitude information, so this column is left blank*
 - **[[latitude_dd]]** 
 - **[[longitude_dd]]**
 - **[[national_site_identifier]]**(fill this in for those sites in the dataset that happen to have one)
 - **[[site_description]]**(fill this information in from the references provided, or ask the dataset provider to provide them)
 - **[[site_name]]** (copy one example of each name appearing in column D of the **a1_radiocarbon_data** sheet)
 - **site_preservation_status_id** *This data set has no site preservation status information, so this column is left blank*
 - **[[site_location_accuracy]]** fill this in based on how accurate the  [[latitude_dd]] and [[longitude_dd]] information is
 - **[[site_id]]** fill this in for any sites that already exist in SEAD, using the [[site_id]] number on record.
# locations
  
 > [!info] all sites have a location--they are located in a country, and perhaps part of a province, county, town, or parish, therefore we also need to:
 
 - [ ] create a sheet called **locations** which contains the following columns 
 
- **system_id** This column is filled incrementally, starting with 1 and is used during the import process to keep track of the data in this sheet, and to cross-reference its connections to the other sheets.
 - **[[location_name]]** Fill in all of the location names associated with the above sites. If a dataset is missing this information, one can open the site coordinates in GoogleMaps, and obtain the country +/- a local place name there.
 - **[[location_type_id]]** (see list of the various types of locations in the lookup table [[tbl_location_types]])
  - **default_lat_dd** This column could be used to define a central point for each of the locations. However, to date these columns have never been used for any of SEAD's data set, so it is ok to leave it blank
  - **default_long_dd** This column could be used to define a central point for each of the locations. However, to date these columns have never been used for any of SEAD's data set, so it is ok to leave it blank
 - **[[location_id]]**  fill this in for any locations associated with this dataset that already exist in SEAD, using the [[location_id]] number on record.
# site locations
> [!info] once the above two sheets are complete it is time to link them (the "relational" part of the database)

  - [ ] create a sheet called **site locations** which contains the following columns from [[tbl_site_locations]]
  
  - **system_id** This column is filled incrementally, starting with 1 and is used during the import process to keep track of the data in this sheet, and to cross-reference its connections to the other sheets.
  - **[[site_id]]** copy this information from the **system_id** numbers of the **sites** sheet (even if a given site already has a SEAD [[site_id]]). (*If it helps to keep track of which ones have been done, you can also add a column to show the corresponding **site_name** on this sheet, but it is not needed for the import process, this column is enough to connect the information for the relational part of the database.*)
   - **location_id** copy this information from the **system_id** numbers of the **locations** sheet (even if a given location already has a SEAD [[site_id]]). (*If it helps to keep track of which ones have been done, you can also add a column to show the corresponding **location_name** on this sheet, but it is not needed for the import process, this column is enough to connect the information for the relational part of the database.*)
   - **[[site_location_id]]** Given that all locations that already exist in SEAD had their [[site_location_id]] identified in the **locations** sheet, it is ok to leave this column blank (and I am not certain why it is in this sheet)
 



