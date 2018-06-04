---
title: Data Quality
category: Data Submission
order: 1
---

## Scope

TNPs should check all files for data quality before submission and verify that they pass *at least* the following tests. Additional tests as each TNP sees fit are highly encouraged, as is reaching out to the City of Chicago for any discussion each TNP thinks useful in this effort.

Errors detected should be fixed before file submission. If it is impossible or unreasonably difficult to fix the errors, TNPs should inform BACP of the nature and degree (such as number of records affected) of the known errors in a file.

## File Format

| Standard # | File(s)   | Standard                             | Test                                                |
|------------|-----------|--------------------------------------|-----------------------------------------------------|
| 1          | Driver    | Driver ID columns complete           | D1, D2, and D3 contain no blanks.                   |
| 2          | Session   | Driver ID columns complete           | S1 and S2 contain no blanks.                        |
| 3          | Trip      | Driver ID columns complete           | T1 and T2 contain no blanks.                        |
| 4          | Vehicle   | Driver ID columns complete           | V8 and V9 contain no blanks.                        |
| 5          | Trip      | Shared trip columns complete         | T14 and T15 contain no blanks.                      |
| 6          | Vehicle   | Vehicle ID columns complete          | V1, V2, and V3 contain no blanks.                   |
| 7          | Trip      | Vehicle ID columns complete          | T3 contains no blanks.                              |
| 8          | Vehicle   | Vehicle description columns complete | V4, V5, V6, and V7 contain no blanks.               |
| 9          | Vehicle   | WAV column complete                  | V10 contains either `Y` or `N` for every record.    |
| 10         | Vehicle   | Valid inspection date                | V11 contains a date in the past for every record.   |
| 11         | Driver    | No duplicates                        | No combination of D2/D3 values appears more than once. |
| 12         | Vehicle   | No duplicates                        | No V1 value or combination of V2/V3 values appears more than once, *except if due to another driver (distinct V8/V9) also using the vehicle*. |
| 13         | Driver<br>Session | Session and Driver files match | All S1/S2 values have corresponding D2/D3 values. |
| 14         | Driver<br>Trip    | Trip and Driver files match    | All T1/T2 values have corresponding D2/D3 values. |
| 15         | Driver<br>Vehicle | Vehicle and Driver files match | All V8/V9 values have corresponding D2/D3 values. |
| 16         | Trip<br>Vehicle   | Trip and Vehicle files match   | All T3 values have a corresponding V1 value.      |
| 17         | All       | Valid data types         | All non-string columns contain values valid for the column type. |

## File Content

The above tests are designed to detect structural errors in the data files. TNPs should also make reasonable efforts to check for situations in which data are structurally valid but incorrect. While no list can be comprehensive, *examples* of things to check might include:

*	The number of records in the file is correct.
*	No records have been excluded in any reasonably detectible way.
*	No excess records have been included in any reasonably detectible way.
*	All values fall into plausible ranges.
*	Totals, averages, and other summary measures are consistent with internal benchmarks.
*	Continuous improvement: If a problem occurs in one period – and especially in multiple periods – add it to the test procedures for future periods. It is understandable if it never occurred to a TNP that a particular error could occur. However, after it does occur and is detected, it is reasonable to assume it might happen again and should be detected and corrected before file submission.
