##  Project for Getting and Cleaning Data Course

The purpose of this project is to demonstrate student's ability to collect, work with and
clean a data set. The goal is to prepare a tidy data set, based on the orignal data set
obtained from the following link.

https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip 

A full description of the original data set is available from the following link:

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones 

Step 1:
Downloaded a zip file and put the file in my working directory after unzipping it.
I renamed the data set directory as HAR to simplify the path name.

Step 2:
To read the txt files for training and test sets, read.table() function was used, and to merge
rbind() function. From features.txt file, manually selected the column numbers for the mean and
standard deviation for each measurement. Out of 561 columns, 66 column data were extracted and
combined by using c( ) function. By using matrix() function, the combined data were converted to
a matrix for adding column names. Column names were added by using colnames() function after
slightly changing the original variable names displayed on features.txt file. Renamed the merged
data set as features.

Step 3:
Read and merged the subject and activity data sets by using read.table() and rbind() function.
Merged all data sets (features, subject and activity) into one data set and named it allData.

Step 4:
Created a second, independent tidy data set with the average of each variable for each activity
and each subject by using ddply() function, and named it "finalData" 
For uploading on the assignment box, finalData.txt file was created by using write.table() function.



  






