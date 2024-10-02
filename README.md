# AeroStat

*Extract and process public data on aviation incidents and accidents with the goal of identifying correlations between contributing factors.*

## Welcome

AeroStat aims to provide tools to help evaluate the following question:

>"Starting with a set of incidents and accidents in aviation, what internal and external variables could contribute to their occurrences?"

Noting that internal variables refer to human factors, systems, and structures, while external variables encompass factors outside the aircraft, such as weather and runway conditions.

Firstly, it is important to define the universe of the database, including any constraints, such as limiting the data to landing gear and brake events. The data is then categorized based on whether it affects flight safety, representing a "classification" problem with categorical or qualitative output.

In the latest version of the code, it shows which variables affect the event but not the extent of their impact.

### Database

The current database used in this code is sourced from the NTSB (National Transportation Safety Board): https://www.ntsb.gov/safety/data/Pages/Data_Stats.aspx

___

### Version Log

#### Initial Version

The initial version of the code is limited to events that happened on ground involving brake system or landing gear failures, leading to runway excursions.

The "eadmspub.pdf" file presents the variables listed in the NTSB database. Considering the variables that might have a direct involvement, the following lists will be the start point of variables under analysis:

##### "aircraft" data sheet
