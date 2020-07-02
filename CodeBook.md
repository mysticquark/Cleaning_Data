The run_analysis.R script performs the data preparation and then followed by the 5 steps required as described in the course project’s definition.

Assign each data to variables:
features:List of all features.
activities:
subject_test:
x_test:
y_test:
subject_train:
x_train:
y_train:


Merges the training and the test sets to create one data set
X:Merge x_train and x_test
Y:Merge y_train and y_test
Subject: Merge subject_train and subject_test 
Merged_Data: Use cbind to merge X,Y and Subject

Extracts only the measurements on the mean and standard deviation for each measurement
TidyData:Subsetting Merged_Data, selecting only columns: subject, code and the measurements on the mean and standard deviation (std) for each measurement.

Uses descriptive activity names to name the activities in the data set
Entire numbers in code column of the TidyData replaced with corresponding activity taken from second column of the activities variable

Appropriately labels the data set with descriptive variable names
Code column in TidyData renamed into Activities
All Acc in column’s name replaced by Accelerometer
All Gyro in column’s name replaced by Gyroscope
All BodyBody in column’s name replaced by Body
All Mag in column’s name replaced by Magnitude
All start with character f in column’s name replaced by Frequency
All start with character t in column’s name replaced by Time

From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject
FinalData:Sumarizing TidyData by taking the means of each variable for each activity and each subject, after grouped by subject and activity.
Export FinalData into FinalData.txt file.
