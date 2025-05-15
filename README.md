This dataset contains information about post-harvest losses of various agricultural commodities in different countries.

Columns
Here's a breakdown of each column in the dataset:

Column Name	Description
m49_code	A numeric code representing a country or geographical area, following the UN M49 standard.
commodity	The specific agricultural product, such as rice, wheat, maize, etc.
year	The year in which the data was collected.
loss_percentage	The estimated percentage of loss for the given commodity in the specified region and year, after harvest and before reaching the consumer.
activity	(Original Column, later transformed) A text description of the stage or activity during which the post-harvest loss occurred (e.g., storage, handling, transportation). This column was later processed to create individual columns for each specific activity.
[Activity Columns]	(Derived Columns) - After data processing, new columns were generated, each representing a unique activity from the original 'activity' column. These columns contain 1 or 0, indicating whether the specific activity was involved in the loss for that data point.
cause_of_loss	(Excluded from analysis) A description of the underlying reason for the loss, such as pests, diseases, or poor storage conditions.
treatment	(Excluded from analysis) Information about any treatments or interventions applied to prevent or reduce losses.
Data Cleaning and Transformations
Activity Column Transformation: The original activity column, containing multiple activities in a single string, was broken down into separate columns for each unique activity to facilitate analysis.
Data Filtering:
Entries for "Rice, milled" and "Other pulses n.e.c." were removed from the dataset due to limited data or differing loss profiles compared to other commodities in their categories.
Rows with missing data were dropped to improve data quality.
Notes
Loss percentage is calculated as a proportion of the total harvested quantity of the commodity.
The dataset may contain estimations and not reflect the actual losses with complete precision.
For more detailed information on each column and methodology, refer to the data source documentation.
