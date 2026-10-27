# AI-Based Network Intrusion Detection Using Machine Learning

**Final Year Project Proposal**\
**The Islamia University of Bahawalpur (IUB)**\
**Department:** Information Technology

## Student Information

  Field                Details
  -------------------- -----------------------------------
  Student Name         Muhammad Nabeel
  Roll Number          F23BINFT1E02115
  Degree Program       BS Information Technology (BS IT)
  Semester / Section   7th Semester / 3M
  Project Supervisor   Dr. Nazeer Ahmad
  Academic Session     2023--2027
  Submission Date      27 October 2026

## Abstract

Computer networks face security threats such as port scanning,
denial-of-service activity, and unauthorized access attempts. A Network
Intrusion Detection System (NIDS) examines network activity to identify
traffic that may indicate malicious behaviour.

This project proposes an AI-based intrusion detection prototype using
machine learning. It will use a suitable public dataset, initially
considering UNSW-NB15, and compare models such as Decision Tree, Random
Forest, and Logistic Regression. Data preparation will include label
definition, feature handling, and a train/test strategy designed to
reduce data leakage.

Model performance will be assessed using accuracy, precision, recall,
F1-score, false positive rate, a confusion matrix, and prediction time.
A Streamlit dashboard will present model comparisons and example
predictions. The initial implementation will focus on offline analysis;
real-time monitoring and automatic attack prevention are outside the
initial scope. Actual results will be established through experiments.

## 1. Introduction

Computer networks support communication, education, commerce, and
digital services. Their security is important because malicious activity
can affect confidentiality, integrity, and availability. Network
Intrusion Detection Systems help identify suspicious activity by
analysing network traffic or traffic-derived features.

Machine learning can learn patterns from labelled examples and use them
to classify new records. Detection performance depends on dataset
quality, feature preparation, class balance, model selection, and
evaluation methodology. This project will compare selected models and
present results in a user-friendly dashboard.

## 2. Problem Statement

Distinguishing malicious traffic from normal traffic is challenging
because their characteristics may overlap. A detector can miss attacks
or incorrectly flag legitimate traffic, creating false negatives and
false positives. Accuracy alone may conceal these issues, particularly
when classes are imbalanced. A systematic comparison is needed to assess
detection performance, false alarms, and prediction cost using a
consistent dataset and testing procedure.

## 3. Aim

To develop and evaluate a machine learning-based Network Intrusion
Detection System that classifies network traffic records as normal or
malicious and presents the results through a simple dashboard.

## 4. Objectives

1.  Review research on network intrusion detection and machine learning.
2.  Select and inspect a suitable public labelled network-traffic
    dataset.
3.  Prepare the data, define target labels, and document preprocessing
    decisions.
4.  Implement and compare at least two classification algorithms.
5.  Evaluate models using precision, recall, F1-score, and false
    positive rate.
6.  Examine false alarms, missed detections, and prediction time.
7.  Build a dashboard to display predictions and evaluation results.
8.  Document findings, limitations, and possible future improvements.

## 5. Research Questions

1.  How effectively can selected machine learning models distinguish
    normal traffic from malicious traffic in the chosen dataset?
2.  Which model provides the most useful balance between detection
    performance and false positive rate?
3.  How do the models compare in prediction time and computational
    requirements?
4.  How can a dashboard make predictions and evaluation results easier
    to inspect?

## 6. Literature Review

Research into network intrusion detection has examined statistical
approaches, rule-based systems, and machine learning classifiers. Public
benchmark datasets support repeatable experimentation, but dataset age,
collection environment, label distribution, and feature definitions can
affect how well results transfer to real networks.

Moustafa and Slay introduced the UNSW-NB15 dataset for network intrusion
detection research and later published a comparative evaluation of
intrusion detection datasets. This project will review these
foundational works alongside recent peer-reviewed studies before
finalising the research gap.

## 7. Proposed Research Gap

The project will investigate the trade-off between detection quality,
false positive rate, and prediction cost when selected baseline
classifiers are evaluated under the same preprocessing and test
conditions. This is a provisional research direction, not a claim that
the gap is novel. It will be refined after reviewing recent literature
and discussing it with the supervisor.

## 8. Proposed Methodology

### 8.1 Dataset Selection

The project will initially consider the UNSW-NB15 dataset, which
contains normal traffic and multiple attack categories. The final
dataset files and target labels will be documented.

**Official dataset page:** [UNSW-NB15
Dataset](https://research.unsw.edu.au/projects/unsw-nb15-dataset)

### 8.2 Data Preprocessing

The dataset will be checked for missing values, duplicates, invalid
values, categorical features, and class distribution. Encoding and
numeric preprocessing will be applied as required. Target labels will be
separated from input features, and possible data leakage will be
reviewed. Preprocessing will be fitted using training data only.

### 8.3 Model Selection

-   **Decision Tree:** Learns decision rules from feature values.
-   **Random Forest:** Combines predictions from multiple decision
    trees.
-   **Logistic Regression:** Provides a relatively simple baseline
    classifier.

At least two models will be implemented, subject to dataset
characteristics and available computing resources.

### 8.4 Training and Testing

Models will be trained on a training subset and evaluated on held-out
test data. Initially, binary classification---normal versus
malicious---will be used. Where appropriate, stratified splitting will
preserve class proportions. The same split and comparable preprocessing
will be used for a fair comparison. Any class-balancing method will be
applied only to training data.

### 8.5 Evaluation Metrics

-   **Accuracy:** Proportion of records classified correctly.
-   **Precision:** Proportion of predicted malicious records that are
    actually malicious.
-   **Recall:** Proportion of malicious records detected.
-   **F1-score:** Harmonic mean of precision and recall.
-   **False Positive Rate:** Proportion of normal records incorrectly
    flagged as malicious.
-   **Confusion Matrix:** Counts of correct classifications, false
    alarms, and missed attacks.
-   **Prediction Time:** Inference time measured under a documented
    setup.

### 8.6 Dashboard

A Streamlit dashboard will display dataset summaries, model comparison
charts, evaluation metrics, a confusion matrix, and sample predictions.
It is intended for demonstration and analysis, not as a production
security appliance.

## 9. Proposed System Architecture

1.  **Dataset Input:** Load the selected public dataset.
2.  **Data Preparation:** Clean and encode features using a reproducible
    pipeline.
3.  **Model Training:** Train selected classifiers.
4.  **Prediction and Evaluation:** Classify held-out records and
    calculate metrics.
5.  **Dashboard:** Display summaries, comparisons, and example flagged
    records.

**Workflow:**
`Dataset → Preprocessing → Model Training → Prediction & Evaluation → Dashboard`

## 10. Tools and Technologies

  Technology           Purpose
  -------------------- -----------------------------------------------
  Python               Core programming language
  Visual Studio Code   Development environment
  Pandas and NumPy     Data handling and numerical operations
  Scikit-learn         Preprocessing, model training, and evaluation
  Streamlit            Dashboard interface
  Matplotlib           Charts and visualisations
  UNSW-NB15            Candidate public dataset

## 11. Expected Outcomes

1.  A working offline machine learning intrusion-detection prototype.
2.  At least two trained classification models.
3.  A comparison of model performance on held-out data.
4.  Documented detection performance and false positive rates.
5.  A dashboard showing evaluation results and sample classifications.
6.  A final report describing implementation, findings, and limitations.

These are expected deliverables, not guaranteed performance claims.
Actual results will be reported after experiments.

## 12. Scope

The initial scope is offline analysis of a public labelled dataset,
binary classification of normal and malicious records, model comparison,
and a dashboard. Live network capture, automatic blocking, production
deployment, and guaranteed detection of previously unseen attacks are
outside the initial scope.

## 13. Limitations

-   Public datasets may not represent every real-world network.
-   The system may generate false alarms or miss genuine attacks.
-   Performance on one dataset may not generalise to unseen traffic.
-   Results depend on preprocessing, class distribution, and hardware.
-   Offline testing alone cannot establish real-time detection
    performance.

## 14. Ethical and Security Considerations

The initial implementation will use a public dataset. Any later live
testing will be limited to networks and devices for which explicit
permission has been obtained. Sensitive traffic will not be collected
without authorisation and appropriate safeguards. The prototype will not
automatically block traffic or change network infrastructure.

## 15. Proposed Work Plan

  -----------------------------------------------------------------------
  Duration                            Activities
  ----------------------------------- -----------------------------------
  Weeks 1--2                          Literature review and refinement of
                                      research questions

  Week 3                              Dataset inspection and
                                      preprocessing

  Weeks 4--5                          Model implementation and training

  Week 6                              Testing, evaluation, and model
                                      comparison

  Week 7                              Dashboard development

  Week 8                              Integration, verification, and
                                      improvements

  Weeks 9--10                         Report writing, supervisor review,
                                      and presentation preparation
  -----------------------------------------------------------------------

The schedule is provisional and may be revised according to supervisor
feedback and departmental deadlines.

## 16. References

1.  Moustafa, N., & Slay, J. (2015). *UNSW-NB15: A comprehensive data
    set for network intrusion detection systems.* In Military
    Communications and Information Systems Conference (MilCIS). IEEE.
2.  Moustafa, N., & Slay, J. (2016). *The evaluation of Network Anomaly
    Detection Systems: Statistical analysis of the UNSW-NB15 dataset and
    the comparison with the KDD99 dataset.* Information Security
    Journal: A Global Perspective.
3.  UNSW Canberra. [UNSW-NB15
    Dataset](https://research.unsw.edu.au/projects/unsw-nb15-dataset).

> **Before submission:** Verify complete bibliographic details and add
> recent peer-reviewed studies reviewed during the literature search.
> Confirm the final format with the project supervisor or department.

## Approval / Review

  Project Supervisor                                      FYP Coordinator / Departmental In-charge
  ------------------------------------------------------- ------------------------------------------------------------
  Name: Dr. Nazeer Ahmad                                  Name: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
  Signature: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_   Signature: \_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_\_
