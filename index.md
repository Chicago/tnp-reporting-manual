---
title: Overview
---

This manual is effective as of August 10, 2020. The information in this site, along with all prior versions of this manual, is stored at [GitHub](https://github.com/Chicago/tnp-reporting-manual/releases).

As part of its licensing process for Transportation Network Providers (sometimes called Ride-hail Providers), Chicago requires the companies to report on their activities monthly. These requirements are set forth in [Chapter 9-115](http://library.amlegal.com/nxt/gateway.dll/Illinois/chicago_il/title9vehiclestrafficandrailtransportati/chapter9-115transportationnetworkprovide?f=templates$fn=default.htm$3.0$vid=amlegal:chicago_il$anc=JD_Ch.9-115) of the Municipal Code of Chicago and [Rule TNP2.02](https://www.cityofchicago.org/content/dam/city/depts/bacp/rulesandregs/TNPRulesAmendedeffJan12017.pdf) issued by the Department of Business Affairs & Consumer Protection.

For questions relating to these reporting requirements, please e-mail [tnp-data-reporting@cityofchicago.org](mailto:tnp-data-reporting@cityofchicago.org).

For TNP matters relating to anything other than data reporting, please e-mail [BACPPV@cityofchicago.org](mailto:BACPPV@cityofchicago.org).

## Submission Deadlines

Below are the deadlines to have all required files (exceptions listed below the table) submitted to the City of Chicago.

|   Due Date   | Beginning Date |   End Date   |
|--------------|----------------|--------------|
| January 21   | December 1      | December 31  |
| February 21     | January 1      | January 31     |
| March 21      | February 1        | February 29      |
| April 21   | March 1         | March 31 |
| May 21  | April 1         | April 30 |
| June 21   | May 1         | May 31 |
| July 21   | June 1         | June 30 |
| August 21   | July 1         | July 31 |
| September 21   | August 1         | August 31 |
| October 21   | September 1         | September 30 |
| November 21   | October 1         | October 31 |
| December 21   | November 1         | November 30 |

Unless stated otherwise, for all files and fields unavailable or unknown values should be left blank. The number 0 should be used only when the value is known to be 0, not as an indicator of missing data. N/A or similar should not be used unless it is the actual text value of the field or the instructions specifically say to use it.

The trip request, location, and communication files are not required to be submitted on a regular basis, and shall be submitted as requested by the City. 

*New fields are marked as **NEW** in the field column for each data file page on this site.

## Submission Format

Submit at least five separate CSV files with the following naming convention, where [company] denotes the submitting company, [topic] represents one of the areas being requested: trip, driver, session, vehicle, compensation, and [date] corresponds to the period covered by the file (not the period when the file is submitted). For instance, ACME service submitting the driver file of drivers eligible in March 2016 would submit "acme-driver-201603.csv".

```
[company]-[topic]-[date].csv
```

Five files should be submitted monthly, consisting of one each for [trips](trip), [drivers](driver), [sessions](session), [vehicles](vehicle), and [compensation](compensation). TNPs will receive separate communications if a file should be submitted for [trip requests](trip_request), [locations](location), or [communications](communication).
