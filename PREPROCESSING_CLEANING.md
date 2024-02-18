**1. Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging,
SIFT feature extraction, removal of instances, processing of missing values)? If so, please provide a description. If not, you may skip the
remaining questions in this section.**

The data within the MIMIC-IV database underwent reorganization to enhance its suitability for retrospective data analysis. This involved denormalizing tables, eliminating audit trails, and consolidating the data into a smaller number of tables. The primary objective of this process was to simplify the retrospective analysis of the database. Notably, no data cleaning procedures were applied to ensure that the dataset accurately represents real-world clinical data.

To protect patient privacy, patient identifiers were removed in compliance with HIPAA regulations. Random ciphers were used to replace patient identifiers, resulting in deidentified integer values for patients, hospitalizations, and ICU stays. Structured data underwent filtering using look-up tables and allow lists. Additionally, dates and times were randomly shifted into the future by a specific number of days. Consequently, the data for each individual patient remains internally consistent [^1].

[^1]:[MIMIC](https://www.nature.com/articles/s41597-022-01899-x)


**2. Is the software that was used to preprocess/clean/label the data available? If so, please provide a link or other access point.**

Unknown. However, authors have stated that the application of a free-text deidentification algorithm was used as a measure to remove personally identifiable information (PHI) from the free-text data, if needed.
