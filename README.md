==================================================================
Getting and Cleaning Data Coursera Peer Assessment
Human Activity Recognition Using Smartphones Dataset
Version 1.0
==================================================================
John Woodbridge
==================================================================

R-code:
run_analysis.R

Required Packages:
- 'reshape'

Purpose:
This code is written to import test and training data, put it into a tidy data
format, before outputting averages on the mean() and std() variables by
activity and subject.

Import files:
- 'features.txt': List of all features.
- 'activity_labels.txt': Links the class labels with their activity name.
- 'train/X_train.txt': Training set.
- 'train/y_train.txt': Training labels.
- 'test/X_test.txt': Test set.
- 'test/y_test.txt': Test labels.
- 'train/subject_train.txt': Each row identifies the subject who performed 
	the activity for each window sample. Its range is from 1 to 30. 
- 'train/subject_test.txt': Each row identifies the subject who performed 
	the activity for each window sample. Its range is from 1 to 30. 

Output files:
- 'ave_data.txt'

Variables:
- X variables are labeled using 'features.txt' list and are not altered further.
- Y variable is labeled as "Activity" and converted from a number to a 
  description using 'activity_labels.txt'.
- Subject numbers are labeled as "Subject" variable from 'subject_t***.txt' file.

Operation:
1. Copy "run_analysis.R" file to working directory.
2. Add the following files to working directory:
- 'features.txt'
- 'activity_labels.txt'
3. Add the following folders to working directory:
- 'train' containing X_train.txt, y_train.txt and subject_train.txt.
- 'test' containing X_test.txt, y_test.txt and subject_test.txt.
4. run command: 'source("run_analysis.R")' from R console.

Assumptions:
1. Only mean() and std() variables are required in the tidy dataset.
2. Output of averages of data are by activity and subject resulting in
   a record for each combination of activity and subject. E.g. Subject 1
   would show a result for each of the six activities, Subject 2 would
   show six activities, and so on where data is available.
3. Where no data is available for an activity/subject combination no record
   is present in the dataset.
4. Feature labels are considered to be adequate descriptions of variables
   for the purpose of this exercise. Explanation of descriptions can be found
   in features_info.txt.
   
