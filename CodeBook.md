# CodeBook

## Input Data

The data is loaded from the original UCI dataset ZIP and is assumed to be in the `./UCI HAR Dataset/` folder. See the [README.md](README.md) for further details on this.

## Variables and Output Data

For each observation in the dataset, each measurement that contains either _mean_ or _std_ in the feature name was extracted and its average calculated.  There is an `x`, `y` and `z` value for each of the main measurement types.

For example, the main type of tBodyAcc will have the following measurements extracted:

* tBodyAcc-mean()-X
* tBodyAcc-mean()-Y
* tBodyAcc-mean()-Z
* tBodyAcc-std()-X
* tBodyAcc-std()-Y
* tBodyAcc-std()-Z

This same pattern was applied to these main types:

* tBodyAcc
* tGravityAcc
* tBodyAccJerk
* tBodyGyro
* tBodyGyroJerk
* tBodyAccMag
* tBodyAccJerkMag
* tBodyGyroMag
* tBodyGyroJerkMag
* fBodyAcc
* fBodyAccJerk
* fBodyGyro
* fBodyAccMag
* fBodyBodyAccJerkMag
* fBodyBodyGyroMag
* fBodyBodyGyroJerkMag.

For a fuller description of each, please see the information and discussion in `./UCI HAR Dataset/features_info.txt`. 

## Transformations

The script, `run_analysis.R`, does the following,

* **Loads** the various files which make-up the UCI dataset.
* **Merges** the three `test` and three `train` files into a single data table.
* **Creates** a smaller dataset containing only the `mean` and `std` measurements for the observations.
* **Sets** descriptive labels for the measurements as contained in `./UCI HAR Dataset/activity_labels.txt`.
* **Computes** the `mean` of each measurement in the second tidy dataset, grouping by subject/activity.
* **Saves** this tidy dataset to `./FinalData.txt`.
