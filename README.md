## Getting and Cleaning Data Course Assignment

This is a repository for the course project of the Coursera online course `Getting and Cleaning Data` (Johns Hopkins University).

The R code is for creating a new tidy data set with the average of selected variables for each activity and each subject from the raw data.

There is one self contained script named `run_analysis.R`.  It:

* Processes the UCI `Human Activity Recognition Using Smartphones Data Set` that can be downloaded at https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip
* Expects the unzipped data files to to be in the `./UCI HAR Dataset/` folder of the main working folder.
* Transforms the data and outputs variables as described in the [CodeBook.md](CodeBook.md)
* Outputs a tidy dataset to '`./FinalData.txt`'


