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

### + 2. How is the data arranged within each modules and for what purpose?

The data within each module is structured in the form of tables, as MIMIC is a well-organized relational database. Each table within a module represents a specific type of data. Within each table, the data is organized into rows and columns. Each row corresponds to a particular patient or event, while each column represents a specific variable or attribute corresponding to that row. This organized structure allows researchers to efficiently extract customized datasets tailored to their research inquiries and facilitates the construction of machine learning models.

### + 3. Can the modules be linked together to create specific dataset for specific tasks?

**Yes**. The tables within a module can be connected to other tables within the same module or across different modules using unique identifiers.

### + 4. Explain in detail the tables presented in each module?

<a href="https://raw.githubusercontent.com/anand-adroid/Datasheet_for_CRD.io/main/Datasheet_tables.pdf" download="Datasheet_tables.pdf">Download Table</a>


### + 5. Can/How the dataset be/are created from the MIMIC database?

The MIMIC database is a comprehensive clinical research database that encompasses various types of data, such as patient admissions, ICU records, triage information, bedside health records, X-rays, and clinician medical notes. It offers researchers the flexibility to create custom datasets tailored to their specific research tasks.

For example, if the objective is to predict **heart failure**, relevant cohorts related to heart failure can be extracted from tables like admission, patient, diagnoses_icd, and d_icd_diagnoses in the hosp module. Additional features associated with heart failure can be obtained by linking tables from the ICU module and ED module. Once the cohort and their corresponding heart-related features are extracted, they undergo pre-processing and cleaning before being represented in either a time series or non-time series format, depending on the prediction task. This allows for the creation of suitable datasets for predictive modeling. Similarly, researchers can curate a wide range of task-specific datasets based on their specific needs.

**6. What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)?**

A dataset derived from the MIMIC contains patient health data. The data can be patient demography (Age, gender, ethnicity, language etc.), ICU details, X-ray images, or even Clinician notes. It differs depending on the intended prediction task.

**7. How many instances are there in total (of each type, if appropriate)?**

Dataset is extracted from the MIMIC database based on the intended task, and count of instances depend on the dataset extracted.

For instance, If we intend to create a *MIMIC IV ED dataset* by linking ED, hosp and ICU modules then the dataset will have *425087* instances. Similarly several complex datasets can be created and the instance of the dataset vary depending on the prediction task/requirements.

**8. Does the dataset/database contain all possible instances or is it a sample (not necessarily random) of instances from a larger set? If the dataset is a sample, then what is the larger set? Is the sample representative of the larger set (e.g., geographic coverage)? If so, please describe how this representativeness was validated/verified. If it is not representative of the larger set, please describe why not (e.g., to cover a more diverse range of instances, because instances were withheld or unavailable).**

The MIMIC-IV database is a subset of deidentified electronic health records (EHRs) obtained from patients admitted to BIDMC between 2008 and 2019. It is a curated collection that has undergone validation and quality assurance by a team of interdisciplinary experts. The database includes a diverse range of patients and diagnoses, making it suitable for various research purposes. However, it is important to acknowledge that the dataset is not comprehensive, as it represents a subset of the overall patient population. Researchers should be mindful of potential biases inherent in the dataset and employ appropriate methods to address them when conducting analyses or studies[^1].
[^1]:(https://mimic.mit.edu/)

**9. What data does each instance consist of? “Raw” data (e.g., unprocessed text or images) or features? In either case, please provide a description.**

MIMIC IV (hosp and ICU module) and MIMIC-IV-ED (ED module) consists of raw unprocessed text, Date time and number data in comma-separated format of the patients admitted to the hospital, ICU, and ED. Whereas, MIMIC-CXR and MIMIC-Note contains images of the Chest X-Rays and free-text clinical notes for hospitalized patients respectively. <a href="https://raw.githubusercontent.com/anand-adroid/Datasheet_for_CRD.io/main/Datasheet_tables.pdf" download="Datasheet_tables.pdf">Table</a>

provides detailed feature information of the data.

**10. Is there a label or target associated with each instance? If so, please provide a description.**

The choice of the target variable in the MIMIC dataset depends on the specific prediction task at hand. For example, if the goal is to predict the length of stay in the ICU, the *los* attribute in the *icustay* table can serve as the target variable. On the other hand, if the objective is to predict *in-hospital mortality*, the *hospital_expire_flag* in the *admissions* table can be used as the target variable. **The selection of the target variable is contingent upon the specific prediction task being undertaken**.

**11. Are there recommended data splits (e.g., training, development/validation, testing)?**

No

**12. Are there any errors, sources of noise, or redundancies in the database? If so, please provide a description.**

Our analysis of the MIMIC IV dataset has revealed several biases and inconsistencies that researchers should be aware of,

+   **Inconsistencies in patient details:** Patient language is inconsistently recorded, with only English being specified while other languages are marked as '?' or unknown.
+    **Inconsistencies in in-hospital expiry information:** The admission table contains multiple reports of the same patient's death, leading to inconsistencies.
+    **Vagueness in insurance coverage information:** The dataset lacks definitive information about insurance coverage, limiting researchers' ability to draw conclusions on insurance choices.
+    **Inconsistencies in hospital admit and discharge timestamps:** The admission table exhibits inconsistencies in the recorded timestamps, and there are also *missing values for death time*.
+    **Potential representation bias in the dataset:** The database owners acknowledge the potential for bias, particularly since the data is derived from a single hospital system and may not be *representative of the entire population*.

The data in the [database](https://physionet.org/content/mimiciv/2.2/) is collected during routine clinical practice, reflecting the specific practices of the hospital. It is important to note that there may be implausible values present in the database due to the archival process[^1]. Therefore, caution should be exercised when using the data, and researchers should be mindful of the dataset limitations and potential biases.

We strongly recommend that researchers adhere to best practice [guidelines](https://www.ahajournals.org/doi/full/10.1161/01.CIR.101.23.e215) when analyzing the data

**13. Does the database contain data that might be considered confidential (e.g., data that is protected by legal privilege or by doctor– patient confidentiality, data that includes the content of individuals’ non-public communications)?**

Yes, the MIMIC IV dataset includes medical records of patients, encompassing confidential personal and health-related information. However, the dataset is constructed with patient privacy as a priority, and all data within the database undergoes de-identification processes to comply with Health Insurance Portability and Accountability Act (HIPAA) regulations.

**14. Does the database identify any subpopulations (e.g., by age, gender)?**

Yes. Database (specifically admission and patient tables) has patient demographic data such as age, gender, ethnicity, language, insurance, and marital status.

### MIMIC IV Distribution statistics

 **Admission distribution statistics**

| Description               | Value     |
|---------------------------|-----------|
| Total records             | 180,733   |
| Male                      | 47%       |
| Female                    | 53%       |
| Min Age                   | 18        |
| Max Age                   | 91        |
| Predominant Ethnicity     | White (67.2%) |

**Patient distribution statistics**

| Description               | Value     |
|---------------------------|-----------|
| Total records             | 299,712   |
| Male                      | 47%       |
| Female                    | 53%       |
| Min Age                   | 18        |
| Max Age                   | 91        |

**ED table distribution statistics**

| Description               | Value     |
|---------------------------|-----------|
| Total records             | 299,712   |
| Male                      | 46%       |
| Female                    | 54%       |
| Predominant Ethnicity     | White (58%) |
| Predominant Disposition   | Home      |

**15. Is it possible to identify individuals (i.e., one or more natural persons), either directly or indirectly (i.e., in combination with other data) from the database? If so, please describe how.**

No, all data in the database is de-identified in accordance with HIPAA regulations.

**16. Does the dataset contain data that might be considered sensitive in any way (e.g., data that reveals race or ethnic origins, sexual orientations, religious beliefs, political opinions or union memberships, or locations; financial or health data; biometric or genetic data; forms of government identification, such as social security numbers; criminal history)?**

Yes, database recorded demographic information like ethnicity, gender, age, marital status, language and insurance

### 17. + Does researchers have to take any important measures to handle the data with care?

To ensure patient privacy, researchers are required to comply data usage agreements mandated in [Physionet](https://physionet.org/content/mimiciv/2.2/)  and obtain the necessary approvals and certifications before accessing the dataset. Researchers working with healthcare-related data have a responsibility to handle the data carefully and ethically, taking measures to prevent any potential harm or dissatisfaction. While the data is de-identified in accordance with HIPAA regulations, it is crucial to treat the data with respect and caution, following best practices. Additionally, the collection of patient information and the creation of the research resource have been approved by the Institutional Review Board of the Beth Israel Deaconess Medical Center.




