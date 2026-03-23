## ETL Decisions

### Decision 1 – Date Format Standardization
* Problem: Dates were in inconsistent formats in raw data.
* Resolution: Converted all dates into standard YYYY-MM-DD format.

### Decision 2 – Handling NULL Values
* Problem: Some fields had NULL values.
* Resolution: Replaced NULLs with default values or removed incomplete rows.

### Decision 3 – Category Standardization
* Problem: Product categories had inconsistent casing (e.g., clothing, Clothing).
* Resolution: Standardized all categories to proper case format.
