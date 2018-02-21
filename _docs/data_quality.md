---
title: Data Quality
category: Data Quality
order: 1
---

## Scope

TNPs should check all files for data quality before submission and verify that they pass *at least* the following tests. Additional tests as each company sees fit are highly encouraged, as is reaching out to the City of Chicago for any discussion each company thinks useful in this effort.

Note that these tests are designed to detect structural errors in the data files. Companies should also make reasonable efforts to check for situations in which data are structurally valid but incorrect.

Errors detected should be fixed before file submission. If it is impossible or unreasonably difficult to fix the errors, companies should inform BACP of the nature and degree (such as number of records affected) of the known errors in a file.

## File Format

| File(s)   | Standard                             | Test                                                |
|-----------|--------------------------------------|-----------------------------------------------------|
| Driver    | Driver ID columns complete           | D1, D2, and D3 contain no blanks.                   |
| Session   | Driver ID columns complete           | S1 and S2 contain no blanks.                        |
| Trip      | Driver ID columns complete           | T1 and T2 contain no blanks.                        |
| Vehicle   | Driver ID columns complete           | V8 and V9 contain no blanks.                        |
| Trip      | Shared trip columns complete         | T14 and T15 contain no blanks.                      |
| Vehicle   | Vehicle ID columns complete          | V1, V2, and V3 contain no blanks.                   |
| Trip      | Vehicle ID columns complete          | T3 contains no blanks.                              |
| Vehicle   | Vehicle description columns complete | V4, V5, V6, and V7 contain no blanks.               |
| Vehicle   | WAV column complete                  | V10 contains either `Y` or `N` for every record.    |
| Vehicle   | Valid inspection date                | V11 contains a date in the past for every record.   |
| Driver    | No duplicates                        | No combination of D2/D3 values appears more than once. |
| Vehicle   | No duplicates                        | No V1 value or combination of V2/V3 values appears more than once, *except if due to another driver (distinct V8/V9) also using the vehicle*. |
| Driver<br>Session | Session and Driver files match | All S1/S2 values have corresponding D2/D3 values. |
| Driver<br>Trip    | Trip and Driver files match    | All T1/T2 values have corresponding D2/D3 values. |
| Driver<br>Vehicle | Vehicle and Driver files match | All V8/V9 values have corresponding D2/D3 values. |
| Trip<br>Vehicle   | Trip and Vehicle files match   | All T3 values have a corresponding V1 value.      |
| All       | Valid data types         | All non-string columns contain values valid for the column type. |

