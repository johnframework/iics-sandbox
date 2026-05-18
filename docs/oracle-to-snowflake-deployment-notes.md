# Oracle to Snowflake Pipeline - Deployment Notes

## Package: oracle-to-snowflake-v1.0.0.zip
## Environment: dev
## Version: 1.0.0
## Date: 2025-05-18

## What this Contains
- Mapping: m_oracle_to_snowflake
- Workflow: wf_oracle_to_snowflake
- Connection: Oracle 23ai source, Snowflake target

## Deployment Steps
1. Import package via IICS Explore > Import
2. Validate connections (Oracle, Snowflake)
3. Run taskflow and confirm row counts match source

## Validation Query
```sql
-- Run on Snowflake after load
SELECT COUNT(*) FROM target_table;
```

# Notes
- Secure Agent must be running on local desktop
- Oracle 23ai VM must be up before triggering pipeline
