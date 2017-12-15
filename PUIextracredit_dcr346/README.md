# Residential Permits Issuance and 311 Building Violations  complaints 
## Abstract:
This study sought to analyze the possible correlation between the **number of residential permits issuance** and buildings violations, represented by **311 building related complaints**. Using several sources of data including Census Bureau, NYC open data, 311 and NYC spatial data, a descriptive analysis and regression models were conducted to better understand the two urban factors. The results were insignificant, which not necessarily mean the correlation between the two isn't exist, rather than different or further methods could have better explain it. A more meaningful negative correlation was detected between renter-occupied housing units and BV complaints.
    
## Data
This research  rely on data from year 2016, and focus  on residential information only. Any personal information was excluded. The analysis was performed in the granularity level of Zip codes, which seemed a reasonable geographical unit to observe urban renewal trends.   
### DOB permit issuance
Permit Issuance data were obtained from [DOB permits issuance open data](https://data.cityofnewyork.us/Housing-Development/DOB-Permit-Issuance/ipu4-2q9a/data) and were cleaned to include **Residential permits** only, then were filtered again to include only **New Buildings** (NB) and **massive Alternation** (AL) permit types, ignoring plumbing, signs, equipment etc. permit types, that are insignificant to this research. The permits data were normalized by the **overall number of occupied housing units**, obtained from the US Census Bureau, [American Fact Finder website](https://factfinder.census.gov/faces/nav/jsf/pages/index.xhtml), using the ACS 5 years estimate data. Data for 2016 do not exist in the zip code geographical level; for that reason I used from year 2013, assuming the change in the number of housing units is not meaningful. All data were grouped by zip code to count the number of permits issued in each zip code in 2016.
 
### 311 building violation complaints
The [311 data](https://data.cityofnewyork.us/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9/data) were filtered to include only Building related complaints in year 2016. The 311 complaints are also divided by complaint descriptor; the descriptors were included in this analysis are:

- Illegal Conversion Of Residential Building/Space
- Illegal Commercial Use In Resident Zone
- Zoning - Non-Conforming/Illegal Vehicle Storage
- No Certificate Of Occupancy/Illegal/Contrary To CO
- SRO - Illegal Work/No Permit/Change In Occupancy/Use
- ROOFING
- PORCH/BALCONY
- SKYLIGHT
- GUTTER/LEADER
- FENCING

311 is a relatively new citizens-city engagement system, of which not all citizens are taking advantage or aware. To overcome this bias the 311 data were normalized by dividing each zip code's number of building-related complaints by its overall number of 311 complaints (see [Ipython notebook](https://github.com/danachermesh/PUI2017_dcr346/blob/master/PUIextracredit_dcr346/311Allcomplaints_data.ipynb)).

## Code
Code to generate this research is found [in this GitHub repo](https://github.com/danachermesh/PUI2017_dcr346/blob/master/PUIextracredit_dcr346/PUIextracredit_dcr346.ipynb). 

## Paper
This study was submitted as an Authorea paper, also included in this repo ([link to the Authorea doc](https://www.authorea.com/224137/wimjsFlEy1aEccNF-r0r3A)).

## Acknowledgment
This project is an expansion of my [former work](https://github.com/danachermesh/CivicAnalytics2017_dcr346/blob/master/Problem%20set%20-1/dcr346_CAproblemset1.ipynb) that had been done as a part of Civic Analytics course, taught by Prof. C.E. Kontokosta, NYU CUSP Fall 2017.
 
 For the Census data, Dr. Bianco helped me understand how to best navigate through their website. Also, got help from [Gitter.com](https://gitter.im/uscensusbureau/general)
