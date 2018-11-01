Below are the data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Here are the raw data for the project: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

In this project we have retrieved the above raw data into R, cleaned it and created an independent tidy data set with the average of each variable for each activity and each subject.
# The repository contains the following files:
README.md : provides an overview of the data set and how it was created
run_analysis.txt : the final tidy data set
run_analysis.R : the R script used to modify raw data to tidy data
CodeBook.md : the code book, containing information about all the variables and summaries calculated
# Procedure for creating tidy data set:
Run the script run_analysis.R, which retrieves source data set and processes it to generate final tidy data set. Below are the step by step procedure to perform the same:

Load the necessary libraries i.e dplyr, readr, reshape2
Read the data and convert them to data frames
Merge subject, activity details and measurements of only mean and standard deviation into test and train data sets
Merge test and train data sets
Make the column names more descriptive
Create a second, independent tidy set with the average of each variable for each activity and each subject
Write modified data set into text file: run_analysis.txt
# Background of the source data set:
The source data set that this project was based on was obtained from the Human Activity Recognition Using Smartphones Data Set, which describes how the data was initially collected as follows:

The experiments have been carried out with a group of 30 volunteers within an age bracket of 19-48 years. Each person performed six activities (WALKING, WALKING_UPSTAIRS, WALKING_DOWNSTAIRS, SITTING, STANDING, LAYING) wearing a smartphone (Samsung Galaxy S II) on the waist. Using its embedded accelerometer and gyroscope, we captured 3-axial linear acceleration and 3-axial angular velocity at a constant rate of 50Hz. The experiments have been video-recorded to label the data manually. The obtained dataset has been randomly partitioned into two sets, where 70% of the volunteers was selected for generating the training data and 30% the test data.

The sensor signals (accelerometer and gyroscope) were pre-processed by applying noise filters and then sampled in fixed-width sliding windows of 2.56 sec and 50% overlap (128 readings/window). The sensor acceleration signal, which has gravitational and body motion components, was separated using a Butterworth low-pass filter into body acceleration and gravity. The gravitational force is assumed to have only low frequency components, therefore a filter with 0.3 Hz cutoff frequency was used. From each window, a vector of features was obtained by calculating variables from the time and frequency domain.
