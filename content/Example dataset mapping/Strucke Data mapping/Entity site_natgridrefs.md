---
Entity_Name: site_natgridrefs
Type: Data (Derived)
Public_ID: "[[site_natgridref_id]]"
SEAD_table: "[[tbl_sites]]"
status: in progress
publish: true
---
> [!to do] The relevant columns for this dataset relating to site in national grid coordinates are:
> - **northing_3006** 
> - **easting_3006**


> [!warning]  the tbl_site_natgridrefs table in SEAD is currently empty. 
> However, it looks like an appropriate place to record the given northering and easting values in this dataset


- [ ] talk to Phil about this table, and if we want to use it for these columns, or if he has a better solution
- [x] create a data-derived entity site_natgridrefs with columns `northing_3006` and `easting_3006`
- [x] drop duplicates on `northing_3006`
- [ ] add to it a column for `method_id` and figure out which one is appropriate for this data set
- [ ] link this entity to [[Example dataset mapping/Strucke Data mapping/Entity site|Entity site]]


| method_id | method_name              | description                                                                                                                                                                                                                                                                                 |
| --------- | ------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| 69        | Swedish RT90'[2.5 gon V] | Swedish Rikets Nät (National Grid) system. Full name "RT 90 2.5 gon V 0:-15". X = south-north, Y = west-east. Essentially superceded by SWEREF 99 although still in extensive use.See http://www.lantmateriet.se/templates/LMV_Page.aspx?id=4766&lang=EN (NOTE: include URL as biblio link) |
| 70        | SWEREF 99 TM (Swedish)   | Swedish geodetic reference system, based on UTM zone 33N bit extended to include the whole of Sweden. Coordinates are generally with decimeters of WGS 84 coordinates for the same place. See http://www.lantmateriet.se/templates/LMV_Page.aspx?id=4219                                    |
| 71        | SWEREF 99 dd mm          | Swedish geodetic reference system for local coordinates (where dd mm are replaced by the appropriate zone meridian.NOTE: exactly how we handle the specific zones yet to be discussed - maybe one method entry per zone?                                                                    |
| 72        | WGS84                    | World Geodetic System.System is used by the Global Positioning System.                                                                                                                                                                                                                      |
| 73        | Local project grid       | Any coordinate or grid system established for local recording of objects. Includes abstract archaeological site grids with origin (0,0) at any location.I available, conversion factors for alignment wiwth standard reference systesm should be given in site notes.                       |
| 102       | Rikets höjdsystem 1970   | Rikets höjdsystem 1970. Swedish national altitude system 1970.                                                                                                                                                                                                                              |
| 103       | RT90 5 gon V             | Rikets koordinatsystem RT90 5 gon V                                                                                                                                                                                                                                                         |
| 105       | Local or unknown grid    | Site-specific grid or unknown site or sampling grid or coordinate system.                                                                                                                                                                                                                   |
| 114       | WGS84 UTM zone 32        | Global coordinate system zone UTM 32 in WGS84 system. Last Revised: June 2, 1995 Area: World - N hemisphere - 6°E to 12°E - by country                                                                                                                                                      |
| 120       | WGS84 UTM zone 33N       | WGS84 UTM zone 33N                                                                                                                                                                                                                                                                          |
| 121       | Rikets höjdsystem 1900   | \nKorrektioner: Ingen landhöjnings- eller tidjordskorrektion                                                                                                                                                                                                                                |


![[schema site national grid.png|]]


# YAML as of 2026-08-25
````
name: site_natgridrefs
type: entity
system_id: system_id
keys: []
columns:
  - fid
  - northing_3006
  - easting_3006
public_id: site_natgridref_id
source: datasheet_v9
drop_empty_rows:
  - northing_3006

```