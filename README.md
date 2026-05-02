# Audit Anomaly Detection - Kenya Public Procurement 2024

## Overview
This project applies machine learning to detect anomalies in Kenya's 2024 public procurement data published by the Public Procurement Regulatory Authority (PPRA).

## Data Source
- **Dataset**: Kenya PPRA Contract Awards 2024
- **Source**: Open Contracting Partnership Data Registry
- **Records**: 29,205 real government procurement contracts
- **Coverage**: National and County Governments

## Anomaly Types Detected
| Type | Count | Risk Level |
|---|---|---|
| Missing Supplier | 7,658 | High |
| Direct Procurement | 628 | High |
| Zero Value Contract | 243 | High |
| After Hours Entry | 345 | Medium |
| Round Number Fraud | 344 | Medium |
| Duplicate Invoice | 344 | Medium |

## Key Findings
- 591 high-risk contracts totalling KES 34.7 billion identified
- IsolationForest detected 1,461 anomalies vs 69 by Z-score alone
- Kenya Ports Authority accounts for highest spend concentration at KES 40+ billion
- July 2024 shows unusual spike in transaction volume

## Methods
- **Z-score**: Statistical threshold on contract amounts
- **IsolationForest**: Unsupervised ML anomaly detection across multiple features

## Tools Used
- Python 3.13
- pandas, numpy
- scikit-learn (IsolationForest)
- matplotlib, seaborn
- Jupyter Notebook

## Files
- `audit_anomaly_detection.ipynb` - full analysis notebook
- `audit_anomaly_detection.csv` - cleaned labelled dataset
- `audit_findings.csv` - findings with risk levels and recommended actions
- `chart1` to `chart7` - visualizations

## Author
Donie | Operations professional transitioning to Cloud/Data/Security engineering
