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

The initial version of the code is limited to events that happened on ground involving brake system or landing gear failures during landing, leading to runway excursions. Some assumptions are made, as follows:

* Any runway excursion is considered a catastrophic event
* The analysis is limited to aircraft category (var "acft_category = AIR")
* No homebuilt aircrafts (var "homebuilt = N")
* 

The "eadmspub.pdf" file presents the variables or predictors listed in the NTSB database. Considering the predictors that might have a direct involvement into the events, the following list will be the start point of variables under analysis:

##### "aircraft" data sheet

- ev_id: Event identifier
- far_part: 14 CFR Part, ex.: 91, 121, 135 etc
- cert_max_gr_wt: Certified max ground weight
- total_seats: Total seats
- num_eng: Number of engines
- fixed_retractable: Fixed or retractable landing gears
- second_pilot: Second pilot
- rwy_num: Runway number
- rwy_len: Runway length
- rwy_width: Runway width
- acft_year: Aircraft year

##### "Events_Sequence" data sheet

- ev_id: Event identifier
- phase_no = 550: Landing Runway excursion
- eventsoe_no = 300: Landing Runway excursion

##### "Finding" data sheet

- ev_id: Event identifier
- finding_description: Finding Description

##### "Events" data sheet

- ev_id: Event identifier
- ev_time: Event time
- ev_tmzn: Event time zone
