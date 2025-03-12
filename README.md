# NHS UK : Appointments Data Analysis

### 📋 Project Brief
I conducted an in-depth analysis of NHS UK appointment data (2020-2022) to identify service utilization patterns, assess resource capacity, and investigate missed appointments, which incur significant costs to the healthcare system.

### ✅ Objectives
The analysis supported key business objectives:
- Understanding service utilization trends and patterns
- Assessing staff and capacity adequacy across regions
- Reducing missed appointments through targeted interventions
- Evaluating the value of external data sources for decision-making

### 🎯 Conclusion
The analysis revealed significant opportunities to improve NHS appointment utilization and reduce missed appointments. Weekdays show consistent over-utilization (73% of days exceeding capacity), while weekends remain under-utilized. Face-to-face appointments account for 78% of all missed appointments, with booking intervals strongly influencing attendance rates.

**Key Recommendations:**
- Increase same-day and next-day appointments to reduce missed rates
- Expand telephone and video consultations to optimize resources
- Improve weekend utilization to relieve weekday overuse
- Implement region-specific interventions for high-miss areas
- Use automated reminders for appointments with longer booking windows
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
#### 1. Data Preparation & Cleaning

| Process | Highlights |
|---------|---------|
| **Data Import** | • Loaded multiple NHS datasets with different time ranges<br>• Consolidated appointment data across regional, national, and duration-specific sources |
| **Data Cleaning** | • Verified data consistency across the datasets<br>• Validated appointment count alignments<br>• Handled duplicate records<br>• Standardized datetime fields for analysis |
| **Data Enhancement** | • Mapped location codes to NHS organizational structure<br>• Added geographical context by linking regions, ICBs, and sub-ICBs<br>• Created derived fields for time analysis (weekday, seasons) |

#### 2. Exploratory Data Analysis

| Process | Highlights |
|---------|---------|
| **Location Analysis** | • Analyzed 7 NHS regions with 42 ICBs and 106 sub-ICBs<br>• Identified regional disparities in appointment volumes and missed rates |
| **Categorical Analysis** | • Created custom functions to analyze multiple appointment categories<br>• Examined service settings, context types, national categories, and appointment modes |
| **Temporal Analysis** | • Assessed monthly, seasonal, and COVID-related trends<br>• Identified impact of lockdown periods on appointment volumes |

#### 3. Advanced Analysis

| Component | Highlights |
|-----------|---------|
| **Missed Appointments** | • Analyzed 30.9M missed appointments (4.16% of total)<br>• Identified key correlations with appointment modes and booking intervals<br>• Quantified business impact at £1.29B over 30 months |
| **Capacity Utilization** | • Evaluated daily capacity against the 1.2M appointment benchmark<br>• Identified weekday vs. weekend utilization disparities<br>• Assessed post-COVID capacity pressures |
| **Multivariate Analysis** | • Combined mode, timing, and regional factors to identify missed appointment patterns<br>• Created region-specific insights on appointment behaviors |

---

### 🗝️ Key Insights:

**Appointment Distribution**
- Identified General Practice as the dominant service setting (91% of appointments)
- Discovered Face-to-Face (60%) and Telephone (28%) as the primary appointment modes
- Face-to-Face appointments decreased while Telephone consultations doubled during COVID
> [!IMPORTANT]
  > **Value Discovery:** 87.7% of all appointments have booking windows of 0-14 days, with same-day appointments showing the lowest missed rates across all modes

<div align="center">
  <img src="https://github.com/user-attachments/assets/bc91e35a-dba6-4859-9377-6436386a4fa0" alt="NHS Appointment Distribution" width="100%"/>
  <p><em>Distribution showing significant variations in appointment volumes and types</em></p>
</div>

**Capacity Utilization**
- Quantified weekday over-utilization with 73% of weekdays exceeding capacity
- Identified Tuesday (107.3%) and Monday (103.6%) as peak utilization days
- Measured weekend under-utilization with Saturday (9.9%) and Sunday (1.1%) showing minimal use
> [!IMPORTANT]
> **Value Discovery:** Weekend appointment expansion could significantly reduce weekday pressure, particularly following post-lockdown peak periods

<div align="center">
  <img src="https://github.com/user-attachments/assets/52ae05a0-7217-406a-97b2-aa41ae8f2646" alt="NHS Capacity Utilization" width="100%"/>
  <p><em>Utilization trends showing weekday overuse and weekend underutilization</em></p>
</div>  

**Missed Appointments**
- Quantified Missed appointments as 4.16% of all appointments over 30 months of analysis.
- Identified Face-to-Face appointments accounting for 78% of all missed appointments
- Discovered strong correlation between booking interval and missed rates
- Longer intervals showed significantly higher missed rates (9.8% for 28+ days vs. 2.0% for same-day)
> [!IMPORTANT]
> Telephone appointments consistently show lower missed rates (1.4-3.3%) across all booking intervals

<div align="center">
  <img src="https://github.com/user-attachments/assets/992b2c80-df7b-49b1-b0ae-d9a37303f43a" alt="Missed Appointments Analysis" width="100%"/>
  <p><em>Analysis of missed appointments by mode, booking interval, and region</em></p>
</div>

---
### 📊 Recommendations to NHS:

Based on the comprehensive data analysis, the following strategic recommendations were presented to enhance NHS appointment management:

**Operational Recommendations**
- Shorten booking intervals by increasing same-day and next-day appointments to reduce missed rates
- Expand remote consultations through telephone and video to capitalize on their lower missed rates
- Implement weekend utilization improvements to balance weekday over-utilization
- Deploy automated appointment reminders for bookings with intervals greater than 8 days
- Develop region-specific interventions targeting the unique patterns in high-miss areas

**Strategic Recommendations**
- Redistribute staff resources to match peak demand periods and underutilized capacity windows
- Balance face-to-face and telephone appointment availability based on regional attendance patterns
- Consider short-term staff augmentation to address post-COVID demand surges
- Improve data collection methods to enable more granular analysis in the future

**Technical Recommendations**
- Create a unified data model linking appointment-level data across all systems
- Incorporate population metrics and healthcare provider data for more comprehensive analysis
- Extend data collection timeframes to better identify seasonal patterns
- Develop advanced predictive models once post-COVID normalization periods provide more stable data
