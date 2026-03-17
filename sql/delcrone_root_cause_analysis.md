## Exploratory Data Analysis (EDA)

```sql
SELECT *
FROM delcrone_telemetry_data
LIMIT 10;

SELECT COUNT(*) AS total_records
FROM delcrone_telemetry_data;

SELECT DISTINCT document_index
FROM delcrone_telemetry_data;

SELECT DISTINCT device_type
FROM delcrone_telemetry_data;

SELECT document_index,
COUNT(DISTINCT device_id) AS machines
FROM delcrone_telemetry_data
GROUP BY document_index;

SELECT status,
COUNT(*) AS occurrences
FROM delcrone_telemetry_data
GROUP BY status;
```

## Calculated Fields

#### Downtime Events

```tableau
IF[Status]="unhealthy" THEN 10 ELSE 0 END
```

#### Facility Downtime & Machine Failure

```tableau
{ FIXED [Device Type]: SUM(IF [Status]="unhealthy" THEN 1 END)}

IF [Facility downtime]={ FIXED :MAX([Facility downtime])} THEN [Factory]END

{ FIXED [Device Type]: SUM(IF [Status]="unhealthy" THEN 1 END)}

IF [Machine failure]={ FIXED :MAX([Machine failure])}THEN[Device Type]END
```
