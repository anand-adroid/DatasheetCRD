**1. How was the data associated with each instance acquired? Was the data directly observable (e.g., raw text, movie ratings), reported by subjects (e.g., survey responses), or indirectly inferred/derived from other data (e.g., part-of-speech tags, model-based guesses for age or language)? If the data was reported by subjects or indirectly inferred/derived from other data, was the data validated/verified? If so, please describe how.**

The data was extracted from the hospital databases of the Beth Israel Deaconess Medical Center (BIDMC) specifically for patients admitted to the intensive care units. A comprehensive patient list was compiled, including all medical record numbers associated with ICU or emergency department admissions from 2008 to 2019. To ensure the reliability of the database, a multidisciplinary team of scientists and clinicians thoroughly evaluated MIMIC-IV during its development, conducting code reviews and documenting any identified issues using a ticket system [^1]

[^1]:[MIMIC](https://www.nature.com/articles/s41597-022-01899-x)

**2. What mechanisms or procedures were used to collect the data (e.g., hardware apparatuses or sensors, manual human curation, software programs, software APIs)? How were these mechanisms or procedures validated?**

MIMIC-IV is derived from two distinct database systems within the hospital setting: a customized *electronic health record (EHR)* used across the entire hospital and a specialized clinical information system called *MetaVision (iMDSoft)* specifically designed for the intensive care units at the Beth Israel Deaconess Medical Center (BIDMC). 

To ensure the accuracy and reliability of the MIMIC-IV dataset, a diverse team of scientists and clinicians conducted a comprehensive evaluation during its development, which included code reviews and the systematic documentation of identified issues using a ticket system [^1].

**3. Over what timeframe was the data collected? Does this timeframe match the creation timeframe of the data associated with the instances (e.g., recent crawl of old news articles)? If not, please describe the timeframe in which the data associated with the instances was created.**

Over a period of *11 years, from 2008 - 2019*

**4. Were any ethical review processes conducted (e.g., by an institutional review board)?**

Yes, the collection of patient information and creation of the research resource was reviewed by the *Institutional Review Board at the Beth Israel Deaconess Medical Center*.

**5. Did you collect the data from the individuals in question directly, or obtain it via third parties or other sources (e.g., websites)?**

Data is collected from hospital EHR and ICU specific clinical information system at the BIDMC called *CareVue and MetaVision (iMDSoft)*.

**6. Has an analysis of the potential impact of the dataset and its use on data subjects (e.g., a data protection impact analysis) been conducted? If so, please provide a description of this analysis, including the outcomes, as well as a link or other access point to any supporting documentation.**

Unknown, however the MIMIC data is deidentified and patient identifiers were removed according to the Health Insurance Portability and Accountability Act (HIPAA) Safe Harbor provision [^1].
