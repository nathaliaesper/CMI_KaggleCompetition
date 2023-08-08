# CMI Kaggle Competition Scripts

----

This repository contain all the scripts we used to organize CMI's actigraphy data to the Kaggle competition that we hosted.

----

To organize the data, run the scripts in the folowwing order:

1. **organize_files.ipynb**

   |-> it will organize the "data_cleaning" files from all raters into one single file

   |-> it will organize the "sleep_log" files from all raters into one single file

   |-> it will copy the csv files to a different folder

**2. You will need to manually edit the "data_cleaning" and "sleep_log" files to delete duplicated entries. This can be done using Excel (too lazy to think about this in Python)**

**3. change_timestamp.ipynb**

   |-> it will read the subject raw csv file and change the timestamp - PHI

**4. add_date_sleeplog.ipynb**

   |-> it will read the "sleeplog" and the subject raw data file to add the date to the "sleeplog" file

**5. correct_dates.ipynb**

   |-> it will read the "sleeplog" created on step 4 and it will correct the wrong dates (for some unknown reason, for me, my "add_date_sleeplog" script is getting the wrong date in some days; mainly the days in which the participant went to bed after midnight)

**6. change_annotation_invalid_nights.ipynb**

   |-> it will read the "sleeplog" file from step 5 and the "data_cleaning" file from step 2 and will change the time of the invalid nights (annotated by the raters) to '03:00:00'

