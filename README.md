# Data-Cleaning-Coursera-Project-Python
The goal of this project was to take obtain the dataset located [here](https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip), from this [source](http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones), and combines all the information from all the files and transforms the data into one clean-data-file, which has all the columns with descriptive names, and performs analysis on cleaned data. The zip file comes in with two files (feature.txt and activity_labels.txt ) and two folders (train and test).

1. The `"feature.txt"` file- contains all the information on features/measurements.
2. The `"activity_labels.txt"` file- consist of all the name of the activities corresponding to numbers (0-6). 
3. The train data consists of the following files.\
    a. `"subject_train.txt"` file- it has all the subjects with subject-Id (0-30) who performed the activities for the   
         measurements\
    b. `"y_train.txt"` file-It consists of all the activities in the form of numbers (0-6) performed by the subjects.\
    c. `"X_train.txt"` file- It consists of measurements of variable/features for each activity performed by each subject
4. The test data consists of the following files.\
    a. `"subject_test.txt"` file- it has all the subjects (0-30) who performed the activities for the measurements\
    b. `"y_test.txt"` file-It consists of all the activities in the form of numbers (0-6) performed by the subjects.\
    c. `"X_test.txt"` file- It consists of measurements of variable/features for each activity performed by each subject.

 ### The script "run_analysis" performs the following analysis       
 1. Read in the test data, train data, and files, with pandas "read_csv" function.
 2. Combine all the train data along horizonal axis to create  "df_train" dataframe.
 3. Combine all the test data along horizonal axis to create  "df_test" dataframe
 4. Merges the train and test dataframes along vertical axis to create one data set ("df).
 5. Appropriately labels the data set with descriptive variable names
 7. Extracts subset of data "df1" that only consists of mean and standard deviations measuremnts variables.
 8. Format the varibales names to easily understandable format by removing special characrters such as "/,(),_".
 9. Creates data set("df2") which consists of mean for each varibale for each actvity and each subject.  
 10. Writes and saves "df2" as "tidy_data" in text format.
