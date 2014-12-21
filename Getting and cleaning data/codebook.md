Introduction
Script run_analysis.R performs  5 steps listed in the course project's definition.

First, all  similar data is vertically merged  using  rbind() function. By similar, we mean those files having the same number of 
columns and referring to the same entities.Then, only those columns with the mean and standard deviation measures are taken from the whole dataset using grep() 
and names have been assigned using features.txt.
As activity data have values 1-6, we take the activity names and IDs from activity_labels.txt and they are substituted in the dataset.
Finally, we generate a new dataset with all the average measures for each subject 
and activity (30*6=180 rows). The output file is called averages_data.txt, and uploaded to this repository.


Variables
x_train, y_train, x_test, y_test, subject_train and subject_test contain the data from the downloaded files.
x_data, y_data and subject_data merge the previous datasets to further analysis.
feat contains the correct names for the x_data dataset, which are applied to the column names stored in mean_and_std_features,
a numeric vector used to extract the desired data into data variable.
A similar approach is taken with activity names and new variable y is created with desired activity names.
all_data merges data, y and subject_data in a big dataset.
Finally, averages_data contains the relevant averages calculated using aggregate() function are later stored in a .txt file. 
