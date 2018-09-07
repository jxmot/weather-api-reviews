# NOAA FAILURE LOG

This file contains a log of failures, as described in the review : [noaa-20180828-jxmot.md](noaa-20180828-jxmot.md)

Please note that there has been **many** failures that have occurred before the first log entry. The log entries are the result of :

* Visually recognizing there is an issue. 
* Analysis of -
    * Application log files
    * Responses obtained with Postman
    
## Log

Listed new to old (*all times are CST*): 

* 2018-09-06 - For a period of time the KORD observation data contained erroneous or NULL data
* 2018-09-01 through 2018-09-05 - KORD observation data has been consistently behind by 4 to 6 hours
* 2018-09-01 @ 23:54:29 - KORD observation was retrieved, observation time stamp was - 1535822700000(Saturday, September 1, 2018 12:25:00 PM)
* 2018-09-01 @ 07:24:29 - KORD observation was retrieved, observation time stamp was - 1535784660000(Saturday, September 1, 2018 1:51:00 AM)
* 2018-08-31 @ 22:24:28 - KORD observation was updated again, observation time stamp was - 1535755860000(Friday, August 31, 2018 5:51:00 PM)
* 2018-08-31 @ 20:54:28 - KORD observation was finally updated, observation time stamp was - 1535752260000(Friday, August 31, 2018 4:51:00 PM)
* 2018-08-31 @ 19:33:00 - KORD observation has not updated since 08-30.
* 2018-08-31 @ 14:18:00 - KORD forecast contains erroneous information.
    * https://api.weather.gov/gridpoints/LOT/65,76/forecast
        * Forecast at - Friday, August 31, 2018 2:17:41 PM
        * "Partly sunny, with a high near 85. Heat index values as high as **9.96921E+36**. South wind around 10 mph, with gusts as high as 20 mph. New rainfall amounts **in excess of 4 inches possible**."
            * Time period name -  "This Afternoon"
            * Info - The temperature is **way** off, and the rain forecast in incorrect.
* 2018-08-31 @ 16:45:00 - KORD observation has not updated since 08-30.
* 2018-08-30 @ 10:51:00 - KORD observation stopped updating.
    *  https://api.weather.gov/stations/KORD/observations/current
    
## Notes

* Endpoints are accessed using Postman and a Node application.
* Access frequency of the Node application is > 1 hour between requests for forecasts and observations. And forecast requests occur approximately 5 to 20 minutes after the observations request.
* Application results verified with Postman.


