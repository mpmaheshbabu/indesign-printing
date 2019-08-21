# Indesign Printing
## InDesign templates and scripts created by the VIRAT Digipress prepress department 

As one of India's best digital print providers, we're used to automating as many tasks as possible. Over the years, we've built up a toolkit of InDesign scripts that have proved useful to us, and now we're going to start sharing them publicly on GitHub.

## Installing and Presets

To install:
1. Clone repo to a local folder.
2. Copy the scripts(.jsx files) to "C:\Program Files\Adobe\Adobe InDesign CC 2019\Scripts\Scripts Panel".
3. Copy templates folder to any local drive/folder.
4. Define print preset `HQsRGB`, open Indesign and navigate to the following 
    `File > Adobe PDF Presets > Define` 
    
## Image Processing

### Example1: To process a double page photobook of size 12"x36" with first and last pages as single pages and rest double pages

Folder structure: `"orderid"\"orderdetails"\"all images go here"`
Sample structure: `20190821001\12x36 NT SILKMATT 20 SHEETS\"all images"`

1. Reaname images to equal number of digits followed by additional details (eg: 01,02,...21). 
2. Open 12x36 template in `photobook-oppodots\double page spread\` folder.
3. Save it to folder in which images are present.
4. Run `image to pdf.jsx` from Scripts Panel.

Output:

Creates csv file.
Adds orderid and orderdetails to left and right TestFrames and checks for overflow.
Maps images to ImageFrame and merges Docoument.
Checks for wrong size images and marks them "TODO".
Gets special sheet details asuming anything as special sheet if filename has more than 3 characters (eg: 10 emboss).
Saves and exports merged Document asynchronously to HQsRGB Preset.
Writes export report to text file and alerts the same.
