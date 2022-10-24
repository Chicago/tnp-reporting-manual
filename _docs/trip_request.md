---
title: Trip Request
category: Data Preparation
order: 1
---

## Scope

A record of each request for a trip made through the licensee's Internet-enabled application or digital platform by a potential passenger.

## File Format

Trip Request data must be reported using the following schema and reported with the following `[company]-triprequest-[date].csv`.

| Field | Element                       | Data Type                           | Required | Description                                                       | 
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------|-------------------------------------|----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| **NEW** R1 | Trip ID				         | String                              | Yes if request resulted in a trip      | Unique ID for trip, if matched. In this case, the value must match the Trip ID in T23.                                                       | 
| **NEW** R2 | Method                		 | String            				   | Yes      | Booking method for passenger. 1 for Smartphone app, 2 for Website, 3 for Phone call, and 4 for Other.   | 
| **NEW** R3 | Initiation Date and time		 | ISO 8601                            | Yes      | Date and time when passenger requested to be picked up.  | 
| **NEW** R4| Requested Mode                  | String 							   | Yes      | Indicate one of the following values: 1) shared, 2) private, 3) WAV.    |
| **NEW** R5| Number of Passengers          | Numeric							   | Yes      | The number of passengers that were indicated by the customer when the trip was requested. Leave blank if not indicated or unknown.   |
| **NEW** R6| Outcome                       | Numeric							   | Yes      | Indicator for the outcome of the e-hail request. 1 for Completed Trip - The passenger was picked up, 2 for No Accepts - There request was not accepted, either because there were no TNP drivers available or no available driver accepted the request, 3 for Passenger Canceled - The passenger canceled the request either before or after it was accepted by a TNP driver, 4 for Passenger No Show - The trip was canceled because the passenger was not at the pickup location, 5 for Driver Canceled - A TNP driver accepted the request but then canceled the trip and no other TNP vehicle was dispatched.   |
| **NEW** R7| Trip Price Quote Private Ride          | Numeric							   | Yes      | The price of the trip that was offered for a private, non-shared ride through the TNP's most used non-shared product. If no quote was given, leave blank.   |
| **NEW** R8| Trip Price Quote Shared Ride          | Numeric							   | Yes      | The price of the trip that was offered for a shared ride through the TNP's most used shared product. If no quote was given, leave blank.   |
