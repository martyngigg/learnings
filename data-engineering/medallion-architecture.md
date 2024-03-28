---
categories: Concepts,Data Architecture
---
# Medallion Architecture

<https://www.databricks.com/glossary/medallion-architecture>

- Data design pattern for organizing data in a lakehouse.
- Also referred to as "multi-hop" architecture.
- Goal of incrementally improving structure and quality of date as it moves
  through the layers.
- Typically 3 layers: bronze, silver, gold.
- Data flows from one to another.

## Bronze (raw)

- Raw ingested source data.
- Cleaned of personally identifiable information only.
- Serves as historical archive.
- Can be placed in cold storage.

## Silver (cleaned/conformed/enriched)

- Data from bronze layer filtered, cleaned, aggregated (just enough).
- Provides a sound reliable foundation for analyses and reports.
- Enterprise view of all key entities.
- Minimal transformations are applied at this layer (ELT vs ETL).
- More 3rd-normal form like data models.

## Gold (curated/business ready)

- Created around business functions/project needs, ready for consumption.
- For reporting and optimized for reading.
- Typically more denormalized data tables using Kimball star schemas or
  Inmon Data marts.
