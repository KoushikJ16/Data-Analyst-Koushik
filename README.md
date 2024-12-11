# Data-Analyst-Koushik
## Exploratory Data Analysis

### Project Description:
Exploratory Data Analysis (EDA) on Building Permits Dataset

### Project Title:
Understanding the Distribution of Low-Density Housing Permits in Vancouver

### Objective:
To analyze the distribution of building permits issued for Low-Density Housing across different months in 2024 and uncover trends and seasonal patterns in construction activities.

### Dataset:
The dataset contains details about building permits issued by the City of Vancouver in 2024, including the following fields:
- `yearmonth`: Month and year of permit issuance
- `permitcategory`: Category of the permit (e.g., Low-Density Housing)
- `specificusecategory`: Specific use of the permit (e.g., Residential)
- `permitnumber`: Unique identifier for each permit

### Methodology:
#### Data Collection and Preparation:
1. **Ingestion:**
   - Uploaded the raw dataset to an Amazon S3 bucket named `ibp-raw-kou`.
   - Identified critical fields (`yearmonth`, `permitcategory`, `specificusecategory`) for the analysis.
2. **Profiling:**
   - Used AWS Glue DataBrew (`ibp-prf-job-kou`) to assess data completeness and identify duplicates or anomalies.
3. **Cleaning:**
   - Removed irrelevant columns and filtered data to retain permits related to Low-Density Housing issued in 2024.
   - Ensured no null or missing values in key fields.

#### Analysis:
4. **Data Pipeline Design:**
   - Designed an ETL pipeline in AWS Glue Studio to group data by `yearmonth`.
   - Counted permits issued for each month.
   - Exported aggregated data to an S3 bucket in CSV format.

### Tools and Technologies:
- AWS S3 for data storage
- AWS Glue Studio for ETL pipeline
- AWS Glue DataBrew for profiling and cleaning
- Python for additional data validation

### Deliverables:
- CSV file containing monthly trends of Low-Density Housing permits.
- Visualizations summarizing seasonal construction activity peaks.

### Insights and Findings:
- Identified months with high and low construction activity, enabling stakeholders to understand seasonal patterns in permit issuance.

---

## Descriptive Analysis

### Project Description:
Descriptive Analysis of Building Permits in Vancouver

### Project Title:
Geographical Distribution of Building Permits Issued in Vancouver

### Objective:
To calculate the percentage distribution of building permits issued across different geographical areas in 2024, highlighting regions with the most and least construction activity.

### Dataset:
The dataset includes geographical and categorical details of permits issued in Vancouver in 2024, including:
- `geolocalarea`: Geographic location of the permit
- `permitcategory`: Permit type
- `yearmonth`: Month and year of permit issuance
- `permitnumber`: Unique identifier for each permit

### Methodology:
#### Data Collection and Preparation:
1. **Ingestion:**
   - Loaded data into an Amazon S3 bucket.
   - Focused on fields like `geolocalarea`, `permitcategory`, and `yearmonth`.
2. **Profiling:**
   - Verified data integrity using AWS Glue DataBrew.
   - Checked for null or invalid entries in `geolocalarea`.
3. **Cleaning:**
   - Removed columns irrelevant to geographical analysis.
   - Filtered rows to retain only permits issued in 2024.

#### Analysis:
4. **Data Pipeline Design:**
   - Grouped data by `geolocalarea`.
   - Counted permits for each area and calculated the percentage distribution.
   - Exported results to an S3 bucket in CSV format.

### Tools and Technologies:
- AWS S3 for data storage
- AWS Glue DataBrew for data profiling
- AWS Glue Studio for pipeline design
- Tableau for visualizing geographical distribution

### Deliverables:
- CSV file showing percentage distribution of permits by area.
- Interactive dashboard visualizing geographical construction activity.

### Insights and Findings:
- Identified regions with the highest construction activity, aiding urban planners and stakeholders in resource allocation.
