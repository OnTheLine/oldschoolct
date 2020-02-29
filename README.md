# otl-oldschoolct
Interactive map of OldSchoolCT photos by Johnna Kaplan. View online at https://ontheline.gitub.io/otl-oldschoolct

Embedded in On The Line book http://ontheline.trincoll.edu

![Map demo screenshot](otl-oldschools-demo.jpg)

## Credits
- All photos of one-room Connecticut schoolhouses copyrighted by Johnna Kaplan, and publicly viewable on her Instagram
https://www.instagram.com/oldschoolct/
- Coding and map design by Ilya Ilyankou and Jack Dougherty
- Python tool to download Instagram images and metadata https://instaloader.github.io/
- Many thanks to Elizabeth Rose for researching school site addresses to improve geographic precision

## Jupyter processing
See the notebook for processing steps (including download). All photos are saved in `photos/` folder, and all metadata is saved in the `catalog.csv` file. The thumbnails (smaller images that are shown on the map, in other words icons) are created with Wand library (http://docs.wand-py.org/en/0.5.7/) and are saved in `photos/thumbnails/`.

1. `Title` column is generated from the caption. It is assumed that a first sentence of the caption contains the school name and/or location (eg `Old Center School, Burlington`).
1. Based on that assumption, `Geocoded` column contains geocoded coordinates of what Google API thinks is an appropriate location for that school name and location.
1. `Latitude` and `Longitude` columns are derived from the `Geocoded` column.

## Catalog-refined
- Created duplicate of `catalog.csv` called `catalog-refined.csv` to research school site addresses, and manually improve precision of geographic coordinate data without overwriting python download.
- Keep all rows intact to match with original. Omit selected rows (e.g. secondary photos of school interiors, historical signs) from map display by removing Lat and Long

## TODO
- Ask photographer to review missing address data in [catalog-refined Google Sheet](https://docs.google.com/spreadsheets/d/1JouNnQTA6FGgCJbVaVoIBKxddhGuO999ecHIMOYfi-Y)
- Improve workflow with photographer to add new photos with EXIF geocoordinate data
