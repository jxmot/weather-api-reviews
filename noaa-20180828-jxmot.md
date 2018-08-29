## NOAA

### Links

* API Homepage - <https://forecast-v3.weather.gov/documentation>
    * Documentation - <https://forecast-v3.weather.gov/documentation> <- click the "API Reference" tab
    * Demonstrations - <https://forecast-v3.weather.gov/point/41.9796,-87.9045>

### API Overview

* Costs - This API is free to use, no costs.
* Sign Up - **No, API key is not required**
* Data Formats - GeoJSON, JSON-LD, DWML, OXML, CAP, ATOM
* Update Activity - Difficult to determine
* Support - None
* Version Reviewed - v3

### Review

At first look this API *appears* to be sufficient for most weather data needs. However after testing and examination of the documentation it's clearly an unfinished API. It has a lot of potential to be a really good API but it's doubtful that it will completed in any reasonable amount of time. My guess is that the resources of the NOAA were over taken by its complexity and the scope of the remaining work. 

#### Technical Details

* Platform - Node.JS, [Postman](https://www.getpostman.com/)
* Language(s) used - JavaScript

### Rating
Scoring can range from -5 to +5. The overall score is the summation of the individual scores.

* Scores : 
    * Documentation : **+2**
        * Optional Notes : Although there is *a notable amount* of documentation the failure is that there are no explanations of the terminology. Some terms and endpoint descriptions can be deduced but there are measurable amount of others that can't be. The cause is likely that the documentation has not been completed. Unfortunately you're required to do some searching to locate necessary pieces of information before you can use some of the endpoints. 
    * API Response Quality : **+2**
        * Optional Notes :  The quality is sufficient in the observation and forecast endpoints. Due to the limitations of the documentation other endpoints were not tested, reviewed or used. The data format used was JSON-LD. The forecast responses contain links to the appropriate weather icon and the weather description text is generally sufficiently detailed.
    * API Reliability : **-3**
        * Optional Notes : Extremely unreliable. Observation and forecast endpoints return stale data or **503** statuses. And it can be hours or days before the data is updated. In addition, there are times when a response is received but key data values are missing. The entries are present but the values are `null`.

Overall Score : **+1**

### Con VS Pro<br>

#### Con
* Unreliable delivery.
* Incomplete documentation.
* No support at all, not even forums.
* In some instances referenced data is missing.

#### Pro
* The forecast and observations text is verbose and can be used directly as content.
* Free
* A number of data formats are available.

### Recommendations

**API Users :** Use at your own risk. A measurable amount of code will need to be written to manage the data reliability issues.

**API Author(s) :** Overall the API needs a lot of work. Address the reliability issues first, then define the terminology and improve the documentation. If it is an active *work in progress* then it would be good idea to make that known.

### Review Author Info

* GitHub Handle - jxmot
* Website(s) : 
    * <https://github.com/jxmot>
* Date of Review - 2018-08-29

<hr>
<p align="center">
©&nbsp;&nbsp;Jim&nbsp;Motyl&nbsp;<a href="https://github.com/jxmot" target="_blank">jxmot</a>
&nbsp;&nbsp;
<a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-sa/4.0/88x31.png" /></a><br />This work is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-sa/4.0/">Creative Commons Attribution-ShareAlike 4.0 International License</a>.
</p>

