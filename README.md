Below are the data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained: http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones

Here are the raw data for the project: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip

In this project we have retrieved the above raw data into R, cleaned it and created an independent tidy data set with the average of each variable for each activity and each subject.
#The repository contains the following files:
README.md : provides an overview of the data set and how it was created
run_analysis.txt : the final tidy data set
run_analysis.R : the R script used to modify raw data to tidy data
CodeBook.md : the code book, containing information about all the variables and summaries calculated
#Procedure for creating tidy data set:
Run the script run_analysis.R, which retrieves source data set and processes it to generate final tidy data set. Below are the step by step procedure to perform the same:

Load the necessary libraries i.e dplyr, readr, reshape2
Read the data and convert them to data frames
Merge subject, activity details and measurements of only mean and standard deviation into test and train data sets
Merge test and train data sets
Make the column names more descriptive
Create a second, independent tidy set with the average of each variable for each activity and each subject
Write modified data set into text file: run_analysis.txt
