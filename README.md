# CROP IRRIGATION ASCE-EWRI (2005)

To start the program, download the entire content of the repository as a compressed file. Then extract the contents on your local computer and launch the calculator with the main file.

To calculate the irrigation requirements for your crop, you will need several parameters. Then you will be able to find the amount in liters per square meter of water you need to supply your crop. The calculations use the reference crop of short grass. You can find what your specific crop requirements are in comparison to the short grass reference, however, they do not vary much from the reference crop. The program was written with functions from the RefET library in python, however no coding is required to launch the app. 

The calculations are for the daily requirements. What I usually do is wait until the day is over and collect all the data, run the program, and irrigate one day later.

Variables
=========

1. Dew point: This variable has the unit of degrees celsius, enter the whole number or decimal as input and convert from fahrenheit if necessary.

2. Temperature: This is also in degrees celsius in whole or decimal numbers.

3. Solar radiation: This is a bit more difficult, the units are megajoules per square meter per day. If you found this, then it is straightforward. However, it is often saved in watts per square meter, this equals one joule per square meter per second. So to convert from watts per square meter you need to multiply by 3600 and then multiply with the hours of daylight on the day of measurement.

          Example: 500 watts per square meter = 500 joules per second per square meter
          This results in 27 megajoules per square meter per day

          1. multiply 500 watts per square meter by 3600 for 1 hour 
          -> 1 800 000 joules per hour per square meter
          
          2. multiply the result with the hours daylight, in this case 15 hours
          -> 27 000 000 joules per square meter per day
          
          3. divide the result by 1 000 000 to get the amount in megajoules per square meter per day 
          ==> 27 megajoules per square meter per day

4. Wind speed: This is measured in kilometers per hour and needs to be converted if you have it in meters per second or miles per hour.

5. Day of year: This asks the calendar day with January 1st as day 1, an example would be May 4th 2020 is day 125.

6. Altitude: This asks for meters above sealevel of your location of measurement, conversion is needed from feet or kilometer.

7. Latitude: This is asked as a decimal value for your location, sometimes it is noted in degrees so you would need to convert it.

8. Rainfall: This variable is the amount of rain on the day of measurement in liters per square meter or milimeters per square meter. It is the same unit as the result for irrigating your crop.

Results
=======

After you have submitted all the variables the calculations will return the amount of irrigation your crops need. This is again in liters per square meters or milimeters per square meter. The calculations first find out what the evaporation via the soil and transpiration via the crop is. This totals the evapotranspiration that is compared to the rainfall to gain the irrigation requirements of the day. Therefore you would still need to understand the speed of your irrigation system, i.e. how many seconds does it take for your pipe to output 1 liter? This way you know how many second you need to irrigate every square meter.

According to current statistics at the world bank, high income countries currently produce up to 600-700 kilograms of non-meat agricultural products per person per year. However, meat consumption has risen in higher income countries to 100 kilograms per person per year. Every kilogram of meat takes up to 20 kilograms of cereals to feed the livestock. Thereby, this amounts to 2200 or more kilograms consumption per person per year, who consume very high amounts of meat. Therefore, these statistics cannot be sustained in the long term for having universal zero hunger results.

References
==========

1. RefET (2019) Computing daily and hourly reference ET following the ASCE Standardized Reference Evapotranspiration Equations (ASCE 2005). https://pypi.org/project/refet/

2. ASCE-EWRI (2005). The ASCE standardized reference evapotranspiration equation. https://ascelibrary.org/doi/book/10.1061/9780784408056

3. Departement Landbouw & Visserij (2020) Berekening irrigatiebehoefte per seizoen. https://lv.vlaanderen.be/nl/voorlichting-info/publicaties/praktijkgidsen/water/duurzaam-watergebruik-de-openluchtgroenteteelt-5
