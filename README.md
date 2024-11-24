# xls-to-tgt
Python script for creating a Hypack target file from an Excel spreadsheet. 

## Background
A land survey department at work maintains a spreadsheat that has all the tide staff locations for our area of responsibiltiy. The Hydrosurveys department uses the information to create a Hypack target file with all of the tide staff locations. The target file is used by the surveyor on the boat for finding the tide staffs, which are necessary to conduct a hydrographic survey. In the past, tide staffs were entered into the Hypack Tide Editor by hand. This project makes the process more streamlined and reduces input errors. 

The spreadsheet is a working document that gets changed frequently. It consists of three sheets with each sheet representing a different land crew's area of responsibiltiy. Hydrosurvey department needs the tide staff locations from all of the sheets. This script was written in and for a Jupyter notebook. 

## Preparation
In order for the script to work, the spreadsheet must be cleaned up. It has duplicate entries because some tide staffs end up being moved, and the previous row is left, but a strikethough font is used to show the information is outdated. The first thing that needs to be done is to remove any rows that have the strikethrough.
Next, there is an extra column in one of the sheets, and the information is not necessary for our purposes. Remove that column.
Finally, there are some missing dates for when a tide staff was set or last checked. To address this, use a date from a nearby tide staff (at the time of writing this I realize I could import the column without the values).

## Usage
After cleaning up the spreadsheet, modify the file name and location in the script. Also, modify the output directory. The file name is fixed and will be "SWG_Tide_Staff_{Date}.tgt"; with {Date} being the date the script was ran and the output file created. 

Run each cell in order and verify each step by looking over the dateframe which is displahyed after each step.

## Expected Outcome
Upon sucessfully completing all of the steps, the end result will be a file saved in the chosen directory. This target file can then be imported into Hypack to show the cast locations.
  
  An example file will look like: "SWG_Tide_Staffs_20241124.tgt"

