# Getting-and-Cleaning-Data
# run_analysis.R
-->It is the main script of the repository. 

In order to produce the 'tidy_data_summary' table, the script 'run_analysis.R' was created and used. It performs the following tasks:

Merges the training and the test sets to create one data set with target variables.
Binds these files:
UCI HAR Dataset/train/subject_train.txt
UCI HAR Dataset/train/X_train.txt
UCI HAR Dataset/train/y_train.txt
from the train set by columns to a table that contains, the human subject, the activity performed and the values of the features.

Binds these files:
UCI HAR Dataset/test/subject_test.txt
UCI HAR Dataset/test/X_test.txt
UCI HAR Dataset/test/y_test.txt
from the test set by columns to a table that contains, the human subject, the activity performed and the values of the features.

Binds the data frames created for test and train set into one large dataset by rows.

Extracts only the measurements on the mean and standard deviation for each measurement.
Finds the target features, which are the features with measurements about mean and standard deviation, and extracts them as well as those that indicate the 'subject' and 'activity' and creates a new data table only with the target variables.
Uses descriptive activity names to name the activities in the data set.
Replace the variable about activity, that contains integers from 1 to 6, with a factor based on levels and labels contained in the 'activity_labels' data file.
Appropriately labels the data set with target variables with descriptive names.
Extracts the target variable names from 'features.txt'.
Corrects a typo that exists in some feature names, that is to replace 'BodyBody' that appears in the names of some features with just 'Body'.
Creates a new tidy dataset with the appropriate labels for the variable names.
From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.
Group the tidy data table created in step 4, by 'subject' and 'activity'.
Summarize each variable to find the average for the grouped values.
Ungroup the data table.
Add descriptive names to the variables of the new tidy data table, by adding the prefix 'Avrg-' in the names of the target feature averages.
Write the data in a text file in the present working directory, by the command: write.table(tidy_data_summary, "tidy_data_summary.txt", row.names = FALSE) 
