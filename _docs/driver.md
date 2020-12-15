---
title: Driver
category: Data Preparation
order: 3
---

## Scope

A record of each of the licensee's drivers who is authorized to pick up passengers using the licensee's Internet-enabled application or digital platform. Any eligible driver on the TNP platform must be reported in this file. This includes drivers who could have provided rides in the relevant time period but did not actually do so.

## File Format

Driver data must be reported using the following schema and reported with the following `[company]-driver-[date].csv`.

|  Field  |        Element          |         Data Type        |    Required    |       Description                  |
|---------|-------------------------|--------------------------|----------------|------------------------------------|
|   D1    | Driver Name             | String                   | Yes            | Full name of TNP driver                |
|   D2    | Driver's license number | String                   | Yes            | Driver's license number            |
|   D3    | Driver's license state  | ISO 3166-2 abbreviations | Yes            | State issuing the driver's license |
|   D4    | Driver's start date     | ISO-8601 date            | Yes            | Date when TNP driver became eligible to drive for your company |
|   D5    | Driver's end date       | ISO-8601 date            | Yes            | The final date the TNP driver was eligible to drive for your company (end of reporting period if still eligible) |
|   **NEW** D6    | Employee or Independent Contractor     | String                   | Yes            | The relationship between the TNP driver and the TNP: Enter W2 for Employee, 1099 for Independent Contractor  |
|   **NEW** D7    | Inactive Reason         | String                   | Yes            | Did the TNP driver initiate their inactive status? (Y/N) For drivers still active at the end of the month, leave blank.        |


