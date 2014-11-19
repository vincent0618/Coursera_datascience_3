README
------

#### This file describes how run_analysis.R script works.

**Source dataset**: https://d396qusza40orc.cloudfront.net/getdata%2Fprojectfiles%2FUCI%20HAR%20Dataset.zip.
 
 **run_analysis.R can do the following:**
>* Merges the training and the test sets to create one data set.
>* Extracts only the measurements on the mean and standard deviation for each measurement. 
>* Uses descriptive activity names to name the activities in the data set
>* Appropriately labels the data set with descriptive variable names. 
>* From the data set in step 4, creates a second, independent tidy data set with the average of each variable for each activity and each subject.

-----
###Steps
* First, unzip the data and rename the folder with "data". Make sure the folder "data" and the run_analysis.R script are both in the current working directory.
* Second, use source("run_analysis.R") command in RStudio.
* Third, you will find two output files are generated in the current working directory:
     * merged_data.txt (7.9 Mb): it contains a data frame called cleanedData with 10299*68 dimension.
     * data_with_means.txt (220 Kb): it contains a data frame called result with 180*68 dimension.
* Finally, use data <- read.table("data_with_means.txt") command in RStudio to read the file. Since we are required to get the average of each variable for each activity and each subject, and there are 6 activities in total and 30 subjects in total, we have 180 rows with all combinations for each of the 66 features.



