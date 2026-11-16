# GeoPulse - System Architecture

## 1. Architecture Overview

GeoPulse follows a modular data engineering and
geospatial analytics architecture.

## 2. Data Flow

### Layer 1: Synthetic Data Generation
- Generate synthetic GPS mobility pings.
- Generate store and competitor locations.
- Generate timestamps and anonymized device IDs.
- Store generated datasets in CSV or Parquet format.

### Layer 2: Data Storage
- Organize raw and processed datasets.
- Use Snowflake for analytical storage.
- Use GEOGRAPHY columns for spatial data.

### Layer 3: Geospatial Processing
- Use Python, GeoPandas and Shapely.
- Use PySpark and Apache Sedona for scalable
  spatial processing.
- Use H3 for hexagonal geographic aggregation.

### Layer 4: Data Transformation
- Use dbt to organize and transform analytical models.
- Build staging, intermediate and mart models.
- Test data quality and model assumptions.

### Layer 5: Business Analytics
- Calculate pedestrian footfall.
- Analyze catchment overlap.
- Evaluate competitor proximity.
- Estimate potential cannibalization scenarios.
- Calculate retail location opportunity scores.

### Layer 6: Visualization
- Use Plotly and Kepler.gl for geospatial exploration.
- Use React for the interactive dashboard.

### Layer 7: Orchestration
- Use Apache Airflow to coordinate repeatable
  data generation and processing workflows.

## 3. High-Level Architecture

Synthetic Data Generator
        |
        v
Raw Data Storage
        |
        v
Snowflake Data Warehouse
        |
        v
PySpark / Apache Sedona
        |
        v
H3 Spatial Aggregation
        |
        v
dbt Transformation Models
        |
        v
Retail Analytics
        |
        v
Plotly / Kepler.gl / React Dashboard

Apache Airflow coordinates the applicable workflows.

## 4. Important Design Principles

- Modular and reusable Python code.
- Reproducible synthetic data generation.
- Data quality validation.
- Privacy-conscious data design.
- Clear separation of raw and processed data.
- Scalable geospatial processing.

## 5. Simulation Disclaimer

All mobility data and resulting analytical findings
are synthetic and illustrative.

Potential cannibalization scores are scenario-based
indicators, not measurements of actual customer loss.