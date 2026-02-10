# Microsoft Sentinel Threat Intelligence Lab (TI Enrichment & MITRE ATT&CK)

This project demonstrates how **Threat Intelligence (TI)** is integrated into **Microsoft Sentinel** to enrich authentication logs, create detections, and map alerts to the **MITRE ATT&CK framework**.

The lab focuses on **SOC detection engineering fundamentals**, including log ingestion, threat intelligence enrichment using KQL, analytics rule creation, and MITRE ATT&CK mapping.

All activities were performed in a **controlled Azure lab environment**.

---

## Objectives

- Deploy Microsoft Sentinel on a Log Analytics workspace  
- Ingest Microsoft Entra ID (Azure AD) sign-in logs  
- Create a custom Threat Intelligence indicator  
- Enrich authentication logs using KQL joins  
- Configure analytics rules with MITRE ATT&CK mapping  
- Validate detection logic and monitoring workflow  

---

## Skills Demonstrated

- SIEM deployment and configuration  
- Threat intelligence lifecycle management  
- KQL query development and log enrichment  
- MITRE ATT&CK mapping  
- Detection engineering fundamentals  
- SOC-style monitoring and validation  

---

## Lab Environment

- **Cloud Platform:** Microsoft Azure  
- **SIEM:** Microsoft Sentinel  
- **Log Source:** Microsoft Entra ID (Sign-in Logs)  
- **Workspace:** Log Analytics Workspace  
- **Region:** Canada Central  

---

## Tools & Technologies Used

- Microsoft Azure Portal  
- Microsoft Sentinel  
- Microsoft Entra ID  
- Microsoft Defender Threat Intelligence  
- Log Analytics Workspace  
- Kusto Query Language (KQL)  
- MITRE ATT&CK Framework  

---

## Project Walkthrough

### 1. Resource Group Creation
A dedicated resource group was created to logically organize Sentinel resources.
  
📸 Screenshot:

![Resource group created](screenshots/01_resource_group_created.png)


---

### 2. Log Analytics Workspace Setup
A Log Analytics workspace was created to store and query security logs. 

📸 Screenshot:

![Log Analytics workspace created](screenshots/02_log_analytics_workspace_created.png)


---

### 3. Microsoft Sentinel Enabled
Microsoft Sentinel was enabled on the Log Analytics workspace.

📸 Screenshot:

![Microsoft Sentinel enabled](screenshots/03_sentinel_enabled.png)


---

### 4. Microsoft Entra ID Data Connector
The Microsoft Entra ID data connector was enabled to ingest sign-in logs.

📸 Screenshot:  
`04_entra_data_connector_enabled.png`

---

### 5. Sign-in Log Generation & Validation
Multiple sign-in events were generated and verified using KQL to confirm log ingestion.

📸 Screenshot:  
`05_signinlogs_data_visible.png`

---

### 6. Threat Intelligence Indicator Creation
A manual IP-based Threat Intelligence indicator was created for lab testing purposes.

📸 Screenshot (IP blurred):  
`06_ti_indicator_created_blurred.png`

---

### 7. Log Enrichment Using KQL
Sign-in logs were enriched by joining authentication events with Threat Intelligence indicators using KQL.

📸 Screenshot:  
`07_enrichment_join_results.png`

---

### 8. Analytics Rule with MITRE ATT&CK Mapping
A Threat Intelligence analytics rule was enabled using a Microsoft-provided rule template with MITRE ATT&CK tactics and techniques.

📸 Screenshot:  
`08_rule_template_mitre_mapping.png`

---

### 9. Analytics Rule Enabled
The analytics rule was successfully created, enabled, and verified.

📸 Screenshot:  
`09_analytics_rule_created_mitre.png`

---

### 10. Incident Monitoring
The Incidents dashboard was monitored after rule deployment.

During the lab timeframe, **no incidents were generated**, as no sign-in events matched the threat intelligence indicator.  
This reflects real-world SOC environments where detections depend on live telemetry and exact indicator matches.

📸 Screenshot:  
`10_incidents_list_no_matches.png`

---

## Queries Included

- `01_signinlogs_check.kql`  
  Used to validate Microsoft Entra ID sign-in log ingestion.

- `02_ti_enrichment_join.kql`  
  Used to enrich sign-in logs with Threat Intelligence indicators.

---

## Security Outcomes

- Microsoft Sentinel successfully deployed  
- Identity logs ingested and validated  
- Threat Intelligence indicator lifecycle demonstrated  
- Log enrichment logic verified using KQL  
- MITRE ATT&CK mapping applied to detections  
- Monitoring workflow validated without false positives  

---

## Data Privacy Note

This assessment was performed in a controlled lab environment.  
All IP addresses and indicators are **masked or redacted**.  
No personal, organizational, or production data is included.

---

## Author

**Umme Farva**  
Cybersecurity Analyst  
