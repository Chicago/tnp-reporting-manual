---
title: Trip
category: Data Preparation
order: 2
---

## Scope

A record of each trip which shows where a passenger is picked up and dropped off. Must include all Trips completed during the reporting period.  Trips in progress at the end of the reporting period should be held for the next report.  For the purposes of this file, a trip is a transaction with a specific customer, including any additional people transported under the same transaction. A transaction with a different customer, even if present in the vehicle at the same time, is a separate trip.

## File Format

Trip data must be reported using the following schema and reported with the following `[company]-trip-[date].csv`.

| Field | Element                       | Data Type                           | Required | Description                                                       | 
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|-------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| T1 | Driver's license number       | String                              | Yes      | The driver's license number of the TNP driver for this trip. This number must correspond with driver's license number listed in field D2.                                                        | 
| T2 | Driver's license state        | ISO 3166-2 abbreviations            | Yes      | The state issuing the driver's license that is listed in T1. The license number and license state combination should correspond to the fields D2 and D3.                                     | 
| T3 | Vehicle Identification Number | ISO 3833                            | Yes      | The VIN of the TNP vehicle that made the trip. This field must correspond with one of the entries in V1.                                                                                         | 
| T4 | Fare Start Date and Time      | ISO 8601                            | Yes      | The date and time of when the trip started. All times must be local time zone and must be noted per ISO 8601 specifications.                                                                 | 
| T5 | Fare Start Location           | Numeric                             | Yes      | The Census Block 2010 corresponding to the starting location of the trip. <br> *(Note: Reporting Latitude and Longitude for this field and T7 instead of Census Blocks is acceptable by special arrangement.)* |
| T6 | Fare End Date and Time        | ISO 8601                            | Yes      | The date and time of when the trip ended. All times must be local time zone and must be noted per ISO 8601 specifications.                                                         | 
| T7 | Fare End Location             | Numeric                             | Yes      | The Census Block 2010 corresponding to the ending location of the trip.                                                                                                                      | 
| T8 | Distance                      | Numeric                             | Yes      | The total distance of the trip as measured by the distances travelled on the road and expressed in miles.                                                                                    | 
| T9 | Total cost                    | Numeric, up to two decimal points | Yes      | The total cost, including tip, taxes, and all charges, charged to the customer. Do not use currency symbols. This elements should equal the sum of T10, T11, T12, and T13.                 | 
| T10| Total fare                    | Numeric, up to two decimal points | Yes      | The fare charged for the consumer, including any initial "flag drop" costs and per milage cost. Do not use currency symbols.                                                             | 
| T11| Tip                           | Numeric, up to two decimal points | Yes      | The tip provided by the customer for the trip. The amount 0.00 should be used if no tip was provided. Do not use currency symbols.                                                           | 
| T12| Taxes and fees                | Numeric, up to two decimal points | Yes      | The total taxes and fees charged to the consumer, including any "pick-up" or other taxes. The amount 0.00 should be used if no taxes or fees were charged. Do not use currency symbols.  | 
| T13| Other charges                 | Numeric, up to two decimal points | Yes      | Other charges and fees levied for the customer (e.g., tolls). If no other charges were rendered, the amount 0.00 should be used. Do not use currency symbols.                             | 
| T14| Shared Trip Authorized        | String                              | Yes      | Did the customer agree to a shared trip, regardless of whether the trip was actually shared. Enter Y or N only.                                                                            | 
| T15| Shared Trip ID                | String                              | Yes      | Each complete empty-to-empty run of a TNP vehicle should be assigned a unique ID and this ID should be entered into this field. The ID should be a non-case-sensitive string value with any letters represented in their capital forms. Each TNP may use a coding system of its liking to assign the IDs. Therefore the IDs need only be unique within a TNP, not between TNPs.  However, within that TNP, the ID must be permanently unique, not just unique within the reporting period. Every trip record within the empty-to-empty run should list the same Shared Trip ID. | 
| **NEW** T16| Fare Start Latitude 			 | Numeric							   | Yes      | Latitude where the TNP driver indicated the passenger was picked up. Precision at 4 decimal places. |
| **NEW** T17| Fare Start Longitude			 | Numeric							   | Yes      | Longitude where the TNP driver indicated the passenger was picked up. Precision at 4 decimal places. |
| **NEW** T18| Fare End Latitude 			 | Numeric							   | Yes      | Latitude where the TNP driver indicated the passenger was dropped off. Precision at 4 decimal places. |
| **NEW** T19| Fare End Longitude			 | Numeric							   | Yes      | Longitude where the TNP driver indicated the passenger was dropped off. Precision at 4 decimal places. |
| **NEW** T20| Tolls						 | Numeric							   | Yes      | Road, bridge, and other tolls charged to the customer. |
| **NEW** T21| Government Taxes	and Fees		 | Numeric							   | Yes      | Government taxes and fees charged to the customer. |
| **NEW** T22| TNP Fees			     | Numeric							   | Yes      | TNP fees charged to the customer. |
| **NEW** T23| Trip ID 						 | String							   | Yes      | Unique identifier for each trip. | 
| **NEW** T24| Number of Passengers			 | Numeric							   | Yes      | The number of passengers associated with this trip ID that were transported by the TNP vehicle . |
| **NEW** T25| On Scene Date and Time		 | ISO 8601							   | Yes      | Date and time when TNP driver arrived at the pick-up location |
| **NEW** T26| Driver Trip Pay 			 	 | Numeric							   | Yes      | Total TNP driver pay if the driver was compensated on a per-trip basis for the trip (not including tolls or tips and net of fees and taxes). Otherwise, include compensation in [compensation data](/tnp-reporting-manual-draft/compensation). |
| **NEW** T27| Shared Trip Match			 | String							   | Yes      | Did the passenger share the TNP vehicle with another passenger who booked separately at any point during the trip? (Y/N) |
| **NEW** T28| Time in Transit Outside Chicago | Numeric						   | Yes	  | For trips that begin outside, end outside, or otherwise leave Chicago, the trip time in seconds spent outside of city boundaries. |
| **NEW** T29| Miles Traveled Chicago 		 | Numeric						       | Yes	  | For trips that begin outside, end outside, or otherwise leave Chicago, the trip distance spent outside of city boundaries. |