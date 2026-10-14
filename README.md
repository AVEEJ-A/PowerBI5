# 🏥 Healthcare Data Cleaning & Star Schema Modelling using Power BI

## 📌 Project Overview

This project focuses on cleaning healthcare data and building a **Star Schema Data Model** using Microsoft Power BI. Power Query Editor is used to clean and transform healthcare records, create dimension tables, and build a central fact table for clinical data analysis.

The project prepares structured healthcare data for reporting, visualization, and analytical purposes.

## 🎯 Objectives

- Clean and transform healthcare datasets using Power Query.
- Correct data types and standardize text values.
- Remove exact duplicate records.
- Categorize patients into age groups.
- Create dimension tables for patients, doctors, hospitals, and dates.
- Build a central `FactAdmission` table.
- Establish relationships using a Star Schema model.

## 🛠️ Technologies Used

- Microsoft Power BI Desktop
- Power Query Editor
- Power BI Model View
- CSV Dataset

## 📂 Repository Contents

| File | Description |
|---|---|
| `PowerBI5 (2).pbix` | Power BI project file |
| `healthcare_data_for_task.csv` | Healthcare dataset |
| `README.md` | Project documentation |

## 📊 Dataset Information

- **Dataset:** Healthcare Dataset
- **Original Records:** 55,500 rows
- **Number of Columns:** 15

### Dataset Columns

1. Name
2. Age
3. Gender
4. Blood Type
5. Medical Condition
6. Date of Admission
7. Doctor
8. Hospital
9. Insurance Provider
10. Billing Amount
11. Room Number
12. Admission Type
13. Discharge Date
14. Medication
15. Test Results

## 🧹 Data Cleaning and Transformation

The following operations were performed using Power Query Editor:

- Loaded the healthcare CSV dataset.
- Renamed the base query to `Healthcare_Cleaned`.
- Assigned appropriate data types to all columns.
- Applied **Trim** and **Clean** operations to text columns.
- Standardized patient names using **Capitalize Each Word**.
- Removed **534 exact duplicate records**.
- Created an `AgeGroup` column.
- Standardized admission types as Emergency, Elective, and Urgent.

### Age Group Categories

| Age Range | Category |
|---|---|
| 0–17 | Pediatric |
| 18–39 | Young Adult |
| 40–59 | Middle Adult |
| 60 and above | Senior |

## ⭐ Star Schema Data Model

The project contains six tables:

| Table Name | Purpose |
|---|---|
| `Healthcare_Cleaned` | Cleaned base dataset |
| `DimPatient` | Patient details and PatientID |
| `DimDoctor` | Doctor details and DoctorID |
| `DimHospital` | Hospital details and HospitalID |
| `DimDate` | Date, year, month, month number, and quarter |
| `FactAdmission` | Admission records and measurable details |

### 🔗 Model Relationships

The `FactAdmission` table is connected to four dimension tables:

- `DimPatient[PatientID]` → `FactAdmission[PatientID]`
- `DimDoctor[DoctorID]` → `FactAdmission[DoctorID]`
- `DimHospital[HospitalID]` → `FactAdmission[HospitalID]`
- `DimDate[Date]` → `FactAdmission[Date of Admission]`

All four relationships use **one-to-many (1:*) cardinality** and **single-direction cross-filtering**.

## 📈 Key Features

- Healthcare data cleaning and preprocessing
- Duplicate record removal
- Patient demographic categorization
- Standardized admission types
- Surrogate key generation
- Fact and dimension table creation
- Star Schema modelling
- Date dimension with year, month, and quarter
- Data model preparation for clinical analytics

## 🚀 How to Run the Project

1. Install and open Microsoft Power BI Desktop.
2. Clone or download this repository.
3. Open the `PowerBI5 (2).pbix` file in Power BI Desktop.
4. If prompted, reconnect the healthcare CSV dataset.
5. To review the transformation steps, select **Home → Transform Data**.
6. Review the cleaning and transformation steps in Power Query Editor.
7. Verify the dimension tables and `FactAdmission` table.
8. Open **Model View** and verify the four relationships.
9. Confirm that the final Star Schema is configured correctly.

Alternatively, you can import the CSV dataset through **Home → Get Data → Text/CSV** and reproduce the transformations.

## 🎯 Expected Outcome

A cleaned healthcare data model with patient, doctor, hospital, and date dimensions connected to a central admission fact table.

The model is structured to support Power BI reporting, data visualization, and further clinical data analysis.

## 🎓 Learning Outcomes

- Understanding data cleaning with Power Query
- Working with healthcare datasets
- Creating fact and dimension tables
- Generating surrogate keys
- Understanding Star Schema architecture
- Creating and managing Power BI relationships
- Preparing structured datasets for analytics

## 👨‍💻 Project Information

- **Project Type:** Academic / Data Analytics Project
- **Domain:** Healthcare Data Analytics
- **Tool:** Microsoft Power BI Desktop
- **Modelling Technique:** Star Schema

## 📄 Documentation

Refer to `PowerBI_Healthcare_Star_Schema_Guide.pdf` for the detailed, step-by-step implementation guide, if available.

## 🔗 Repository Links

- **Repository:** [AVEEJ-A/PowerBI5](https://github.com/AVEEJ-A/PowerBI5)
- **Source Code and Files:** [Browse Repository](https://github.com/AVEEJ-A/PowerBI5/tree/main)
- **Issues:** [Report an Issue](https://github.com/AVEEJ-A/PowerBI5/issues)

---

⭐ If you find this project useful, consider giving the repository a star!
