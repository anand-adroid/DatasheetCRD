**1. What is the composition of the database?**

MIMIC IV database is grouped into four modules: **MIMIC IV (hosp, and icu)** , **MIMIC IV-ED (ed)**, **MIMIC IV-Note (note)** and **MIMIC-CXR (cxr)**

**MIMIC IV**

+  **Hosp** module grants access to diverse data extracted from the hospital's electronic health record system, including patient and admission details, laboratory measurements, microbiology information, medication administration records, and billed diagnoses. These data are organized in the form of tables, including patient and admission-related tables (patients, admissions, transfers), laboratory measurement tables (labevents, d_labitems), microbiology culture table (microbiologyevents), provider order tables (poe, poe_detail), medication administration tables (emar, emar_detail), medication prescription tables (prescriptions, pharmacy), and hospital billing information tables (diagnoses_icd, d_icd_diagnoses, procedures_icd, d_icd_procedures, services).

+  **ICU** module contains information collected from the clinical information system (BIDMC: MetaVision (iMDSoft)) used within the ICU. Documented data includes intravenous administrations, ventilator settings, and other charted items. Data documented in the icu module includes intravenous and fluid inputs (inputevents), ingredients of the aforementioned inputs (ingredientevents), patient outputs (outputevents), procedures (procedureevents), information documented as a date or time (datetimeevents), and other charted information (chartevents).

**MIMIC IV-ED**\
\
The **ED** module of MIMIC IV-ED focuses on emergency department patients and encompasses information regarding reasons for admission, triage assessments, vital signs, and medication reconciliation. The subject_id and hadm_id identifiers within MIMIC-IV-ED allow for linkage with other MIMIC-IV modules.\
\
**MIMIC IV-Note**\
\
The **Note** module contains deidentified free-text clinical notes for hospitalized patients.\
\
**MIMIC IV-CXR**\
\
The **CXR** module of MIMIC IV-CXR provides lookup tables that establish connections between patient identifiers and MIMIC-CXR study_id and dicom_id, facilitating the analysis of patient chest x-rays in conjunction with clinical data from other MIMIC-IV modules.    \
\
**_+ 2. How is the data arranged within each modules and for what purpose?_**

The data within each module is structured in the form of tables, as MIMIC is a well-organized relational database. Each table within a module represents a specific type of data. Within each table, the data is organized into rows and columns. Each row corresponds to a particular patient or event, while each column represents a specific variable or attribute corresponding to that row. This organized structure allows researchers to efficiently extract customized datasets tailored to their research inquiries and facilitates the construction of machine learning models.

**_+ 3. Can the modules be linked together to create specific dataset for specific tasks?_**

**Yes**. The tables within a module can be connected to other tables within the same module or across different modules using unique identifiers.
