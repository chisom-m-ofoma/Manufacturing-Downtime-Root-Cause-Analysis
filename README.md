# Manufacturing Downtime Root Cause Analysis

## Business Overview

Delcrone is a manufacturing company that uses Industrial Internet of Things (IoT) sensors to monitor machine health across its production facilities. Each factory contains multiple machine types that send telemetry data every 10 minutes.

Recently, stakeholders observed production delays and operational inefficiencies caused by frequent disruptions on the assembly lines.

The technology team collected and converted a month of IoT telemetry data from four production facilities to help identify the root cause of the downtime. 

The goal of this analysis is to identify the primary source of assembly-line disruption and to provide insights to improve operational efficiency.

### Key Metrics
- Which production facility experiences the highest machine downtime?
- Which machine types contribute the most to downtime in that facility?
- What percentage of total downtime is caused by the most problematic machines?

## Exploratory Data Analysis (EDA)

The telemetry dataset was explored using SQL to understand machine behavior across facilities.

#### Key exploration steps included:
- Inspecting data structure and health status categories
- Identifying all production facilities and machine types
- Measuring machine distribution across factories
- Calculating downtime events by facility
- Identifying machine types responsible for the most failures

[*Check Out Core SQL Queries*](XYZ)

## Insights

*General Dashboard image*

Analysis revealed that FACTORY A experiences the highest machine downtime across all facilities.

Further investigation shows that DEVICE TYPE A is responsible for the majority of downtime events in this facility, making it the most significant contributor to assembly line disruptions.

This is shown in the dashboard below.

*Filtered dashboard image*

## Recommendations
- Preventive maintenance efforts should prioritize DEVICE TYPE A MACHINES in FACTORY A.
- Monitor machine health trends weekly to detect early signs of failure.
- Implement automated alerts for machines entering unhealthy states.
