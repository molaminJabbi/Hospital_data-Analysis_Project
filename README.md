# Hospital Data Analysis Project

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-blue?logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Interactive-orange?logo=jupyter&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## 📋 Overview

A comprehensive data analysis project examining hospital patient records from a Chinese healthcare facility, focusing on healthcare costs, patient demographics, and operational efficiency across multiple departments. This project demonstrates proficiency in data cleaning, exploratory data analysis (EDA), and extracting actionable insights from complex healthcare datasets.

**Dataset**: 527 patient records from a Chinese hospital across multiple departments  
**Location**: Guizhou Province, China (Anshun region)  
**Time Period**: April 2015 - February 2016  
**Currency**: Chinese Yuan (CNY/¥)  
**Primary Focus**: Cost analysis, length of stay patterns, departmental performance, and billing component breakdown

---

## 📊 Key Findings at a Glance

| Metric | Value |
|--------|-------|
| **Total Patient Records** | 527 |
| **Average Length of Stay** | 13.7 days |
| **Median Length of Stay** | 10 days |
| **Average Total Fees per Patient** | ¥3,203.99 |
| **Cost Range** | ¥396.18 - ¥23,503.40 |
| **Data Completeness** | 99.24% |
| **Primary Cost Driver** | Western Medicine (34.9%) |

### 💰 Cost Breakdown (Average per Patient)
- **Western Medicine Fees**: ¥1,117.08 (34.9%)
- **Lab Fees**: ¥518.26 (16.2%)
- **Medical Fees**: ¥511.58 (16.0%)
- **Inspection Fees**: ¥268.30 (8.4%)
- **Other Fees**: ¥229.63 (7.2%)
- **Surgery Fees**: ¥189.23 (5.9%)
- **Bed Fee**: ¥94.05 (2.9%)
- **Anesthesia Fee**: ¥83.11 (2.6%)
- **Nursing Fee**: ¥66.25 (2.1%)
- **Grass Fee (Traditional Medicine)**: ¥5.83 (0.2%)

### 🏥 Department Coverage
- Department of Obstetrics and Gynecology (multiple locations)
- Internal Medicine
- Department of Surgery
- Emergency Department
- Outpatient Services

---

## 🎯 Business Value & Insights

This analysis provides critical intelligence for:

✅ **Healthcare Administrators**  
- Identify cost optimization opportunities within each department
- Benchmark departmental performance against hospital averages
- Optimize resource allocation based on patient volume and complexity

✅ **Finance Teams**  
- Understand billing patterns and cost drivers
- Develop targeted billing optimization strategies
- Identify outlier cases for cost review

✅ **Clinical Leadership**  
- Evaluate treatment protocols relative to costs
- Make evidence-based decisions on care pathways
- Monitor patient stay duration trends by diagnosis

✅ **Quality Assurance**  
- Analyze relationships between treatment type and outcomes
- Identify opportunities for clinical pathway improvements
- Support value-based care initiatives

---

## 📁 Project Structure

```
Hospital_data-Analysis_Project/
├── hospital_data.ipynb          # Main analysis notebook with complete EDA
├── clean_dataset.csv            # Cleaned, processed dataset ready for analysis
└── README.md                    # Project documentation (this file)
```

---

## 🔍 Analysis Sections

### 1️⃣ **Data Loading & Initial Exploration**
   - Successfully imported hospital dataset with 527 records
   - 21 distinct columns covering patient demographics, clinical information, and financial data
   - Initial data structure inspection using `.info()` method

### 2️⃣ **Exploratory Data Analysis (EDA)**
   - Comprehensive statistical summary using `.describe()`
   - Identified key distributions and outliers:
     - Length of stay: Wide range (0-317 days) with 13.7 day average
     - Total fees: Significant variation indicating diverse treatment complexity
   - Analyzed patterns across all fee categories

### 3️⃣ **Data Cleaning & Preprocessing**
   - **Missing Value Handling**: Identified and documented 4 missing values in `days` column (0.76%)
   - **Datetime Standardization**: Converted admission/discharge timestamps to proper datetime objects
   - **Column Normalization**: Standardized column naming (lowercase, snake_case)
   - **Data Quality**: Achieved 99.24% completeness rate

### 4️⃣ **Cost Analysis & Breakdown**
   - Decomposed total patient fees into 10 distinct cost categories
   - Calculated percentage contribution of each cost component
   - Identified Western medicine and lab fees as top cost drivers
   - Analyzed cost variation across departments

### 5️⃣ **Patient Demographics & Patterns**
   - Analyzed birth place distribution (primarily Guizhou province and Anshun)
   - Examined admission/discharge timing patterns
   - Studied diagnoses and treatment types by department
   - Identified high-cost vs. routine cases

---

## 🛠️ Technologies & Tools

| Technology | Purpose |
|-----------|---------|
| **Python 3.x** | Core programming language |
| **Pandas** | Data manipulation, cleaning, and analysis |
| **Matplotlib** | Data visualization and charting |
| **Jupyter Notebook** | Interactive analysis and documentation |
| **NumPy** | Numerical computations (implicit via Pandas) |

---

## 📊 Dataset Specifications

### Columns & Data Types

**Patient Information:**
- `id` - Patient identifier (int64)
- `birth_place` - Patient origin location (object) - primarily Guizhou Province, China
- `department` - Hospital department (object)

**Clinical Data:**
- `discharge_diagnosis` - Primary diagnosis at discharge (object)
- `other_diagnoses_for_discharge` - Secondary/comorbid diagnoses (object)
- `outpatient_physician` - Attending physician (object)
- `outpatient_physician_department` - Physician's department (object)

**Temporal Data:**
- `admission_time` - Patient admission timestamp (datetime64[ns])
- `discharge_time` - Patient discharge timestamp (datetime64[ns])
- `days` - Length of stay in days (float64) - *4 missing values*

**Financial Data (10 categories, all in Chinese Yuan - ¥):**
- `fees` - Total patient fees (float64)
- `lab_fees` - Laboratory services (float64)
- `inspection_fees` - Diagnostic inspection (float64)
- `western_medicine_fees` - Western medication costs (float64)
- `nursing_fee` - Nursing care costs (int64)
- `grass_fee` - Traditional/herbal medicine (float64)
- `anesthesia_fee` - Anesthesia services (float64)
- `other_fees` - Miscellaneous charges (float64)
- `surgery_fees` - Surgical procedures (int64)
- `bed_fee` - Hospital bed charges (float64)
- `medical_fees` - General medical services (float64)

---

## 🚀 Getting Started

### Prerequisites
```bash
Python 3.8 or higher
pip package manager
```

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/molaminJabbi/Hospital_data-Analysis_Project.git
   cd Hospital_data-Analysis_Project
   ```

2. **Create a virtual environment (recommended)**
   ```bash
   python -m venv venv
   
   # On Windows:
   venv\Scripts\activate
   
   # On macOS/Linux:
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install pandas matplotlib jupyter openpyxl
   ```

### Running the Analysis

```bash
# Start Jupyter Notebook
jupyter notebook

# Open 'hospital_data.ipynb' in your browser and run cells sequentially
```

---

## 📈 Key Insights & Observations

### 💡 Clinical Insights
- **Obstetrics & Gynecology** departments handle significant proportion of admissions (typical for Chinese hospitals with reproductive health focus)
- **Length of Stay**: Average 13.7 days suggests mix of routine and complex cases
- **Emergency Department**: Lower LOS with varying cost profiles
- **Traditional Medicine**: Grass fee component (¥5.83 avg) reflects integration of traditional Chinese medicine in healthcare

### 💰 Financial Insights
- **Cost Concentration**: Western medicine (35%) and lab fees (16%) account for 51% of total costs
- **Cost Variation**: High standard deviation (¥2,423.88) indicates diverse case complexity
- **Outlier Cases**: Maximum fees (¥23,503.40) suggest high-complexity surgical cases
- **Surgery Fees Impact**: Highly variable (¥0-¥3,470) depending on procedure type
- **Affordable Healthcare**: Average fees of ¥3,203.99 reflect China's healthcare pricing structure

### 📊 Data Quality Observations
- **Minimal Missing Data**: Only 4 records missing length of stay (highly reliable dataset)
- **Complete Financial Records**: All fee categories recorded for every patient
- **Consistent DateTime Formats**: Proper temporal data for admission/discharge tracking
- **Geographic Consistency**: All patients from Guizhou Province region confirms single facility analysis

---

## 🔧 Technical Approach

### Data Cleaning Strategy
1. Imported raw Excel file with 527 patient records
2. Validated data types and identified inconsistencies
3. Converted datetime strings to proper datetime objects
4. Standardized column naming for reproducibility
5. Documented missing values and data quality metrics

### Analysis Methodology
- **Descriptive Statistics**: Mean, median, std deviation across all numeric features
- **Distribution Analysis**: Identified outliers and normal/skewed distributions
- **Categorical Analysis**: Examined department, diagnosis, and physician distributions
- **Cost Component Analysis**: Decomposed total fees into constituent parts

### Quality Assurance
- Verified data integrity after each transformation
- Cross-checked calculations against raw data
- Documented all assumptions and preprocessing decisions

---

## 📚 Data Dictionary

| Column Name | Description | Type | Notes |
|------------|-------------|------|-------|
| id | Unique patient identifier | int64 | 1-527 |
| department | Hospital department name | object | Multiple departments |
| birth_place | Patient's birthplace/origin | object | Primarily Guizhou region, China |
| discharge_diagnosis | Primary diagnosis at discharge | object | Medical diagnosis codes/descriptions |
| other_diagnoses_for_discharge | Secondary diagnoses | object | Comorbidities and related conditions |
| admission_time | Hospital admission date/time | datetime64 | April 2015 - Feb 2016 |
| discharge_time | Hospital discharge date/time | datetime64 | April 2015 - Feb 2016 |
| days | Length of hospital stay | float64 | 0-317 days; 4 missing values |
| fees | Total patient charges | float64 | ¥396.18 - ¥23,503.40 |
| outpatient_physician | Attending/referring physician | object | Physician name (partially masked) |
| outpatient_physician_department | Physician's primary department | object | Department assignment |
| lab_fees | Laboratory test charges | float64 | ¥23.50 - ¥2,239.50 |
| inspection_fees | Diagnostic/imaging fees | float64 | ¥0 - ¥2,012.00 |
| western_medicine_fees | Medication/pharmaceutical costs | float64 | ¥0 - ¥7,258.85 |
| nursing_fee | Nursing care charges | int64 | ¥0 - ¥969 |
| grass_fee | Traditional/herbal medicine | float64 | ¥0 - ¥396.00 |
| anesthesia_fee | Anesthesia service charges | float64 | ¥0 - ¥909.00 |
| other_fees | Miscellaneous charges | float64 | ¥5.50 - ¥15,560.52 |
| surgery_fees | Surgical procedure charges | int64 | ¥0 - ¥3,470 |
| bed_fee | Hospital bed/accommodation charges | float64 | ¥0 - ¥527.40 |
| medical_fees | General medical service charges | float64 | ¥0 - ¥9,415.00 |

---

## 🎯 Potential Extensions & Future Work

### Advanced Analytics
- 📈 **Predictive Modeling**: Build models to predict patient costs based on diagnosis and LOS
- 🔍 **Diagnosis-Specific Analysis**: Deep-dive into cost patterns by diagnosis type
- 📊 **Department Benchmarking**: Create performance scorecards for departmental comparison
- 🎯 **Treatment Outcome Analysis**: Correlate costs with patient outcomes (if outcome data available)

### Automation & Scaling
- 🔄 **Automated Reporting Pipeline**: Monthly cost analysis reports
- 📅 **Time-Series Analysis**: Trend analysis across admission periods
- 🎨 **Interactive Dashboards**: Tableau/Power BI visualizations for stakeholders
- 💾 **Database Integration**: Move from CSV to relational database for scaling

### Clinical Insights
- 🏥 **Departmental Efficiency Metrics**: Cost per patient, cost per day by department
- 🔬 **Comorbidity Analysis**: Impact of secondary diagnoses on total costs
- 📋 **Care Pathway Optimization**: Identify efficient vs. inefficient treatment protocols
- ⚠️ **Outlier Case Studies**: Deep analysis of high-cost cases for learnings

### Business Intelligence
- 💡 **Cost Optimization Strategy**: Actionable recommendations for finance
- 📊 **Revenue Cycle Analysis**: Identify billing optimization opportunities
- 🎓 **Physician Performance**: Analyze cost efficiency by physician
- 🏆 **Benchmarking Study**: Compare against Chinese healthcare standards

---

## 📝 Methodology & Assumptions

### Data Assumptions
- All cost data is in Chinese Yuan (CNY/¥)
- Dataset represents a single hospital facility in Guizhou Province, China
- Datetime fields represent actual admission/discharge times
- Diagnosis descriptions are standardized within the system
- All 527 records represent valid, completed patient episodes
- "Grass fee" refers to traditional Chinese medicine/herbal treatments

### Analysis Limitations
- **Temporal Scope**: Single year (2015-2016) - seasonal patterns require multi-year data
- **Outcome Data**: Analysis lacks patient outcome metrics (readmission, complications)
- **External Context**: No socioeconomic or insurance status data available
- **Geographic Scope**: Limited to one hospital facility in Guizhou Province
- **No Inflation Adjustment**: Cost data not adjusted for inflation across the study period

### Data Quality Notes
- 4 missing values in `days` column (0.76%) - calculated from admission/discharge times where available
- Physician names partially masked (privacy protection)
- All other fields are 100% complete
- Data sourced from hospital management system, ensuring clinical accuracy

---

## 👥 Use Cases

| User Role | Key Questions Answered |
|-----------|----------------------|
| **Hospital CFO/Finance Director** | What are our biggest cost drivers? Where can we optimize? |
| **Hospital Administrator** | How do departments compare? Where are inefficiencies? |
| **Department Head** | What's our average cost per patient? How do we benchmark? |
| **Quality Officer** | Do high-cost cases have documented clinical justification? |
| **Billing Manager** | Are there patterns in outlier charges? Billing errors? |
| **Clinical Director** | Do treatment protocols correlate with outcomes and costs? |
| **Health Policy Researcher** | What are typical costs for different diagnoses in China? |

---

## 📞 Contact & Support

**Questions or Feedback?**
- Open an [Issue](https://github.com/molaminJabbi/Hospital_data-Analysis_Project/issues) on GitHub
- Check existing issues for similar questions

**Contributions Welcome!**
- Submit pull requests with enhancements
- Suggest additional analyses or visualizations
- Improve documentation and data quality

---

## 📜 License

This project is open source and available under the **MIT License**.  
See LICENSE file for details.

---

## 🙏 Acknowledgments

- Dataset sourced from hospital records (April 2015 - February 2016)
- Guizhou Province, China healthcare facility
- Analysis performed using Python's pandas ecosystem
- Visualization created with Matplotlib

---

**Project Status**: ✅ Complete Analysis | 📅 Last Updated: August 2026

**Tags**: #HealthcareAnalytics #ChinaHealthcare #DataScience #Python #Pandas #CostAnalysis #Jupyter #EDA #GuizhouProvince
