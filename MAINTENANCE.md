**1. Is the database maintained? Who will be supporting/hosting/maintaining the database?**

Yes, MIMIC-IV is maintained by the Laboratory for Computational Physiology at the Massachusetts Institute of Technology (MIT) and BIDMC. They provide ongoing support and maintenance for the database.

**2. How can the owner/curator/manager of the database be contacted (e.g., email address)?**

For private issue, they can be contacted at `mimic-support@physionet.org` and for issues related to patient health information (PHI) `phi-report@physionet.org` is being used.

**3. Will the database be updated (e.g., to correct labeling errors, add new instances, delete instances)? If so, please describe how often, by whom, and how updates will be communicated to dataset consumers (e.g., mailing list, GitHub)?**

Yes, the MIMIC-IV database is regularly updated by the MIT Laboratory for Computational Physiology team. The latest version, v2.2, has been released, which includes updates from the previous version, v1.0. The frequency of future updates is unknown, but any information regarding updates can be found on the official [PhysioNet website](https://physionet.org/content/mimiciv/2.2/) and [GitHub](https://github.com/MIT-LCP/mimic-code).

**4. Will older versions of the database continue to be supported/hosted/maintained? If so, please describe how. If not, please describe how its obsolescence will be communicated to dataset consumers.**

Previous versions of the database will continue to be supported and maintained, however, it is not explicitly stated whether they might have any further updates by the owners.

**5. If others want to extend/augment/build on/contribute to the dataset, is there a mechanism for them to do so? If so, please provide a description.**

Content for the MIMIC website and documentation is hosted publicly on GitHub. To raise a problem or to suggest an improvement, a new issue can be created at: [GitHub Issues](https://github.com/MIT-LCP/mimic-website/issues). To take part in the discussion, use [GitHub Discussions](https://github.com/MIT-LCP/mimic-code/discussions).

### + 6. What is the Data life cycle of MIMIC database?

The life cycle of MIMIC CRD includes:

1. Data Acquisition
2. Data Archive
3. Data Preparation
4. Data loading

**Data Acquisition**

Data is collected from the source which may be internal, external, or both. Below is a breakdown of internal and external data sources:

| Internal (In-hospital) data                                   | External data source              |
|---------------------------------------------------------------|-----------------------------------|
| ICU/MICU/SICU/CCU/CVICU/NICU data (vitals, trends, anomalies) | Social Security Death Index, etc. |
| Chart details (Fluids, medications, etc.)                     |                                   |
| Demographics (age, gender, ethnicity, language, marital status, religion, insurance, etc.) | |
| Lab reports                                                   |                                   |
| Billing details                                               |                                   |
| Physician notes                                               |                                   |
| Provider order entries, etc.                                  |                                   |



**Data Archive**

Data collected from the source is Archived before proceeding with data preparation for later use.

**Data Preparation**

To ensure compliance with HIPAA regulations, measures such as de-identification, date shifts, and format conversions are applied to the archival data. The data is then reorganized into a more suitable format for retrospective analysis, which involves consolidating tables, denormalizing data, and removing audit trails. It's important to note that no data cleaning procedures were performed to maintain the authenticity of the real-world clinical dataset. Feedback from users will be considered for further iterations, and the final version of the data will be loaded into the database.

**Data loading to database**

The final version of the data is then loaded into the database, which is built on a PostgreSQL relational database management system and is hosted on a secure server infrastructure. The data can either be downloaded locally or accessed on the cloud via BigQuery, AWS, or GCS.
