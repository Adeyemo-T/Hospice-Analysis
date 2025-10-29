## Project Background

A **Hospice Facility in the United States** is currently facing the operational challenge of **high patient readmission rates**. This issue directly threatens the facility's ability to access critical funding, which is essential for maintaining and improving overall operational efficiency and patient care quality.

This project thoroughly analyzes the facility's clinical and demographic data to uncover the root causes of high readmission rates and support data-driven decision-making.

The analysis delivers actionable insights focused on the following key areas:

* **Care Performance Evaluation:** A deep dive into core metrics like **Readmission Rate**, **Discharge Efficiency**, and **Average Length of Care** to benchmark performance.
* **Patient Profile Segmentation:** Analysis of **patient demographics (age, gender)** and **Top ICD-10 Diagnoses** to identify high-risk patient groups.
* **Care Flow Analysis:** An evaluation of how patients exit care (discharged vs. died) and the factors that influence the total time patients remain in the care program.

## Data Structure & Initial Checks

### 📊 Data Overview
The analysis was conducted on a denormalized dataset compiled from several disparate hospital records, including tables for **Patient Demographics**, **Clinical Encounters**, and **Discharge Status**. The final compiled data set contained **441 patient records** and 25 variables related to care length, diagnoses, and readmission events.

### 🧹 Data Cleaning and Preparation
The raw data required significant cleaning and transformation to ensure reliable insights.

* **SQL for Integration:** Complex `JOIN` operations were used to merge records from the patient, admission, and discharge tables, ensuring each row represented a complete patient journey.
* **Missing Values:** Addressed a significant number of missing values (over 700) in the `Discharge Reason` and `Length of Stay` fields by classifying them as "Unknown" to maintain data count integrity for further analysis.
* * **Type Conversion:** Standardized all date-related columns to a uniform format to allow for accurate trend analysis and calculation of the Average Length of Care (ALOC).
* **Feature Engineering:** Calculated the **Discharge Efficiency (23%)** metric by creating a new field based on the ratio of planned vs. unplanned care exits.

## Executive Summary

The facility's **12% readmission rate** is driven by low **Discharge Efficiency (23%)** and a lack of standardized post-discharge protocols, suggesting significant operational gaps in the final stage of patient care. Analysis of patient flow reveals critical friction points, particularly among the high-risk **75+ age group** and those with dementia/cancer, who are highly vulnerable to readmission. Addressing these two core areas presents the clearest path to improving patient outcomes and securing essential funding.


* **Interactive Power BI Dashboard:** The full, interactive clinical insights dashboard can be accessed [here](https://drive.google.com/file/d/1h7tkk58PjUAU1FCY8DchzsOQoDEjJBUH/view?usp=drivesdk).

![Image](https://github.com/user-attachments/assets/cb09118a-5d32-4f9b-81af-4b7fa5b68baa)

### Care Performance & Flow

* **Low Discharge Efficiency:** At **23%**, discharge efficiency is critically low, indicating a major bottleneck in standardizing the completion of care. This friction point is the largest contributor to poor overall performance.
* **Average Length of Care (ALOC):** The ALOC sits at **84 days**. While this duration is within expected ranges, the goal must be to ensure the quality of care provided during this time directly correlates with successful patient outcomes (i.e., planned discharges) rather than readmission.
* **Exit Status:** Analysis of how patients exit the program shows that a clear understanding of the full patient journey is needed to distinguish between planned discharges and high-risk unplanned exits.

   ![Image](https://github.com/user-attachments/assets/3957b2ee-7cb5-485d-ab9b-76815cce2f33)

### Patient Profile Deep Dive

* **Highest-Risk Demographic:** Patients in the **75-84 age bracket** constitute the largest demographic group. This high concentration of elderly patients demands targeted care management and robust, specialized post-discharge plans.
* **Top Diagnostic Categories:** **Dementia** and **Cancer** are the most common primary diagnoses. These complex, chronic conditions are known drivers of readmission, necessitating highly coordinated, interdisciplinary care plans.
* **Vulnerable Groups:** Proactive intervention should focus on the intersection of the 75+ age group and these chronic diagnoses, as they represent the most vulnerable population segments.

  ![Image](https://github.com/user-attachments/assets/9a9b3efa-834f-4c31-9944-6aa6a7b5f841)
  
### Business Recommendations

Based on the uncovered insights, the following recommendations are provided to reduce readmission and improve operational efficiency:

* **Implement a Structured Post-Discharge Plan:** Immediately establish a standardized post-discharge process. This includes using telehealth or home visits for follow-up checks on high-risk, elderly patients during the critical first week after discharge.
* **Audit and Improve Discharge Processes:** Launch a formal investigation into the critically low **23% discharge efficiency**. The goal is to create clear discharge checklists and procedures to reduce friction and improve patient success rates.
* **Target High-Risk Groups:** Develop tailored care protocols and support for patients aged **75+** with **Dementia/Cancer** diagnoses, as they are statistically the most vulnerable to unplanned readmission.
* **Address Data Gaps:** Improve the documentation process within the EMR system to reduce the high number of "Unknown" entries for length of stay and discharge reasons.


