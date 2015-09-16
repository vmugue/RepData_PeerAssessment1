# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data
```r
## reading file 
tryCatch(
    unzip("activity.zip", overwrite = FALSE, exdir = "figure"), 
    warning = function(w) "file already exists")
initActiv <- read.csv("figure/activity.csv")    

## adding new useful dimensions ##
initActiv$hour <- floor(initActiv$interval / 60)
initActiv$minute <- initActiv$interval - initActiv$hour*60
initActiv$datetime <- as.POSIXlt(
    paste(initActiv$date, initActiv$hour, initActiv$minute, sep = " "), 
    format = "%Y-%m-%d %H %M")    
```
## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
