---
title: Session
category: Data Preparation
order: 4
---

## Scope

A record of each TNP driver session on the licensee's Internet-enabled application or digital platform. For purposes of this section, a driver's session begins
when a licensee's driver activates a mode in the licensee's Internet-enabled application or digital platform, signaling the driver's readiness to receive and respond to trip requests. For purposes of this section, a driver's session ends when the driver deactivates the mode and is no longer able to receive and respond to TNP requests.

All sessions completed during the reporting period must be reported in this file.  Sessions in progress at the end of the reporting period should be held for the next report.

## File Format

Session data must be reported using the following schema and reported with the following `[company]-session-[date].csv`.

| Field | Element                     | Data Type                | Required | Description                                                                                                                                                                                                           | 
|-------|-----------------------------|--------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| S1    | Driver's license number     | String                   | Yes      | The driver's license number of the TNP driver for this trip. This number must correspond with driver's license number listed in field D2.                                                                                 | 
| S2    | Driver's license state        | ISO 3166-2 abbreviations            | Yes      | The state issuing the driver's license that is listed in S1. The license number and license state combination should correspond to the fields D2 and D3.                                                             | 
| S3    | Session start date and time | ISO 8601                 | Yes      | The date and time when a TNP driver logs in to the application or otherwise becomes eligible to be hired for a trip for customers. All times must be local time zone and must be noted per ISO 8601 specifications.       | 
| S4    | Session end date and time   | ISO 8601                 | Yes      | The date and time when a TNP driver logs off the application or otherwise is no longer eligible to provide trips to customers. All times must be local time zone and must be noted per ISO 8601 specifications. | 
| **NEW** S5    | Miles Traveled Total   	  | Numeric                  | Yes      | Total miles traveled during session. |
| **NEW** S6    | Miles Traveled with Passenger  | Numeric                  | Yes      | Total miles traveled with a passenger during session. | 
| **NEW** S7    | Session End Reason   		  | String                  | Yes      | Indicator of whether or not the TNP driver initiated the end of the session, either by logging off or leaving the service area. Y for driver initiated end of session, N for driver did not initiate end of session. | 