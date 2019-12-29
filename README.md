# Introduction

Below you can see my work from Google Code in `Reading and Writing CSV data - R Project for Statistical Computing`. I have described my code with comments

# Prerequisites

- R
- RStudio
- Jsonlite
- Curl

# Code Description
The code below can be copied to R and executed as is.

```
#Use the simple Cranlogs API to obtain half-yearly R package downloads summaries in 2018

library('jsonlite')
library('curl')


#The task is to obtain the total downloads of all R packages in 2018, half-yearly and save the results in a single CSV file

stat_firsthalf = jsonlite:: fromJSON("https://cranlogs.r-pkg.org/downloads/total/2018-01-01:2018-06-30")
stat_secondhalf = jsonlite:: fromJSON("https://cranlogs.r-pkg.org/downloads/total/2018-07-01:2018-12-31")

stat_fullyear = rbind(stat_firsthalf,stat_secondhalf )

write.csv(stat_fullyear, "C:\\Users\\srish\\Desktop\\stat_fullyear.csv")

```

# Screen Record
![Screen Recording]()

# Authors
- Srishti Jain
