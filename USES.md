**_1. Has the database/dataset been used for any tasks already? If so, please provide a description._**

Yes, the MIMIC database is one of the most widely used Critical Research Databases (CRD). It has been extensively utilized for various types of works, such as:

1. **Prediction tasks like,**
   - **Mortality** - Predict the likelihood of patients dying.[^1][^2][^3]
     - **In-hospital** - Predict the likelihood of patient dying in hospital while they are admitted (helpful to identify high risk patients early on to provide medical interventions).[^4][^5]
     - **Short term** - Predict short-term mortality (typically within 2-3 days) after ICU admission.[^6][^7]
     - **Long term** - Predict long-term mortality (typically within 30 days to 1 year) after hospital discharge.[^8][^9]
   - **Length of stay (LOS)** - Predict the length of stay of each admission (typically predicting > 3 and 7 days stay. Custom days is also being predicted.)[^10]
   - **Readmission** (30, 60, 90, 120, and custom days) - Predict patients at risk of readmission early in the health care process (helps to prioritize care towards such patients preventing mortality and readmission).[^11]
   - **Phenotype label and ICD-9/10 code grouping** - Helpful in tasks like disease prediction, outcome analysis, treatment recommendation, and customized treatments.
     - **Phenotype labelling** - Classify patients into specific groups based on their diagnoses, procedures, medications, and other clinical variables.[^12]
     - **Grouping ICD 9/10 codes** - Into different categories based on patient diagnosis to classify the disease.[^13]

2. **Prediction for specific health ailments like,**
   - Heart failure[^14]
   - Chronic Kidney Disease (CKD)[^15]
   - Chronic obstructive pulmonary disease (COPD)[^16]
   - Coronary artery disease (CAD)[^17]
   - Sepsis[^18]
   - Cancer[^19]
   - Ventilation failure[^20]

[^1]:[1](https://link.springer.com/article/10.1186/s12911-020-01271-2)
[^2]:[2](https://www.sciencedirect.com/science/article/pii/S1532046419301881)
[^3]:[3](https://link.springer.com/article/10.1007/s12652-020-02456-3)
[^4]:[4](https://www.cell.com/heliyon/pdf/S2405-8440(23)00407-3.pdf)
[^5]:[5](https://www.hindawi.com/journals/bmri/2021/6638919/)
[^6]:[6](https://www.sciencedirect.com/science/article/pii/S0147956322000875?casa_token=STzPJK32rBwAAAAA:0F4gtqUX_R9YqTMsEhsB_ODQQGcdmH6aHNhfOe5kM_vgoAKgyBIuVkxV2Ei4VWJKCTYr3gCDjw)
[^7]:[7](https://journals.plos.org/plosone/article?id=10.1371/journal.pone.0265758)
[^8]:[8](https://www.frontiersin.org/journals/neurology/articles/10.3389/fneur.2021.678998/full)
[^9]:[9](https://link.springer.com/article/10.1007/s12652-020-02456-3)
[^10]:[10](https://link.springer.com/article/10.1007/s11739-023-03199-7)
[^11]:[11](https://jaredthacker.com/report_tmp.pdf)
[^12]:[12](https://academic.oup.com/jamia/article/30/2/367/6839857?login=false)
[^13]:[13](https://ojs.aaai.org/index.php/AAAI/article/view/6331)
[^14]:[14](https://www.sciencedirect.com/science/article/pii/S0002870322002642?casa_token=iRWCyiF0-BQAAAAA:mXaQo_dGLlqUIZtpCS3zr_PiEdNpSskLpfbIQ77pXJV7fvRzHzDo8bkh2LudZpMPcDoBRV8_aQ)
[^15]:[15](https://translational-medicine.biomedcentral.com/articles/10.1186/s12967-022-03364-0)
[^16]:[16](https://bmcpulmmed.biomedcentral.com/articles/10.1186/s12890-021-01526-2)
[^17]:[17](https://eurjmedres.biomedcentral.com/articles/10.1186/s40001-023-00995-x)
[^18]:[18](https://translational-medicine.biomedcentral.com/articles/10.1186/s12967-022-03364-0)
[^19]:[19](https://ieeexplore.ieee.org/abstract/document/9108225)
[^20]:[20](https://www.mdpi.com/2077-0383/10/17/3824)


**_2. Is there a repository that links to any or all papers or systems that use the database/dataset? If so, please provide a link or other access point._**

No specific repository links to all papers or systems that use the database. However, the [MIT-LCP/mimic-code](https://github.com/MIT-LCP/mimic-code) repository on GitHub hosts code and discussions related to the database.

**_3. Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses? For example, is there anything that a dataset consumer might need to know to avoid uses that could result in unfair treatment of individuals or groups or other risks or harms? If so, please provide a description. Is there anything a dataset consumer could do to mitigate these risks or harms?_**

The dataset reflects the idiosyncrasies of routine clinical practice. The archival process may have introduced biases or implausible values. Researchers are encouraged to follow best practice guidelines when using the data.

**_4. Are there tasks for which the dataset should not be used? If so, please provide a description._**

There is no specified information on tasks for which the dataset should not be used, as the database owners did not provide clear guidelines in the documentation.
