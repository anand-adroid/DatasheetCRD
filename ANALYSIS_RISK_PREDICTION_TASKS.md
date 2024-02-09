MIMIC-III and IV have been pivotal in healthcare machine learning (HML) prediction tasks. This analysis zeroes in on MIMIC-IV version 2.0, the most recent release available to the public. We procured datasets for, 
- In-hospital mortality concerning 
  - Heart failure
  - Chronic kidney disease (CKD)
  - Sepsis  
- 30-day readmission, and 
- Length of stay (LOS) for heart failure 
by adhering to the established [pipeline](https://proceedings.mlr.press/v193/gupta22a) except for sepsis mortality. 

For sepsis mortality, we directly extracted patient data affected by sepsis, omitting the use of a specific pipeline, to validate and compare outcomes derived from both methodologies.

## Analysis of Sensitive Attributes and Their Association With Prediction Outcomes

Our study employed the *Chi-Square* statistical test to discern the attribute most strongly associated with prediction outcomes. Despite considering various sensitive attributes such as Age, Gender, Ethnicity, Insurance, Language, and Marital Status, chi-square results predominantly indicated that ethnicity bore the most significant association with the prediction tasks. Hence Ethnicity is the sensitive attribute considered throughout the modelling and fairness evaluation of the main paper.

### Risk Prediction Analysis:


## 30-day ICU Readmission Analysis

![Relationship between Readmission rates and patient's ethnicity/insurance](https://raw.githubusercontent.com/anand-adroid/Datasheet_for_CRD.io/main/Images/Try_3_Readmitted_based_on_Insurance.jpg)


**Cohort Distribution Insights** \
The median age for patients readmitted to the ICU within 30 days was 64, with a distribution of 56% male and 44% female. Predominantly, the White demographic represented 69% of the cohort, followed by Black, Other, Hispanic/Latino, and Asian subgroups, reflecting the geographical context of data collection.

**Insurance Utilization Patterns** \
A significant portion of the cohort primarily relied on Other insurance (48%), with Medicare following closely at 44%. The analysis indicates that Other-subgroup and Hispanic/Latino patients predominantly utilized Other insurance, with Black and Asian patients following suit. Medicaid utilization was notably lower across all ethnic subgroups, at 8%. Interestingly, only a small fraction (5.4%) of Caucasian patients utilized Medicaid, with Black and Other ethnic patients showing higher Medicaid utilization, underscoring socio-economic disparities.

**Readmission Rates and Ethnicity** \
The analysis reveals that the Black subgroup, along with Medicaid-insured Asian patients, displayed higher readmission rates across various ailments. The chi-square (χ² = 141.89, p < 0.001) test further corroborate the significant association between ethnicity concerning readmission rates.

## In-Hospital Mortality Prediction 

### Sepsis-Related Ailments
\
**Cohort Distribution Insights** \
The cohort's median age was 63, evenly distributed between male (53%) and female (47%) patients. The dataset primarily comprised the White demographic (69%), with subsequent representation from Black, Other, Hispanic/Latino, and Asian subgroups.
**Insurance Utilization Patterns:**Medicare emerged as the most utilized insurance across all ethnicities (51%), with Other insurance closely behind at 41%. Medicaid saw the least utilization at 8%. Notably, White and Black patients had the highest Medicare utilization, indicative of an older population within these communities. Conversely, minority groups showed a preference for Other insurance, suggesting a relatively younger demographic or the presence of private insurance coverage. Despite being the largest demographic, only 5.5% of Caucasians utilized Medicaid, whereas Black patients had a higher Medicaid utilization, highlighting socio-economic disparities.



![Sepsis Mortality in Relation to Ethnicity/Insurance : Figure illustrates the % mortality among sepsis patients by depicting the variations in mortality across different ethnic groups and insurance categories, with Label 0 denoting the alive patients and Label 1 indicating the deceased.](https://raw.githubusercontent.com/anand-adroid/Datasheet_for_CRD.io/main/Images/Sepsis Dead V alive based on Insurance and race percentage grouped horizontal bar chart (1).jpg)
  

**The mortality rate analysis** \
Analysis starkly illustrates that individuals from other ethnic groups and Asians had consistently higher death proportions, irrespective of their insurance status. The Chi-square test (χ² = 975.185, p < 0.001)  validate a strong association between ethnicity and sepsis mortality, underlining the necessity of considering demographic variables in predictive modeling of sepsis mortality.

### Heart failure

**Cohort distribution** \
Heart failure cohort consisted of patients with a median age of 72, with a nearly equal distribution of male (55%) and female (45%). The majority of patients (70%) belonged to the White demographic, followed by the Black, Other, Hispanic/Latino, and Asian subgroups, reflecting the specific geographical location of data collection.

**Cohort Insurance utilization** \
White and Black individuals had the highest patient counts, followed by the Other subgroup. Medicare was the most commonly used insurance among all the subgroups, except for Asians, as indicated by the figure. White patients exhibited the highest utilization of Medicare, followed by the Other-ethnic subgroup. Medicaid utilization was lower across all subgroups, except for Hispanic/Latino, Asian, and Black patients. 

<figure>
    <img src="https://github.com/anand-adroid/Datasheet_for_CRD.io/tree/main/Images/Try 2 Insurance_by race pie final (1).jpg" 
    alt="Insurance Utilization among Heart Failure Cohorts based on Ethnicity: Figure showcases the % insurance utilization within heart failure patients, categorized by their respective ethnicity."
</figure>

**Mortality rate** \
Individuals from other ethnic groups consistently exhibited higher mortality rates, irrespective of their insurance. Asians insured with Other and Medicaid also demonstrated a relatively higher proportion of death. Caucasian death rates were significantly lower in comparison to other subgroups. The chi-square test statistic yielded a significant result of 105.107 (p < 0.001), providing robust evidence of an association between the variables. 

### Chronic Kidney Disease

**Cohort distribution** \
CKD cohort primarily consists of older male patients, with a median age of 71 where White individuals represent the majority (64%), followed by Black, Other, Hispanic/Latino, and Asian subgroups. White and Black patients have the highest patient counts, along with the Other subgroup.

**Cohort Insurance utilization** \
Medicare insurance is widely utilized, with 60.5% of patients across all ethnicity opting for it. Medicaid records the lowest utilization, with only 4.7% of patients utilizing it. Among the race subgroups, White and Black individuals demonstrate the highest usage of Medicare insurance, while Asians show a preference for other insurance types. 2.3% of Caucasians utilize Medicaid insurance whereas Black patients have a higher utilization of Medicaid insurance compared to other subgroups.

<figure>
    <img src="https://github.com/anand-adroid/Datasheet_for_CRD.io/tree/main/Images/Try 3 Dead V alive based on Insurance and race percentage bar chart.jpg" 
    alt="% CKD mortality rate with respect to their Ethnicity/Insurance."
</figure>

**Mortality rate** \
The figure shows individuals from other-ethnic groups consistently exhibit higher proportions of deaths, regardless of their insurance type. Medicare-insured Blacks experience the second-highest mortality rates, preceded by Caucasians. The chi-square (χ² = 106.578, p < 0.001) statistical test shows a significant association suggesting a potential relationship between ethnicity and mortality outcomes.

### ICU Length of Stay Prediction

The ICU LOS > 7 days cohort had a median age of 72, balanced between males (55%) and females (45%). The dataset predominantly consisted of Whites (69%), followed by other demographic groups. 

| Ethnicity       | Insurance | <7 days | >7 days |
|-----------------|-----------|---------|---------|
| Asian           | Medicaid  | 75.926  | 24.074  |
|                 | Medicare  | 87.634  | 12.366  |
|                 | Other     | 82.511  | 17.489  |
| Black           | Medicaid  | 88.938  | 11.062  |
|                 | Medicare  | 88.377  | 11.623  |
|                 | Other     | 87.197  | 12.803  |
| Hispanic/Latino | Medicaid  | 91.304  | 8.696   |
|                 | Medicare  | 85.185  | 14.815  |
|                 | Other     | 86.282  | 13.718  |
| Other           | Medicaid  | 78.947  | 21.053  |
|                 | Medicare  | 82.698  | 17.302  |
|                 | Other     | 82.653  | 17.347  |
| White           | Medicaid  | 83.898  | 16.102  |
|                 | Medicare  | 87.341  | 12.659  |
|                 | Other     | 85.873  | 14.127  |

Furthermore, Chi-square (p < 0.001) statistical test confirms an association between LOS and ethnicity, reinforcing the influence of these demographic factors on ICU outcomes for heart failure patients.


This analysis underscores the importance of considering ethnic demographics in predictive modeling.
