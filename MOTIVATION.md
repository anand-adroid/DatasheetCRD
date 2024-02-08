**1. For what purpose was the database created? Was there a specific task in mind? Was there a specific gap that needed to be filled? Please provide a description.**\
The [MIMIC-IV](https://www.nature.com/articles/s41597-022-01899-x) Clinical Research Database (CRD) was designed to enhance patient care by supporting knowledge discovery and algorithm development through a historically collected medical dataset. It's structured for broad access and has been instrumental in various healthcare applications.

**2. Who created the database (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)?**\
The database was developed by the MIT Laboratory for Computational Physiology, by Alistair Johnson, Lucas Bulgarelli, Tom Pollard, Steven Horng, Leo Anthony Celi, and Roger Mark, reflecting a collaborative effort across research groups.

**3. Who funded the creation of the database?**\
Funding was provided by the National Institute of Biomedical Imaging and Bioengineering (NIBIB) of the National Institutes of Health (NIH) under award numbers R01-EB001659 (2003-2013) and R01-EB017205 (2014-2018)[^1]

[^1]:[MIMIC](https://mimic.mit.edu/)

**4. Any other comments?**

MIMIC-IV, part of a series of [MIMIC](https://mimic.mit.edu/docs/about/) databases, includes deidentified health data from intensive care units and has been pivotal in healthcare machine learning research. MIMIC is a large and freely available database that contains deidentified health-related data from patients admitted to the critical care units of the Beth Israel Deaconess Medical Center. There are multiple versions of MIMIC that have been released:
1. MIMIC-IV encompasses data collected from 2008 to 2019, obtained from Metavision bedside monitors.
2. MIMIC-III comprises data collected from 2001 to 2012, obtained from both Metavision and CareVue bedside monitors.
3. MIMIC-II includes data collected from 2001 to 2008, obtained exclusively from CareVue bedside monitors. While MIMIC-II is no longer publicly available, its data can still be obtained from MIMIC-III by selectively including the data from the CareVue monitors.

Throughout the surveyed timeline, MIMIC III and MIMIC IV have been extensively utilized for healthcare machine learning (HML) prediction models. The datasheet provided is specifically for MIMIC IV v2.0, the latest available version of the database. 

**License** - The licensing for the MIMIC files can be found in the [PhysioNet Credentialed Health Data License 1.5.0 (MIT-LCP)](https://physionet.org/content/mimiciv/2.2/).
