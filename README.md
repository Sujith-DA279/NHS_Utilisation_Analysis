# NHS UK : Appointments Data Analysis

### 📋 Project Brief
I conducted an in-depth analysis of NHS UK appointment data spanning 30 months (742.8M appointments) to identify service utilization patterns, assess resource capacity, and investigate missed appointments. Using Python, pandas, and statistical analysis techniques, I delivered actionable insights on appointment management.

### ✅ Objectives & Analytical Approach
The analysis addressed key business needs through advanced data techniques:
- **Service Utilization Analysis**: Applied temporal pattern detection and trend analysis across 7 regions, 42 ICBs, and 106 sub-ICBs
- **Capacity Assessment**: Developed custom utilization metrics based on NHS benchmark of 1.2M daily appointments
- **Missed Appointment Investigation**: Created multivariate analysis combining appointment modes, booking intervals, and regional factors
- **External Data Evaluation**: Analyzed Twitter data to assess sentiment and public communication opportunities

### 🎯 Key Findings & Business Impact
The analysis revealed significant optimization opportunities through statistical pattern identification. **Weekdays show consistent over-utilization (73% days exceeded daily capacity)**, while weekends remain under-utilized. **Face-to-face appointments** account for 78% of all missed appointments (DNA), with booking intervals strongly correlated to attendance rates (up to 4.9x difference).

**Data-Driven Recommendations:**
- Optimize booking intervals based on statistical missed appointment patterns (2.0% same-day vs. 9.8% for 28+ days)
- Expand telephone consultations that show consistent 2.5% lower missed rates across all booking windows
- Implement targeted weekend capacity to address 103%+ weekday utilization vs. 9.9%/1.1% weekend use
- Deploy region-specific strategies for high-miss areas (London's 11%+ Face-to-Face DNA rate)
- Implement automated reminder system for appointments with booking intervals >8 days
---

### Project Overview:
<div>
  <table>
    <tr align="center">
      <th align="center">⏱️ Duration</th>
      <th align="center">🏆 Grade</th>
      <th align="center">🛠️ Tools</th>
      <th align="center">📊 Datasets</th>
    </tr>
    <tr>
      <td align="center"><b>6 Weeks</b></td>
      <td align="center"><b>93% (High Distinction)</b></td>
      <td align="center">
        <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white">
        <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white">
        <img src="https://img.shields.io/badge/Seaborn-4EABE5?style=for-the-badge&logo=python&logoColor=white">
      </td>
      <td align="center">
        <b>30 months</b> of appointment data<br>
        <b>742.8M</b> appointments analyzed
      </td>
    </tr>
  </table>
</div>

---

### Analytical Approach:
#### 1. Data Preparation & Engineering

| Process | Highlights & Technical Implementation |
|---------|---------|
| **Data Import & Validation** | • Loaded multiple NHS datasets using pandas (ar, nc, ad) with different time ranges<br>• Performed dataset validation with `.info()`, `.describe()`, `.shape()` functions<br>• Created cross-dataset appointment count verification between regional and national sources |
| **Data Cleaning** | • Identified and analyzed 21,604 duplicates using `.duplicated()` method<br>• Handled datetime conversions with `pd.to_datetime()` for appointment dates<br>• Created comprehensive data quality checks for missing values with `.isna().sum()` |
| **Location Mapping** | • Implemented granular location mappings with `pd.merge()` on reference code columns<br>• Connected region, ICB, and sub-ICB relationships using external location datasets<br>• Used NHS reconfiguration data to map 106 sub-ICBs to 42 integrated care boards and 7 regions |
| **Feature Engineering** | • Created weekday extraction using `.dt.strftime('%A')` and categorical ordering<br>• Developed custom `assign_season()` function to categorize months into seasons<br>• Applied `pd.Categorical()` with custom ordering for chronological season analysis |

#### 2. Exploratory Data Analysis & Custom Functions

| Process | Technical Implementation |
|---------|---------|
| **Custom Analysis Functions** | • Developed reusable `analyze_category()` function for standard statistical analysis across multiple dimensions<br>• Created parameterized helper functions for consistent data formatting with `style.format()` and `background.gradient()`<br>• Implemented data validation functions to ensure cross-dataset alignment |
| **Distribution Analysis** | • Applied `.groupby()`, `.pivot_table()`, and `.agg()` operations for multi-level aggregations<br>• Utilized `nunique()` function to identify location breakdown patterns<br>• Created flattened aggregation dataframes with sorted value ordering |
| **Temporal Analysis** | • Implemented month-by-month trend analysis using pandas datetime aggregation<br>• Applied pandas datetime accessors for date component extraction<br>• Analyzed seasonal patterns through custom grouping and aggregation<br>• Used chronological visualization techniques with annotations for COVID-19 lockdown periods |

#### 3. Advanced Statistical Analysis & Multivariate Modeling

| Component | Technical Implementation |
|-----------|---------|
| **Missed Appointment Analysis** | • Developed multi-factor groupby operations with complex aggregation functions<br>• Created univariate analytical subsets using Boolean filtering and lambda functions<br>• Built correlation analysis between appointment modes and booking intervals<br>• Calculated financial impact using NHS cost metrics and appointment volume analysis |
| **Capacity Utilization Modeling** | • Designed capacity utilization calculation based on NHS benchmarks<br>• Created separate weekday/weekend analysis with statistical outlier detection<br>• Implemented boxplot analysis for outlier identification<br>• Developed daily, monthly, and seasonal utilization trends with extrapolated capacity estimates |
| **Region-Specific Analysis** | • Built multi-level categorical breakdowns with customized aggregation functions<br>• Implemented statistical comparison between regions, ICBs, and sub-ICBs<br>• Developed outlier analysis for region-specific attendance patterns<br>• Applied complex filtering with chained Boolean operations to isolate specific regional patterns |

---

### 🗝️ Key Insights:

**Data Structure & Appointment Distribution**
- Analyzed datasets spanning different timeframes: appointments_regional (30 months), national_categories (11 months), and actual_duration (7 months)
- Identified General Practice as the dominant service setting (91% of appointments)
- Discovered Face-to-Face (60%) and Telephone (28%) as the primary appointment modes
- Tracked the shift from Face-to-Face to Telephone, with telephone consultations doubling during COVID
- Developed custom category analysis functions to systematically examine 16 national appointment categories
> [!IMPORTANT]
  > **Value Discovery: 87.7% of all appointments have booking windows of 0-14 days, with same-day appointments showing consistently lowest missed rates across all modes (2.0% for Face-to-Face vs. 9.8% for 28+ day bookings)**

<div align="center">
  <img src="https://github.com/user-attachments/assets/bc91e35a-dba6-4859-9377-6436386a4fa0" alt="NHS Appointment Distribution" width="100%"/>
  <p><em>Distribution showing significant variations in appointment volumes and types</em></p>
</div>

**Capacity Utilization**
- Quantified weekday over-utilization with 73% of weekdays exceeding capacity
- Identified Tuesday (107.3%) and Monday (103.6%) as peak utilization days
- Measured weekend under-utilization with Saturday (9.9%) and Sunday (1.1%) showing minimal use
- Developed custom utilization rate calculations based on the NHS benchmark of 1.2M appointments/day
> [!IMPORTANT]
> **Value Discovery: Weekend appointment expansion could significantly reduce weekday pressure, particularly following post-lockdown peak periods of up to 125% utilization**

<div align="center">
  <img src="https://github.com/user-attachments/assets/52ae05a0-7217-406a-97b2-aa41ae8f2646" alt="NHS Capacity Utilization" width="100%"/>
  <p><em>Utilization trends showing weekday overuse and weekend underutilization</em></p>
</div>  

**Missed Appointments**
- Identified Face-to-Face appointments accounting for 78% of all missed appointments
- Discovered strong correlation between booking interval and missed rates
- Longer intervals showed significantly higher missed rates (9.8% for 28+ days vs. 2.0% for same-day)
- Calculated business impact of missed appointments at £1.29B over 30 months (£43.28M per month)
> [!IMPORTANT]
> **Telephone appointments consistently show lower missed rates (1.4-3.3%) across all booking intervals, despite doubling in volume post-COVID**

<div align="center">
  <img src="https://github.com/user-attachments/assets/992b2c80-df7b-49b1-b0ae-d9a37303f43a" alt="Missed Appointments Analysis" width="100%"/>
  <p><em>Analysis of missed appointments by mode, booking interval, and region</em></p>
</div>

---
### 📊 Recommendations to NHS:

Based on the comprehensive data analysis, the following strategic recommendations were presented to enhance NHS appointment management:

**Operational Recommendations**
- Reduce booking intervals for Face-to-Face appointments: Statistical analysis shows 2.0% DNA rate for same-day vs. 9.8% for 28+ days
- Optimize appointment distribution: Increase 1-day appointments (currently only 1.33M/month vs. 5.36M same-day)
- Implement weekend capacity utilization: Weekend utilization data shows only 9.9% (Saturday) and 1.1% (Sunday) vs. 103%+ on weekdays
- Target high-impact regions: Midlands, London, North West and North East & Yorkshire account for 62% of missed appointments
- Deploy automated reminders for appointments with booking intervals greater than 8 days, where missed rates increase significantly

**Strategic Recommendations**
- Redistribute staff resources based on daily utilization patterns: Data shows Tuesday (107.3%) and Monday (103.6%) as highest demand days
- Promote telephone consultations: Analysis confirms consistently lower miss rates (1.4-3.3%) across all booking intervals
- Implement region-specific strategies: London shows 11%+ missed rates for face-to-face appointments while performing better with telephone
- Balance capacity across regions: Midlands manages 57.4M appointments (5.21M monthly average) vs. North West at 35.9M (3.26M monthly)
- Address post-COVID backlogs: Data shows 125% utilization peaks after lockdown periods requiring targeted intervention

**Technical Recommendations**
- Create a unified data model: Current analysis limited by inability to merge datasets at individual appointment level
- Enhance data collection: Improve segregation of healthcare professional types and geographic data points
- Implement advanced predictive modeling: Extend time series data beyond COVID recovery period for seasonal pattern identification
- Conduct granular geographic analysis: Identify and study high-performing vs. high-risk locations to reveal localized patterns
- Incorporate population demographics: Add metrics on age, major illnesses, and provider-to-patient ratios to enable deeper insights
