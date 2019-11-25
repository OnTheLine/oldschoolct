# otl-oldschoolct
interactive map demo of OldSchoolCT photos by Johanna Kaplan

## Notes

All photos of one-room Connecticut schoolhouses copyrighted by Johanna Kaplan, and publicly viewable on her Instagram
https://www.instagram.com/oldschoolct/

This python tool downloads Instagram images and metadata
https://instaloader.github.io/

- filename
- caption (example: Clarence R. O’Crowley Schoolhouse, Coventry. Built in ……)
- comments (if any)
- geotag or EXIF data (if it exists, to plot location)

Ilya: See the combined .csv list with data.
- Column 1 is the “post” name.
- Column 2 is the link to the photo. Note that two post have two photos (“gallery” in instagram terms), so there are 230 posts and 232 photos.
- Column 3 is the Caption with tags.
- Column 4 is my attempt to determine the name of the school and the town where it is in — I noticed that most captions start with one sentence of the form “School name, Town”.
- Columns 5 and 6 are the coordinates for the "attempted school name” (column 4) with Google geo coder. Note that I did not clean any of the data and you should go through and fix them manually (eg the very last row has a period in the school name, so I didn’t properly cut the sentence and hence geocoding is most likely wrong).




I just realized I re-ran the script and did not account for the 2 “gallery” posts that I mentioned (posts that are associated with 2 images):

2019-04-08_09-45-59_UTC.txt should refer to:
2019-04-08_09-45-59_UTC_1.jpg
2019-04-08_09-45-59_UTC_2.jpg

2019-01-28_16-51-52_UTC.txt should refer to:
2019-01-28_16-51-52_UTC_1.jpg
2019-01-28_16-51-52_UTC_2.jpg
