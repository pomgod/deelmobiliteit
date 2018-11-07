---
title: Trips
category: Monthly Submission
order: 1
---

# Reporting

All stakeholders within a MaaS Ecosystem have their own need for data. As mentioned in the previous chapter it is important to share data. Since not all data is needed in real-time and most data has sensitivity issues, some data could/should be shared in a report format. Not all data needs to be shared with 





## Trips

### Scope

All Trips completed during the reporting period. Trips in progress at the end of the reporting period should be held for the next report. For the purposes of this file, a trip is a transaction with a single rider.

### File Format <a id="file-format"></a>

Trip data must be reported using the following schema and reported with the following `[company]-trips-[date].csv`.

| Field | Element | Data Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| T1 | Trip ID | String | Yes | A unique identifier that identifies the trip. The identifier should be permanently unique, not just within the reporting period. |
| T2 | Bike ID | String | Yes | A unique identifier for the bicycle. Should be the same ID used throughout reporting requirements. |
| T3 | Start Time | ISO 8601 \(YYYY-MM-DDTHH:MM:SS+00:00\) | Yes | The date and time that the trip began \(e.g., 2018-06-30T20:06:06-05:00\). |
| T4 | End Time | ISO 8601 \(YYYY-MM-DDTHH:MM:SS+00:00\) | Yes | The date and time that the trip concluded \(e.g., 2018-06-30T20:06:06-05:00\). |
| T5 | From Latitude | Latitude \(WGS84\) | Yes | Latitude of where the trip began. |
| T6 | From Longitude | Longitude \(WGS84\) | Yes | Longitude of where the trip began. |
| T7 | To Latitude | Latitude \(WGS84\) | Yes | Latitude of where the trip ended. |
| T8 | To Longitude | Longitude \(WGS84\) | Yes | Longitude of where the trip ended. |
| T9 | Trip Distance | Numeric \(feet\) | Yes | The amount of distance the bicycle traveled during the course of the trip. |



## Customer Reports

### Scope <a id="scope"></a>

All reports, violations, and complaints submitted to the company. Should include all reports by customers and other members of the public, even if the report cannot be verified or was an invalid complaint.

### File Format <a id="file-format"></a>

Customer Report data must be reported using the following schema and reported with the following `[company]-reports-[date].csv`.

| Field | Element | Data Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| R1 | Report ID | String | Yes | A unique ID for the report. IDs should be permanently unique, not just unique within the reporting period. |
| R2 | Date and time reported | ISO 8601 \(YYYY-MM-DDTHH:MM:SS+00:00\) | Yes | The date and time of when the report was reported to the company \(e.g., 2018-06-30T20:06:06-05:00\). |
| R3 | Description | String | Yes | A text description of the alleged violation, complaint, comment, or other report. |
| R4 | Resolution | String | Yes | A text description of the action taken or other resolution by the company. To the extent possible, distinguish between reports determined to be unfounded and reports whose validity could not be determined \(e.g., report of inappropriate bicycle return for a bicycle rented again before the company could investigate\). |
| R5 | Latitude | Latitude \(WGS84\) | No | Latitude of the location of the alleged violation or other subject of the report. |
| R6 | Longitude | Longitude \(WGS84\) | No | Longitude of the location of the alleged violation or other subject of the report. |



## Maintenance

### Scope <a id="scope"></a>

All maintenance performed on the bicycles during the reporting period.

### File Format <a id="file-format"></a>

Maintenance data must be reported using the following schema and reported with the following `[company]-maintenance-[date].csv`.

| Field | Element | Data Type | Required | Description |
| :--- | :--- | :--- | :--- | :--- |
| M1 | Bike ID | String | Yes | A unique ID for the bicycle. Should be the same ID used in the Trips file. |
| M2 | Maintenance Date | ISO 8601 \(YYYY-MM-DD\) | Yes | Date when the maintenance was conducted. The timestamp \(hour/minute\) not required. |
| M3 | Description | String | Yes | Text description of the maintenance completed. |

