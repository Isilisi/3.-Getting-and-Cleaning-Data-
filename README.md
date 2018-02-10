### overview

This is the final project of the third course, "Getting and Cleaning Data", of the coursera "Data Science specialisation".

The purpose of this project is to practice data-cleaning.

### files description

The original data is in "UCI HAR Dataset" folder. The folder can also be downloaded here: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

A full description is available at the site where the data was obtained: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

The full analysis script lies in "run_analysis.R". The analysis consists of five steps:

1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement.
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names.
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

The clean data set from step 5 is "tidy_data.txt". After downloading or reproducing, it can be read in as, for example:
``` {r}
tidy_data <- read.table(file.path(".", "tidy_data.txt"))
tidy_data <- tidy_data[,-1]
colnames(tidy_data) <- c("id", "activity", "feature_name", "mean", "std")
```

For more information on variables and analysis steps see "code_book.md"

### for coursera markers

Please give a thorough feedback.