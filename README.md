# Post-Harvest Losses Dataset

This dataset contains information about post-harvest losses of various agricultural commodities in different countries.

## Columns

### Main Columns

| Column Name        | Description |
|--------------------|------------|
| `m49_code`         | Numeric code representing a country/geographical area (UN M49 standard) |
| `commodity`        | Agricultural product (e.g., rice, wheat, maize) |
| `year`            | Year of data collection |
| `loss_percentage` | Estimated percentage loss (post-harvest, pre-consumer) |
| `activity`        | *(Original column)* Stage/activity where loss occurred (e.g., storage, handling, transportation) - later transformed |
| `cause_of_loss`   | *(Excluded from analysis)* Reason for loss (pests, diseases, poor storage, etc.) |
| `treatment`       | *(Excluded from analysis)* Interventions applied to reduce losses |

### Derived Columns (Post-Processing)
New columns were generated from the `activity` column, each representing a unique activity with binary values:
- `1`: Activity was involved in the loss
- `0`: Activity was not involved

## Data Cleaning and Transformations

### Activity Column Transformation
- Original `activity` column (containing multiple activities in strings) was split into separate binary columns for each unique activity

### Data Filtering
1. Removed entries for:
   - "Rice, milled"
   - "Other pulses n.e.c."
   *(Due to limited data or differing loss profiles)*

2. Dropped rows with missing data to improve quality

## Notes
- Loss percentage represents proportion of total harvested quantity
- Data contains estimations (may not reflect exact losses)
- Refer to source documentation for detailed methodology
