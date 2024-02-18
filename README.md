# MIMIC IV v2.0 Datasheet

In the high-stakes context of healthcare, it is critical to ensure unbiased predictive outcomes. Despite the significant progress made in healthcare machine learning (HML), unfairness still exists due to the presence of biases in data and algorithms. Popular ML fairness strategies aim to assess and reduce algorithmic discrimination by imposing fairness constraints during model training. However, one of the inherent limitations of model-centric strategy is the data itself, which encodes real-world biases and inconsistencies, making it difficult to achieve fairness in healthcare settings. This highlights a need to reconsider fairness in the context of (i) the task and (ii) the data driving the model, and ways to make it a central part of any HML analysis.

To spark advances in fair HML and to aid practitioners, we present a comprehensive **Datasheet for MIMIC IV v2.0 CRD**, highlighting data inconsistencies across the database and includes task-specific feature-target analysis to streamline fairness evaluations for equitable decision-making in HML models. More than a mere inventory, the datasheet provides comprehensive insights into the database's 

## Contents
- [Motivation](MOTIVATION.md)
- [Composition](COMPOSITION.md)
- [Collection Process](COLLECTION_PROCESS.md)
- [Preprocessing/cleaning/labeling](PREPROCESSING_CLEANING.md)
- [Uses](USES.md)
- [Distribution](DISTRIBUTION.md)
- [Maintenance](MAINTENANCE.md)
- [Analysis - Risk Prediction Tasks](ANALYSIS_RISK_PREDICTION.md)

This datasheet, inspired by [Gebru et al., 2021](https://dl.acm.org/doi/pdf/10.1145/3458723) template, has been adapted for the intricacies of Clinical Research Databases (CRDs) and enriched to offer a thorough understanding of the data's fabric and its implications for HML tasks.


For more details, please refer to the complete MIMIC IV v2.0 datasheet provided in this repository.
