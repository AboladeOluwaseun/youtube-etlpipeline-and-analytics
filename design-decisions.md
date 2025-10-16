# Design Decisions

## Why AWS Glue over Apache Spark on EC2?
- **Serverless:** No infrastructure management
- **Cost-effective:** Pay per DPU-hour, scales automatically
- **Native integration:** Works seamlessly with S3 and Data Catalog
- **Maintenance-free:** AWS handles updates and patching

## Why Athena over Redshift?
- **For exploratory queries:** Fast, ad-hoc analysis without pre-loading
- **Cost:** Pay only for data scanned
- **Alternative:** Use Redshift for complex joins on large datasets

## Medallion Architecture (Bronze/Silver/Gold)?
- **Bronze (Landing):** Raw, unprocessed data
- **Silver (Cleansed):** Validated, deduplicated, standardized
- **Gold (Analytics):** Aggregated, business-ready for reporting