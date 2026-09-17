# Data Preparation — Master Curriculum (Final Version)

**Version:** Final v1.0  
**Sections:** 41  
**Structure:** 3 Layers + Optional Specialization  
**Cross-cutting Concerns:** Leakage · Sampling · Temporal · Observability · Bias/Fairness · Privacy

---

##  Overall Structure

LAYER 1 — CORE DATA PREPARATION              (Sections 1 – 25)
LAYER 2 — SPECIALIZED DATA PREPARATION       (Sections 26 – 29)
LAYER 3 — PRODUCTION, GOVERNANCE & MLOps     (Sections 30 – 40)
OPTIONAL — AI / LLM ERA SPECIALIZATION       (Section 41)

---

#  LAYER 1 — CORE DATA PREPARATION

## 1. Data Leakage Fundamentals

- 1-1. What is Data Leakage & Why It Matters
- 1-2. Target Leakage
- 1-3. Train-Test Contamination
- 1-4. Temporal Leakage
- 1-5. Group Leakage
- 1-6. Preprocessing Leakage
- 1-7. Feature Engineering Leakage
- 1-8. Aggregation Leakage
- 1-9. Label Leakage
- 1-10. Leakage Detection Techniques
- 1-11. Point-in-time Correctness
- 1-12. Leakage Auditing Checklist
- 1-13. Early Awareness of Splitting Principles *(Cross-ref to 24)*

## 2. Data Collection

- 2-1. Defining Data Requirements
- 2-2. Identifying Data Sources
- 2-3. Planning Collection Strategy
- 2-4. Setting Collection Frequency
- 2-5. Choosing Collection Methods
- 2-6. Ensuring Data Relevance
- 2-7. Estimating Data Volume Needed
- 2-8. Addressing Privacy Concerns
- 2-9. Setting Collection Timeline
- 2-10. Documenting Collection Plan
- 2-11. Data Contracts Definition
- 2-12. Cost & Resource Estimation
- 2-13. Storage & Processing Budget Planning

## 3. Sampling & Dataset Construction

- 3-1. Random Sampling
- 3-2. Stratified Sampling
- 3-3. Systematic Sampling
- 3-4. Cluster Sampling
- 3-5. Reservoir Sampling
- 3-6. Importance Sampling
- 3-7. Temporal Sampling
- 3-8. Group Sampling
- 3-9. Sampling Bias & Selection Bias
- 3-10. Train/Test Population Alignment
- 3-11. Dataset Curation
- 3-12. Dataset-level Deduplication & Near-duplicate Detection
- 3-13. Contamination Checks

## 4. Data Acquisition

- 4-1. Accessing Internal Databases
- 4-2. Using Public Datasets
- 4-3. Purchasing External Data
- 4-4. Scraping Web Data
- 4-5. Collecting via APIs
- 4-6. Gathering Sensor / IoT Data
- 4-7. Conducting Surveys & Forms
- 4-8. Logging User Interactions
- 4-9. Handling Data Access Permissions
- 4-10. Verifying Data Ownership
- 4-11. Webhooks & Event-driven Collection
- 4-12. Change Data Capture (CDC)
- 4-13. Streaming Collection

## 5. Data Semantics & Metadata

- 5-1. Business vs Technical Metadata
- 5-2. Data Definitions & Semantic Types
- 5-3. Data Domains
- 5-4. Units & Measurement Semantics
- 5-5. Metadata Quality
- 5-6. Data Ownership & Stewardship
- 5-7. Metadata Discovery
- 5-8. Source-of-Truth Identification

## 6. Data Integration

- 6-1. Identifying Common Keys
- 6-2. Schema Matching
- 6-3. Handling Different Formats
- 6-4. Resolving Data Conflicts
- 6-5. Merging Multiple Sources
- 6-6. Joining Tables Efficiently
- 6-7. Handling Time Zone Differences
- 6-8. Unifying Units & Scales
- 6-9. Creating Master Dataset
- 6-10. Validating Integrated Data
- 6-11. Schema Evolution Management

## 7. Entity Resolution & Record Linkage

- 7-1. Exact Matching
- 7-2. Fuzzy Matching
- 7-3. Blocking & Indexing Strategies
- 7-4. Probabilistic Matching
- 7-5. Entity-level Deduplication
- 7-6. Entity Resolution
- 7-7. Record Linkage
- 7-8. Master Data Management (MDM)
- 7-9. Surrogate Keys
- 7-10. Slowly Changing Dimensions (SCD)
- 7-11. Golden Record Creation

## 8. Scalable / Big Data Processing

- 8-1. When Pandas Isn't Enough
- 8-2. Polars
- 8-3. Dask
- 8-4. Spark
- 8-5. Out-of-core Processing
- 8-6. Chunked Reading & Processing
- 8-7. Memory Optimization
- 8-8. Columnar Formats
- 8-9. Partitioning Strategies
- 8-10. Benchmarking & Profiling

## 9. Exploratory Data Analysis (EDA)

- 9-1. Dataset Shape & Dimensions
- 9-2. Data Types Inspection
- 9-3. Descriptive Statistics
- 9-4. Univariate Analysis
- 9-5. Bivariate Analysis
- 9-6. Multivariate Analysis
- 9-7. Correlation Analysis
- 9-8. Distribution Analysis
- 9-9. Class Balance Inspection
- 9-10. Documenting EDA Findings
- 9-11. Automated EDA
- 9-12. Data Drift Baseline
- 9-13. Visualization Best Practices

## 10. Data Cleaning

- 10-1. Removing Duplicates
- 10-2. Fixing Inconsistent Formats
- 10-3. Correcting Typos & Errors
- 10-4. Standardizing Categories
- 10-5. Handling Invalid Values
- 10-6. Cleaning Text Data
- 10-7. Fixing Date & Time Formats
- 10-8. Removing Irrelevant Columns
- 10-9. Standardizing Naming Conventions
- 10-10. Creating Cleaning Pipeline

## 11. Data Validation

- 11-1. Checking Data Types
- 11-2. Validating Value Ranges
- 11-3. Referential Integrity
- 11-4. Business Rules
- 11-5. Logical Inconsistencies
- 11-6. Cross-field Validation
- 11-7. Schema Validation
- 11-8. Completeness Checks
- 11-9. Consistency Checks
- 11-10. Validation Reports
- 11-11. Data Contracts Enforcement
- 11-12. Quality Dimensions Scoring

## 12. Data Profiling

- 12-1. Column-level Profiling
- 12-2. Table-level Profiling
- 12-3. Distribution Profiling
- 12-4. Pattern & Format Profiling
- 12-5. Cross-column Dependency
- 12-6. Temporal Profiling
- 12-7. Profiling Tools
- 12-8. Profiling Reports & Baselines
- 12-9. Profiling for Anomaly Detection
- 12-10. Continuous Profiling

## 13. Data Quality Framework

- 13-1. Accuracy Metrics
- 13-2. Completeness Metrics
- 13-3. Consistency Metrics
- 13-4. Timeliness Metrics
- 13-5. Validity Metrics
- 13-6. Uniqueness Metrics
- 13-7. Quality Scorecards
- 13-8. Root Cause Analysis
- 13-9. Quality Monitoring Dashboards
- 13-10. Quality Improvement Feedback Loop

## 14. Missing Value Handling

- 14-1. Identifying Missing Patterns
- 14-2. Missing Mechanisms (MCAR, MAR, MNAR)
- 14-3. Deleting Rows / Columns
- 14-4. Mean / Median / Mode Imputation
- 14-5. Forward / Backward Fill
- 14-6. Interpolation
- 14-7. Model-based Imputation
- 14-8. Multiple Imputation
- 14-9. Indicator Variables
- 14-10. Evaluating Imputation Impact
- 14-11. Iterative Approach with Outliers

## 15. Outlier Detection

- 15-1. Statistical Methods
- 15-2. Visualization Methods
- 15-3. Distance-based Methods
- 15-4. Density-based Methods
- 15-5. Model-based Detection
- 15-6. Multivariate Outlier Detection
- 15-7. Time-series Outlier Detection
- 15-8. Domain-specific Rules
- 15-9. Ranking Severity
- 15-10. Documenting Outliers

## 16. Outlier Treatment

- 16-1. Removing Outliers
- 16-2. Capping / Winsorizing
- 16-3. Transformation Methods
- 16-4. Binning Extreme Values
- 16-5. Treating as Missing
- 16-6. Separate Modeling
- 16-7. Robust Scaling
- 16-8. Domain-informed Correction
- 16-9. Evaluating Treatment Impact
- 16-10. Keep vs Treat Strategy
- 16-11. Re-checking Missing Values

## 17. Noise Reduction

- 17-1. Identifying Noise Sources
- 17-2. Smoothing Techniques
- 17-3. Filtering Methods
- 17-4. Moving Average / Rolling Window
- 17-5. Wavelet Denoising
- 17-6. Frequency Domain Filtering
- 17-7. Robust Statistical Methods
- 17-8. Feature-level Noise Handling
- 17-9. Label Noise Detection
- 17-10. Measuring Noise Reduction Effect

## 18. Label Quality & Annotation

- 18-1. Labeling Guidelines
- 18-2. Manual Annotation Workflows
- 18-3. Inter-Annotator Agreement
- 18-4. Crowdsourcing Quality Control
- 18-5. Weak Supervision
- 18-6. Active Learning
- 18-7. Semi-supervised Labeling
- 18-8. Label Noise Detection & Correction
- 18-9. Label Distribution Analysis
- 18-10. Label Versioning
- 18-11. Human-in-the-loop
- 18-12. Multi-annotator Consensus

## 19. Data Transformation (ML-Centric)

- 19-1. Type Conversion
- 19-2. Normalization
- 19-3. Standardization
- 19-4. Log / Box-Cox / Yeo-Johnson
- 19-5. Label Encoding
- 19-6. One-Hot Encoding
- 19-7. Ordinal Encoding
- 19-8. Target Encoding
- 19-9. Discretization / Binning
- 19-10. Custom Transformers & Pipelines

## 20. Data Transformation (Data-Engineering-Centric)

- 20-1. Reshaping
- 20-2. Aggregation
- 20-3. Join Transformations
- 20-4. Window Operations
- 20-5. JSON / Nested Normalization
- 20-6. Semi-structured Data
- 20-7. SQL-based Transformations
- 20-8. Flattening Hierarchies
- 20-9. Array / List Handling
- 20-10. Documenting DE Transformations

## 21. Feature Engineering

- 21-1. Domain-driven Features
- 21-2. Date / Time Features
- 21-3. Text Features
- 21-4. Interaction Features
- 21-5. Polynomial Features
- 21-6. Aggregation Features
- 21-7. Lag & Rolling Features
- 21-8. Binning-based Features
- 21-9. Feature Extraction
- 21-10. Documenting Feature Engineering
- 21-11. Leakage-aware Feature Creation *(Cross-ref to 1 & 24)*

## 22. Feature Selection

- 22-1. Filter Methods
- 22-2. Wrapper Methods
- 22-3. Embedded Methods
- 22-4. Regularization-based
- 22-5. Stability Selection
- 22-6. Domain-informed Selection
- 22-7. Multicollinearity (VIF)
- 22-8. Evaluating Impact
- 22-9. Documenting Selected Features
- 22-10. Leakage-aware Selection

## 23. Dimensionality Reduction & Representation Learning

- 23-1. PCA
- 23-2. Truncated SVD
- 23-3. Factor Analysis
- 23-4. ICA
- 23-5. LDA (Supervised)
- 23-6. UMAP
- 23-7. t-SNE
- 23-8. Autoencoders
- 23-9. Evaluating Reduction Impact
- 23-10. Documenting Strategy

## 24. Data Splitting

- 24-1. Train / Validation / Test Split
- 24-2. Stratified Split
- 24-3. Group-based Split
- 24-4. Time-series Split
- 24-5. K-Fold Cross-Validation
- 24-6. Stratified K-Fold
- 24-7. Leave-One-Out / Leave-P-Out
- 24-8. Nested Cross-Validation
- 24-9. Data Leakage Prevention
- 24-10. Documenting Split Strategy
- 24-11. Leakage Auditing Checklist
- 24-12. Split Testing & Validation

## 25. Imbalance Handling

- 25-1. Detecting Class Imbalance
- 25-2. Random Undersampling
- 25-3. Random Oversampling
- 25-4. SMOTE / ADASYN / Borderline-SMOTE
- 25-5. Tomek Links / ENN
- 25-6. Class Weight Adjustment
- 25-7. Threshold Moving
- 25-8. Ensemble Methods
- 25-9. Evaluating Impact
- 25-10. Documenting Strategy
- 25-11. Apply Only on Train Set

---

# 🟩 LAYER 2 — SPECIALIZED DATA PREPARATION

> **Note:** This layer contains 4 specialized tracks. Each can be expanded into a standalone module with 10 sub-sections. Common prerequisite: Layer 1.

## 26. Time-series Specific Preparation

- 26-1. Timestamp Indexing & Resampling
- 26-2. Seasonality Handling
- 26-3. Stationarity Testing (ADF, KPSS)
- 26-4. Detrending & Differencing
- 26-5. Missing Values in Time-series
- 26-6. Time-series Outlier Treatment
- 26-7. Lag & Window Features
- 26-8. Fourier & Calendar Features
- 26-9. Time-series Cross-Validation
- 26-10. Temporal Leakage Prevention *(Cross-ref to 1-4)*

## 27. Multimodal & Unstructured Data Preparation

- 27-1. Image Preprocessing
- 27-2. Audio Preprocessing
- 27-3. Video Preprocessing
- 27-4. Text Preprocessing
- 27-5. Embedding Extraction (CLIP, Whisper, BERT)
- 27-6. Modality Alignment
- 27-7. Multimodal Fusion Strategies
- 27-8. Handling Missing Modalities
- 27-9. Storage & Format Optimization
- 27-10. Documenting Multimodal Prep

## 28. Graph / Network Data Preparation

- 28-1. Node & Edge Definition
- 28-2. Graph Construction from Tabular Data
- 28-3. Graph Cleaning & Deduplication
- 28-4. Node Feature Engineering
- 28-5. Edge Feature Engineering
- 28-6. Graph Sampling & Subgraph Extraction
- 28-7. Handling Dynamic Graphs
- 28-8. Graph Splitting
- 28-9. Graph Libraries (NetworkX, PyG, DGL)
- 28-10. Documenting Graph Prep

## 29. Geospatial Data Preparation

- 29-1. Coordinate Systems & CRS Handling
- 29-2. Geocoding & Reverse Geocoding
- 29-3. Spatial Joins
- 29-4. Distance & Proximity Features
- 29-5. Spatial Aggregation
- 29-6. Handling Invalid Geometries
- 29-7. Raster vs Vector Data
- 29-8. Map Projections
- 29-9. Geospatial Libraries (GeoPandas, Shapely, Rasterio)
- 29-10. Documenting Geospatial Prep

---

# 🟥 LAYER 3 — PRODUCTION, GOVERNANCE & MLOps

## 30. Synthetic Data Generation

- 30-1. When to Use Synthetic Data
- 30-2. Statistical Generation (CTGAN, TVAE)
- 30-3. Rule-based Generation
- 30-4. Data Augmentation Techniques
- 30-5. Privacy-preserving Synthesis
- 30-6. Fidelity vs Utility Trade-off
- 30-7. Evaluating Synthetic Data Quality
- 30-8. Mixing Real & Synthetic Data
- 30-9. Bias in Synthetic Data
- 30-10. Documenting Synthetic Data Usage

## 31. Data Privacy & Compliance

- 31-1. GDPR Compliance
- 31-2. CCPA / CPRA Compliance
- 31-3. HIPAA
- 31-4. Anonymization Techniques
- 31-5. Pseudonymization
- 31-6. Differential Privacy
- 31-7. K-Anonymity / L-Diversity / T-Closeness
- 31-8. Data Masking & Tokenization
- 31-9. Consent Management
- 31-10. Privacy Impact Assessment

## 32. Bias & Fairness in Data

- 32-1. Types of Bias
- 32-2. Detecting Bias in Features
- 32-3. Detecting Bias in Labels
- 32-4. Protected Attributes Identification
- 32-5. Fairness Metrics
- 32-6. Bias Mitigation (Pre-processing)
- 32-7. Reweighing & Resampling
- 32-8. Fairness Auditing Tools (AIF360, Fairlearn)
- 32-9. Documenting Bias Assessment
- 32-10. Ethical Review Checklist

## 33. Data Drift & Concept Drift Detection

- 33-1. Types of Drift
- 33-2. Statistical Drift Tests (KS, PSI, Chi-square)
- 33-3. Window-based Drift Detection
- 33-4. Drift Monitoring Setup
- 33-5. Alerts & Thresholds
- 33-6. Retraining Triggers
- 33-7. Drift Visualization
- 33-8. Tools (Evidently, NannyML)
- 33-9. Documenting Drift Events
- 33-10. Drift Response Playbook

## 34. Data Observability

- 34-1. Freshness Monitoring
- 34-2. Volume Monitoring
- 34-3. Distribution Monitoring
- 34-4. Schema Monitoring
- 34-5. Lineage Observability
- 34-6. Quality Observability
- 34-7. Anomaly Detection in Production
- 34-8. Incident Detection & Alerting
- 34-9. SLA / SLO Definition
- 34-10. Root Cause Analysis
- 34-11. Data Observability Tools (Monte Carlo, Soda, GE)

## 35. Data Documentation

- 35-1. Creating Data Dictionary
- 35-2. Documenting Data Sources
- 35-3. Recording Collection Methods
- 35-4. Describing Cleaning Steps
- 35-5. Noting Transformations Applied
- 35-6. Logging Missing Value Strategies
- 35-7. Documenting Outlier Decisions
- 35-8. Versioning Datasets
- 35-9. Writing Data Quality Report
- 35-10. Maintaining Update History

## 36. Data Versioning & Lineage

- 36-1. Dataset Versioning (DVC, LakeFS, Delta Lake)
- 36-2. Data Lineage Tracking
- 36-3. Transformation Graph Documentation
- 36-4. Reproducibility of Data Pipelines
- 36-5. Snapshot Management
- 36-6. Rollback Strategies
- 36-7. Metadata Management
- 36-8. Catalog Tools (DataHub, Amundsen)
- 36-9. Audit Trails
- 36-10. Compliance & Retention Policies

## 37. Feature Store & Feature Serving

- 37-1. Feature Store Concepts (Online vs Offline)
- 37-2. Feature Definitions & Registry
- 37-3. Feast / Tecton / Hopsworks
- 37-4. Feature Versioning
- 37-5. Point-in-time Correctness
- 37-6. Online Serving (Low-latency)
- 37-7. Offline Serving (Batch)
- 37-8. Train-Serve Consistency
- 37-9. Feature Monitoring
- 37-10. Documenting Feature Store Usage

## 38. End-to-End Data Pipeline & Automation

- 38-1. Pipeline Design Principles
- 38-2. sklearn Pipeline
- 38-3. Pandas Pipeline / Method Chaining
- 38-4. Kedro for Structured Pipelines
- 38-5. Airflow for Orchestration
- 38-6. Prefect / Dagster
- 38-7. Scheduling & Triggers
- 38-8. Error Handling & Retries
- 38-9. Pipeline Testing (Unit, Integration, Property-based)
- 38-10. CI/CD for Data Pipelines

## 39. Data Saving, Containerization & Reproducibility

- 39-1. Saving Clean Dataset (CSV, Parquet)
- 39-2. Saving Transformers (joblib, pickle)
- 39-3. Saving Pipelines (sklearn Pipeline)
- 39-4. Saving Feature Metadata
- 39-5. Saving Split Indices
- 39-6. Environment & Dependency Locking
- 39-7. Random Seed Management
- 39-8. Containerization (Docker)
- 39-9. Infrastructure as Code (Terraform, Ansible)
- 39-10. Reproducibility Checklist
- 39-11. Handoff Documentation for Modeling

## 40. Data Governance & Ethics

- 40-1. Data Ownership & Stewardship
- 40-2. Data Access Control
- 40-3. Data Retention Policies
- 40-4. Ethical Data Use Guidelines
- 40-5. Bias Auditing Framework
- 40-6. Transparency & Explainability
- 40-7. Regulatory Compliance Matrix
- 40-8. Incident Response Plan
- 40-9. Stakeholder Communication
- 40-10. Governance Review Cycle

---

# 🟪 OPTIONAL — AI / LLM ERA SPECIALIZATION

## 41. AI / LLM Dataset Preparation

- 41-1. Document Collection & Filtering
- 41-2. Language Identification
- 41-3. Document Deduplication
- 41-4. Near-duplicate Detection
- 41-5. PII Detection & Redaction
- 41-6. Quality Filtering
- 41-7. Toxic / Unsafe Content Filtering
- 41-8. Document Structure Extraction
- 41-9. Chunking Strategies
- 41-10. Metadata Enrichment
- 41-11. Dataset Mixture Design
- 41-12. Train/Eval Contamination Prevention
- 41-13. Synthetic Data Mixing
- 41-14. Preference / Instruction Data Preparation

---

# 📊 Cross-Cutting Concerns Map

| Concept             | Related Sections                                             |
| ------------------- | ------------------------------------------------------------ |
| **Leakage**         | 1 (primary) → 3, 21-11, 22-10, 24-9, 24-11, 25-11, 26-10, 37-5 |
| **Sampling**        | 3 (primary) → 9, 25, 32                                      |
| **Temporal**        | 1-4, 3-7, 15-7, 21-7, 26 (primary)                           |
| **Observability**   | 12-10, 13-9, 33, 34 (primary)                                |
| **Bias / Fairness** | 3-9, 18-8, 30-9, 32 (primary)                                |
| **Privacy**         | 2-8, 30-5, 31 (primary), 40                                  |

---

# 🎯 Recommended Study Tracks

| Track                       | Sections                                                     | Duration | Audience                 |
| --------------------------- | ------------------------------------------------------------ | -------- | ------------------------ |
| 🟢 **Core**                  | 1, 2, 3, 6, 9, 10, 11, 14, 15, 16, 17, 18, 19, 21, 22, 24, 25, 35 | ~40h     | Beginner–Intermediate    |
| 🟡 **Intermediate**          | Core + 4, 5, 7, 8, 12, 13, 20, 23, 30, 31, 32, 33            | ~80h     | Data Scientist / Analyst |
| 🔴 **Advanced / Production** | All + 26–29 (Specialized) + 34, 36, 37, 38, 39, 40           | ~120h+   | ML Engineer / MLOps      |
| 🟣 **LLM / AI Track**        | 1, 3, 18, 27 + 41 (full)                                     | ~50h     | NLP / LLM Engineer       |

---

# 📋 Statistical Summary

| Metric                     | Value                                                        |
| -------------------------- | ------------------------------------------------------------ |
| **Layers**                 | 3 + 1 Optional                                               |
| **Sections**               | 41                                                           |
| **Sub-sections**           | ~420                                                         |
| **Cross-cutting concerns** | 6                                                            |
| **Study tracks**           | 4                                                            |
| **Coverage**               | Data Engineering + Data Quality + ML Prep + Governance + MLOps + Specialized + LLM |

---

# ✅ Final Checklist

- [x] Leakage as foundational concept at the start
- [x] Sampling & Dataset Construction as standalone
- [x] Entity Resolution & Record Linkage
- [x] Data Semantics & Metadata
- [x] Data-Engineering Transformations (JSON, SQL, Semi-structured)
- [x] Dimensionality Reduction separated from Feature Selection
- [x] Specialized Layer (Time-series, Multimodal, Graph, Geospatial)
- [x] Production Layer (Observability, Feature Store, Pipeline, Governance)
- [x] AI/LLM Specialization
- [x] Inline cross-references
- [x] Separated study tracks

---

**Version:** Final v1.0  
**Status:** ✅ Ready as Master Reference
