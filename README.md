# icd10-medical-coding-analytics
healthcare standards analytics — ICD10 SNOMED LOINC RxNorm FHIR R4

# ICD-10 Medical Coding Analytics — Synthea FHIR R4
Healthcare interoperability project analyzing clinical data using 

industry-standard medical coding systems across 1,180 synthetic patients.

## Overview

This project explores how healthcare data is standardized and analyzed 
using real-world coding systems used in US hospitals, payers, and EHR 
platforms. Built using Synthea synthetic FHIR R4 data — no real patient 
data, fully HIPAA-safe.

The analysis covers the full clinical data lifecycle — from raw FHIR 
resources through terminology mapping, lab standardization, and medication 
coding, and population health insights.

---

## Standards Covered

| Standard | Purpose | Records Analyzed |
|---|---|---|
| HL7 FHIR R4 | Interoperability & data exchange | All resources |
| SNOMED-CT | Clinical condition terminology | 8,766 conditions |
| ICD-10-CM | Diagnosis coding & billing | 4,327 mapped codes |
| LOINC | Lab results & vitals standardization | All observations |
| RxNorm | Medication naming & e-prescribing | All prescriptions |
| HIPAA | Privacy — Safe Harbor approach | Synthetic data only |

---

## What's Inside

**Section 1 — Data Loading**
Loads 1,180 Synthea FHIR R4 patient bundles and inventories all 
resource types across the dataset.

**Section 2 — SNOMED-CT to ICD-10 Crosswalk**
Maps SNOMED-CT clinical terminology to ICD-10-CM diagnosis codes — 
the same process used in production EHR systems like Epic and Cerner 
when exchanging data between clinical and billing systems.

**Section 3 — ICD-10 Disease Burden Analysis**
Analyzes population-level disease patterns using ICD-10 chapter 
classifications. Identifies top diagnoses, chronic disease prevalence, 
and onset trends over time.

**Section 4 — LOINC Lab & Vitals Standardization**
Extracts and categorizes LOINC-coded observations including vitals, 
metabolic panels, lipid panels, CBC, renal function, and liver function. 
Visualizes distributions against clinical reference ranges.

**Section 5 — RxNorm Medication Analytics**
Analyzes prescription patterns by drug class and therapeutic category. 
Covers cardiovascular, diabetes, mental health, respiratory, and 
antibiotic medications with trend analysis over time.

**Section 6 — Standards Coverage Summary**
End-to-end summary of all standards demonstrated, data volumes 
processed, and patient clinical complexity metrics.

---

## Key Findings

- Most common diagnosis: Viral Infection (J09.X9) — 1,237 patients
- Highest disease burden: Respiratory conditions
- Most prescribed category: Cardiovascular medications
- SNOMED → ICD-10 mapping coverage: 49.4% (4,327 of 8,766 conditions)
- Average conditions per patient: varies across chronic disease cohorts

---

## Tech Stack
Python 3.10
pandas
numpy
matplotlib
seaborn
json
pathlib

## Data Source

**Synthea™** — Synthetic Patient Population Simulator by The MITRE Corporation  
👉 synthea.mitre.org

---

## How to Run

```bash
# Clone the repo
git clone https://github.com/nipa-analytics/icd10-medical-coding-analytics.git
cd icd10-medical-coding-analytics

# Create environment
conda create -n fhir_env python=3.10
conda activate fhir_env

# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Download Synthea data
# Go to synthea.mitre.org/downloads
# Download FHIR R4 sample → place JSON files in data/fhir/fhir/

# Launch notebook
jupyter notebook
# Open: icd10_medical_coding_analytics.ipynb
```

---

## Output Charts

| File | Description |
|---|---|
| `icd10_disease_burden.png` | Top ICD-10 diagnoses + disease burden by chapter |
| `loinc_vitals_dashboard.png` | 12-panel vitals & labs with clinical reference ranges |
| `loinc_category_summary.png` | LOINC category distribution |
| `rxnorm_medication_dashboard.png` | Prescription patterns by drug class |
| `standards_summary.png` | Records processed per standard |
| `patient_complexity.png` | Conditions, meds, observations per patient |

---

## Related Projects

- [FHIR Healthcare Analytics](https://github.com/nipa-analytics/fhir-healthcare-analytics)
- [Patient Segmentation — MIMIC-IV](https://github.com/nipa-analytics/patient-segmentation-mimic-iv-)
- [30-Day Readmission Risk — MIMIC-IV](https://github.com/nipa-analytics/30-Day-Readmission-Risk-MIMIC-IV)
- [ICU Deterioration Prediction](https://github.com/nipa-analytics/ICU-Deterioration-Prediction)

---

## Author

**Nipa Shah** — Data Scientist | Healthcare Analytics | AI/ML  
📍 Jersey City, NJ  
🔗 [LinkedIn](https://www.linkedin.com/in/nipa-s-486287382)  
🐙 [GitHub](https://github.com/nipa-analytics)  
📧 nipashah2311@gmail.com
