# Automated FP&A Budget Audit AI Agent (n8n + Gemini)

An automated AI agent built with **n8n** and **Google Gemini** that audits monthly Budget vs. Actuals financial data, detects key variances, and delivers structured executive insights for CFO decision-making.

## Workflow Architecture

1. **Data Ingestion (Trigger):** Captures monthly financial inputs and variance data via an automated trigger/webhook.
2. **AI Financial Controller (`AI Agent` + `Google Gemini`):** Acts as a Senior FP&A Controller to quantify budget overruns/savings (in `$` and `%`), identify root-cause anomalies, and formulate prioritized CFO recommendations.
3. **Structured Output (`Structured Output Parser`):** Enforces a strict JSON schema (`statut_global`, `resume_executif`, `anomalies_cles`, `recommandations_cfo`) to eliminate formatting errors and guarantee reliable downstream parsing.
4. **Audit Logging (`Google Sheets`):** Automatically logs each structured audit into `Audit_FPA_Logs` across dedicated columns (`Date`, `Statut`, `Resume_Executif`, `Anomalies_Cles`, `Recommandations_CFO`) for historical tracking.
5. **Executive Alerting (`Gmail` - Optional):** Sends an instant English executive summary to stakeholders whenever critical budget variances are detected.

## Tech Stack
- **Orchestration:** n8n (Self-hosted)
- **LLM:** Google Gemini
- **Database & Reporting:** Google Sheets API
- **Notifications:** Gmail OAuth2 API


  <img width="1672" height="702" alt="image" src="https://github.com/user-attachments/assets/7cfc9399-4fc5-48ae-a051-6d28e61d6894" />

