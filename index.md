This page is a summary of data pulled from effluent reports for fertilizer manufacturing.

# 1.	IDENTIFYING NPDES PERMITS ASSOCIATED WITH FERTILIZER MANUFACTURING

I used [EPA’s Water Pollution Search tool](https://echo.epa.gov/trends/loading-tool/water-pollution-search) to identify 2021 Discharge Monitoring Reports (DMRs) associated with Industrial Sector IDs (SIC codes) or North American Industry Classification System codes (NAIC codes) corresponding to fertilizer manufacturing. 

*Note, I could alternatively use the [Facility Search tool](https://echo.epa.gov/facilities/facility-search?mediaSelected=all) to see all facilities with these codes including ones that may not have DMR data. Also note that I pull data from preceding years associated with permits existing in 2021, but I could expand this list to permits not included in 2021 if desired.

This search yeilds the following permits:

CATEGORY | SIC | NAICS | UNIQUE PERMITS
---------|-----|-------|---------------
Fertilizer (Mixing Only) Manufacturing |2875 |325314 |**373**
Nitrogenous Fertilizer Manufacturing |2873 |325311 |**82** 
Phosphatic Fertilizer Manufacturing |874 |325312|**30**

Across search terms and facility types, this search yields a total of **485 unique NPDES permits**.

2.	ACCESSING EFFLUENT CHARTS

For each of the unique NPDES permits, I pulled the full effluent chart data. (Technically, I missed the first permit (which is in Alaska) due to an error, so there are 484 not 485 permits in the analysis moving forward, but I can add it in or we can say this is for contiguous U.S.)

I used a script, but this is identical to downloading the chart available here on ECHO: https://echo.epa.gov/effluent-charts#AR0000752, which can be accessed by searching the NPDES permit ID using the Water Pollution Search tool (https://echo.epa.gov/trends/loading-tool/water-pollution-search), selecting the facility, clicking “View Effluent Charts”, and then clicking “Download All Data.”

Across the 484 permits, this yields 128,655 total observations of 249 different pollutants. 298 of the permits have NO DATA in the effluent charts, so this results in data only for 186 permits.
 
3.	FILTERING FOR POLLUTANTS OF INTEREST

I then subset the data for the 186 permits with data to extract observations of N pollutants. (If there are other pollutants of interest — such as phosphorus, I can also pull these out, but for simplicity, I will focus on N for now.) 

Of the 249 pollutants in the full dataset, I selected any observations that matched the 14 different parameter names below associated with N pollution:

1.	Ammonia nitrogen, total, [as N] 30 day
2.	Ammonia, unionized
3.	Annual Nitrate Nitrogen Discharged
4.	Nitrogen, total [as N]
5.	Ammonia [as N] + unionized ammonia
6.	Nitrogen, ammonia total [as N]
7.	Nitrite + Nitrate total [as N]
8.	Nitrogen, nitrate total [as N]
9.	Nitrogen, organic total [as N]
10.	Nitrite Plus Nitrate Total
11.	Nitrogen, Kjeldahl, total [as N]
12.	Nitrogen, nitrite total [as N]
13.	Nitrogen, ammonia, total [as NH3]
14.	Nitrogen, ammonia total [as NH4]

Note that for accurate comparisons across N pollutant names, the last two should be converted to [as N] by multiplying [as NH3] by 0.82 or [as NH4] by 0.77.

There are 140 permits with observations of one of the parameters above. 

Observations may be in units of mg/L (concentrations) or kg/d. Observations may also be minimum, maximum or average values at different timescales. For the plots below, I selected only Daily Average observations. I think we would want to expand this to include other timescales as they match permit requirements.

Looking only at observations of Daily Average discharges, this yields 192 observations of N pollutants in units of kg/d and 184 observations in mg/L. Note that only N or P manufacturing facilities (no mixing facilities) show up after this series of filtering, and there are only three permits ("GA0002071", "GA0002356", "TX0007285") with values under this narrow filtering. 






 
![image](https://user-images.githubusercontent.com/72046860/124164350-89e9f100-da6e-11eb-843d-076f554ec1f7.png)
