# NOAA FAILURE LOG

This file contains a log of failures, as described in the review : [noaa-20180828-jxmot.md](noaa-20180828-jxmot.md)

Please note that there has been **many** failures that have occurred before the first log entry.

## Log

Listed new to old (*all times are CST*): 

* 2018-08-31 @ 22:24:28 - KORD observation was updated again, observation time stamp was - 1535755860000( Friday, August 31, 2018 5:51:00 PM)
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
* Access frequency of the Node application is > 1 hour between requests for forecasts and observations. And forecasts occur approximately 5 to 20 minutes after the observations request.
* Application results verified with Postman.


