---
title: Compensation
category: Data Preparation
order: 7
---

## Scope

A record of each of the licensee's drivers who is paid an hourly rate, and any other record needed to capture actual TNP driver pay information that is not reflected in licensee's hourly rate compensation records.

## File Format

Compensation data must be reported using the following schema and reported with the following `[company]-compensation-[date].csv`.

| Field | Element                     | Data Type                | Required | Description                                                                                                                                                                                                           | 
|-------|-----------------------------|--------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------| 
| **NEW** COMP1    | Driver's license number     | String                   | Yes      | The driver's license number of the TNP driver for this record. This number must correspond with driver's license number listed in field D2.  
| **NEW** COMP2    | Driver's license state        | ISO 3166-2 abbreviations            | Yes      | The state issuing the driver's license that is listed in COMP1. The license number and license state combination should correspond to the fields D2 and D3.                                                                      | 
| **NEW** COMP3	| Total Fares | Numeric | Yes| Total fares from all passenger trips collected over reporting period. |
| **NEW** COMP4	| Hourly Pay | Numeric | Yes| Total of any hourly rate paid to the TNP driver, exclusive of all other compensation during reporting period. |
| **NEW** COMP5	| Trip Pay | Numeric | Yes| Total TNP driver trip pay as reported in the [trips data](/tnp-reporting-manual-draft/trip) (not including tolls or tips and net of fees and taxes taxes) over reporting period. |
| **NEW** COMP6     | Tips | Numeric | Yes| Total amount of tips received from passengers over reporting period. |
| **NEW** COMP7	| Other Compensation | Numeric | Yes| Total value of any other compensation that is not reflected by any other fields in this dataset, including incentives, bonuses and any other payments. |
| **NEW** COMP8	| Vehicle Payment Deduction | Numeric | Yes| Total deductions for pay to cover TNP vehicle payments. |
| **NEW** COMP9	| Gas Deduction | Numeric | Yes| Total deductions from pay to cover gas expenses. |
| **NEW** COMP10 	| Cleaning Deduction | Numeric | Yes| Total deductions from pay to cover cleaning fees. |
| **NEW** COMP11	| Other Deduction | Numeric | Yes| Total deductions from pay for other expenses. |
| **NEW** COMP12	| Driver Net Pay | Numeric | Yes| Total TNP driver net pay including bonus payments and subtracting deductions. |
| **NEW** COMP13    | Report Period Start Date | ISO 8601 | Yes | Start date of reporting period for pay/incentives/deductions. |
| **NEW** COMP14    | Report Period End Date | ISO 8601 | Yes | Start date of reporting period for pay/incentives/deductions. |