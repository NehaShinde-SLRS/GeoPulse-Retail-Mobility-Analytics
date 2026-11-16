# GeoPulse - Data Dictionary

All mobility records in this project are synthetic.

## 1. GPS Mobility Data

| Column | Data Type | Description |
|---|---|---|
| ping_id | String | Unique GPS record identifier |
| device_id | String | Synthetic anonymized device identifier |
| timestamp | Datetime | Date and time of simulated ping |
| latitude | Float | Simulated latitude |
| longitude | Float | Simulated longitude |
| h3_index | String | H3 geographic cell identifier |
| movement_type | String | Simulated movement category |

## 2. Store Location Data

| Column | Data Type | Description |
|---|---|---|
| store_id | String | Unique store identifier |
| store_name | String | Store name |
| latitude | Float | Store latitude |
| longitude | Float | Store longitude |
| store_type | String | Retail category |
| opening_date | Date | Simulated store opening date |

## 3. Competitor Location Data

| Column | Data Type | Description |
|---|---|---|
| competitor_id | String | Unique competitor identifier |
| competitor_name | String | Competitor name |
| latitude | Float | Competitor latitude |
| longitude | Float | Competitor longitude |
| competitor_type | String | Competitor category |

## 4. Analytical Output Data

| Column | Data Type | Description |
|---|---|---|
| h3_index | String | Geographic hexagon identifier |
| footfall_count | Integer | Simulated mobility ping count |
| unique_device_count | Integer | Distinct synthetic device count |
| store_id | String | Related store identifier |
| catchment_distance | Float | Distance from store |
| overlap_score | Float | Catchment overlap indicator |
| opportunity_score | Float | Simulated retail opportunity score |

## 5. Data Quality Rules

- GPS coordinates must be within valid geographic ranges.
- Ping identifiers must be unique.
- Device identifiers must be synthetic.
- Timestamps must use a consistent timezone convention.
- H3 indexes must be valid.
- Missing or invalid coordinates must be flagged.
- All analytical outputs must retain their synthetic-data disclaimer.

## 6. Important Note

Footfall counts represent generated synthetic observations,
not actual people or measured customer visits.