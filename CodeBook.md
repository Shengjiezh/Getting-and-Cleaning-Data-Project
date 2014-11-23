Introduction:
=========================

The script run_analysis.R performs the 5 steps transformation to the data set:
 
1. Merges the training and the test sets to create one data set.
2. Extracts only the measurements on the mean and standard deviation for each measurement. 
3. Uses descriptive activity names to name the activities in the data set
4. Appropriately labels the data set with descriptive variable names. 
5. From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.


Data Set:
============================

The data provided by the course represent data collected from the accelerometers from the Samsung Galaxy S smartphone. A full description is available at the site where the data was obtained: 

http://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones


Variables:
============================

1. x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files;
2. x_data, y_data and subject_data merge the previous datasets to further analysis;
3. features contains the correct names for the x_data dataset, which are applied to the column names stored in mean_and_std_features, a numeric vector used to extract the desired data;
4. A similar approach is taken with activity names through the activities variable;
5. all_data merges x_data, y_data and subject_data in a big dataset;
6. Finally, averages_data contains the relevant averages which will be later stored in a .txt file. ddply() from the plyr package is used to apply colMeans() and ease the development.
