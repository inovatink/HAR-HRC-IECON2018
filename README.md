# Task-Based Control and Human Activity Recognition for Human-Robot Collaboration

In order to evaluate the performance of the developed classifier algorithm for HAR in human-robot collaboration scenario, publicly available Skoda mini checkpoint data set was used [1]. This dataset contains the data of 10 activities of assembly-line worker in a car production environment. The activities together with unlabeled activity and corresponding classes are given in Table 1. The activities were performed at the quality assurance checkpoint of the automobile production plant.

In the considered dataset ten sensor nodes were placed on the right arm and other nine sensor nodes were placed on the left arm during the data collection. Throughout the experiment assembly worker performed each activity given in Table 1, except for unlabeled, for 19 times. Unlabeled activities are activities performed during assembly other than 10 labeled activities.

The dataset at hand contains calibrated tri-axial accelerometer signals collected at 64 Hz. In the *data preprocessing* stage, accelerometer signals were filtered using low-pass filter with cut-off frequency of 20 Hz to remove the noise. Data was segmented into 1 s (N=64) windows with 50% (N=32) overlap. In the *feature extraction* step, statistical and nonlinear features were calculated from for each 1 s segment. Extracted features used in training are following: *maximum, minimum, RMS, variance, mean absolute deviation, 25th percentile, 75th percentile, median, mean, skewness, Hjorth mobility, Hjorth complexity and mean cross rate*. Each of the features are calculated for data from each axis of each sensor for given sliding window. Formed learning datasets for left arm, right arm and for both arm combined are made publicly available in this repository. Software program for training and validation of ANNs was written in Python language in Jupyter notebook. All of the necessary materials to repeat the training and validation can be also found in this repository.

| Class      |           Activity           |
|:----------:|:----------------------------:|
|  null (32) |           unlabeled          |
|   0 (48)   |       write on notepad       |
|   1 (49)   |           open hood          |
|   2 (50)   |          close hood          |
|   3 (51)   | check gaps on the front door |
|   4 (52)   |     open left front door     |
|   5 (53)   |     close left front door    |
|   6 (54)   |     close both left doors    |
|   7 (55)   |       check trunk gaps       |
|   8 (56)   |     open and close trunk     |
|   9 (57)   |     check steering wheel     |
Table 1. Activities and classes

## References

[1] P. Zappi, C. Lombriser, T. Stiefmeier, E. Farella, D. Roggen, L. Benini,and  G.  Tr ̈oster,  “Activity  recognition  from  on-body  sensors:  accuracy-power  trade-off  by  dynamic  sensor  selection”  in Wireless  sensor  net-works.    Springer, 2008, pp. 17–33. 
