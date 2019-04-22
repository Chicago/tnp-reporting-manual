---
title: Session
category: Data Preparation
order: 2
---

## Scope

All sessions completed during the reporting period.  Sessions in progress at the end of the reporting period should be held for the next report.

## File Format

Session data must be reported using the following schema and reported with the following `[company]-session-[date].csv`.

| Field | Element                     | Data Type                | Required | Description                                                                                                                                                                                                           | 
|-------|-----------------------------|--------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| S1    | Driver's license number     | String                   | Yes      | The driver's license number of the driver for this trip. This number must correspond with driver's license number listed in field D1.                                                                                 | 
| S2    | Driver's license state      | ISO 3166-2 abbreviations | Yes      | The state issuing the driver's license that is listed in S1. The license number and license state combination should correspond to the fields D1 and D2.                                                              | 
| S3    | Session start date and time | ISO 8601                 | Yes      | The date and time when a driver logs in to the application or otherwise becomes eligible to be hired for a trip for customers. All times must be local time zone and must be noted per ISO 8601 specifications.       | 
| S4    | Session end date and time   | ISO 8601                 | Yes      | The date and time when a driver logs off the application or otherwise is no longer eligible to provide trips to customers. All times must be local time zone and must be noted per ISO 8601 specifications. | 
