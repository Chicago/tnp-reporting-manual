---
title: Location
category: Data Preparation
order: 6
---

## Scope

For every transportation network vehicle and driver combination, location snapshots captured **every 60 seconds** for all times the driver is in a session, as defined in subsection (b)(4) of [Chapter 9-115 of the Municpal Code of Chicago](http://library.amlegal.com/nxt/gateway.dll/Illinois/chicago_il/title9vehiclestrafficandrailtransportati/chapter9-115transportationnetworkprovide?f=templates$fn=default.htm$3.0$vid=amlegal:chicago_il$anc=JD_Ch.9-115). Each snapshot shall indicate the vehicle's precise location and corresponding date and time.

## File Format

Location data must be reported using the following schema and reported with the following `[company]-location-[date].csv`.

| Field | Element                     | Data Type                | Required | Description                                                                                                                                                                                                           | 
|-------|-----------------------------|--------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| **NEW** L1    | Driver's license number     | String                   | Yes      | The driver's license number of the driver for this location. This number must correspond with driver's license number listed in field D2.
| **NEW** L2    | Driver's license state        | ISO 3166-2 abbreviations            | Yes      | The state issuing the driver's license that is listed in L1. The license number and license state combination should correspond to the fields D2 and D3.                                                                          | 
| **NEW** L3    | Vehicle license plate number  | String                   | Yes      | The license plate on the car registered for service with your company.  |
| **NEW** L4    | Location Date and Time        | ISO 8601                 | Yes      | Date and time of the vehicle location reading. | 
| **NEW** L5    | Latitude 			 			| String							   | Yes      | Latitude of the vehicle location. Precision at 4 decimal places. |
| **NEW** L6    | Longitude			 			| String							   | Yes      | Longitude of the vehicle location. Precision at 4 decimal places. |
