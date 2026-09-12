# Free Dataset and Data-Source Plan

## Primary datasets
### 1. CIC-IDS2017
Canadian Institute for Cybersecurity dataset containing benign traffic and common attacks with PCAPs and labeled flow CSVs. Good first benchmark for supervised detection and flow analytics. Official source: https://www.unb.ca/cic/datasets/ids-2017.html

### 2. UNSW-NB15
Contains normal and synthetic contemporary attack traffic, PCAP/BRO/Argus/CSV data, 49 engineered features and nine attack categories. Official source: https://research.unsw.edu.au/projects/unsw-nb15-dataset

### 3. CTU-13
Thirteen botnet scenarios with labeled botnet, command-and-control, normal and background traffic. Useful for botnet/C2 detection and correlation. Official source: https://www.stratosphereips.org/datasets

## Supporting data sources
### 4. Zeek logs
Use Zeek-generated formats such as `conn.log`, `dns.log`, `http.log`, `ssl.log`, `ssh.log`, `files.log`, `notice.log` and `intel.log` to develop the ingestion/normalization layer. Official documentation: https://docs.zeek.org/en/current/reference/logs/index.html

### 5. MITRE ATT&CK
Use ATT&CK techniques/tactics as the semantic knowledge layer for detection mapping, investigation context and SOC assessment. Prefer the official ATT&CK/STIX data and cite the exact version used in experiments.

## Initial dataset strategy
**Phase 1:** CIC-IDS2017 CSV subset for a quick reproducible detection benchmark.

**Phase 2:** UNSW-NB15 for cross-dataset evaluation and generalization.

**Phase 3:** CTU-13 for botnet/C2 scenarios.

**Phase 4:** Zeek-style logs for realistic SIEM ingestion and event normalization.

## Data governance
Do not commit downloaded datasets or potentially sensitive raw logs to GitHub. Store only small synthetic samples, schemas, feature descriptions and download instructions under `data/README.md` unless a dataset license explicitly permits redistribution.

## Evaluation Metrics
Accuracy alone is insufficient. Track precision, recall, F1, false-positive rate, detection latency, throughput, case-resolution time and response success rate. For imbalanced security data, emphasize precision/recall, F1, PR-AUC and per-class results.
