# Test Plan - PCTO Manager

**Team 3** - April 10, 2020

**Team Members:** Ambrosi Marco, Bonoldi Enrico, Lorenzoni Luca

**Revision History**

| **Author**   | **Change Date** | **Description of changes** |
| ------------ | --------------- | -------------------------- |
| L. Lorenzoni | 13/04/2020      | Initial Release            |
|              |                 |                            |

- [Test Plan - PCTO Manager](#test-plan---pcto-manager)
  - [Introduction](#introduction)
  - [Incidents](#incidents)
  - [Defects](#defects)
  - [Summary](#summary)

## Introduction

This document outlines the outcome of completed system tests.  Incidents, Defects and Changes that need to be made will be presented here formally.  Although the ideas expressed here are separate entities, they will be combined into this one document.

## Incidents

This section defines the incidents discovered while performing various tests on the system.  This section will expand as more incidents are found.For each incident there is a serial number.


|             |                                                                    |
| ----------- | ------------------------------------------------------------------ |
| ID          | 1                                                                  |
| Description | Data visibility on the school database                             |
| Date        | 13-11-2019                                                         |
| Severity    | low                                                                |
| Responder   | Bonoldi Enrico - Ambrosi Marco                                     |
| Cause       | Wrong configuration inside the DB scheme for our user access level |
| Status      | Close                                                              |
| Resolution  | Check the previus user access levels and update the references     |

|             |                                                       |
| ----------- | ----------------------------------------------------- |
| ID          | 1                                                     |
| Description | The ETL doesn't respond to the actual data structure  |
| Date        | 10-12-2019                                            |
| Severity    | medium                                                |
| Responder   | Bonoldi Enrico                                        |
| Cause       | Wrong configuration inside the Laravel service        |
| Status      | Close                                                 |
| Resolution  | Check the data structures inside the database imports |


|             |                                                          |
| ----------- | -------------------------------------------------------- |
| ID          | 3                                                        |
| Description | Data normalization inconsistency                         |
| Date        | 29-11-2019                                               |
| Severity    | medium                                                   |
| Responder   | Lorenzoni Luca - Bonoldi Enrico                          |
| Cause       | Exported data was not nomalized and errors were presents |
| Status      | Close                                                    |
| Resolution  | Validation system                                        | s |
 

## Defects

At this time, defects that were found were labeled as incidents.

## Summary

Up to now there are no other issues with the project.

Further system testing will be done as newly implemented features become available. These features include all the functionality of the Students page which entails adding and removing reviews on companies.