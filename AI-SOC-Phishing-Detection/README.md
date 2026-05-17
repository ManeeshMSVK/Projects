# AI-Driven SOC Assistant for Phishing Detection
![ChatGPT](https://img.shields.io/badge/ChatGPT-GPT--4-74aa9c?logo=openai&logoColor=white)
![Gemini](https://img.shields.io/badge/Gemini-AI-4285F4?logo=google&logoColor=white)
![Copilot](https://img.shields.io/badge/Microsoft-Copilot-0078D4?logo=microsoft&logoColor=white)
![Claude](https://img.shields.io/badge/Claude-Anthropic-D97757?logoColor=white)
![MITRE ATT&CK](https://img.shields.io/badge/MITRE-ATT%26CK-red)
![SOC](https://img.shields.io/badge/SOC-Blue%20Team-1D9E75?logoColor=white)
![Prompt Engineering](https://img.shields.io/badge/Prompt-Engineering-purple)

## Project Overview

An end-to-end AI-augmented SOC workflow that detects phishing emails, extracts Indicators of Compromise (IOCs), maps threats to MITRE ATT&CK, and auto-generates structured incident reports — using ChatGPT, Gemini, and Microsoft Copilot.

**Built as a hands-on demonstration of how AI tools accelerate real SOC operations**, reducing manual phishing analysis time and producing consistent, structured threat intelligence outputs.

| What | Detail |
|------|--------|
| Role simulated | SOC Analyst (Tier 1) |
| Emails analyzed | 5+ phishing samples |
| AI tools used | ChatGPT, Gemini, Copilot, Claude |
| Output format | Structured incident report (IOCs, risk level, mitigation) |
| MITRE mapping | T1566.001 — Spearphishing Attachment |

## How to Use This Project

This project does not require any installation. All AI analysis was performed using browser-based tools.

### Step 1 — Open the prompt file
Open `1_Prompt_Engineering.docx` to view the 3 prompt templates used for detection, incident reporting, and awareness content.

### Step 2 — Test with your own email sample
Copy any suspicious email text. Paste it into ChatGPT, Gemini, or Copilot using the prompts from Step 1. Compare the outputs.

### Step 3 — Review the analysis outputs
Open `2_AI_Analysis.docx` to see side-by-side comparison of ChatGPT, Gemini, and Copilot outputs for the test phishing email.

### Step 4 — View the generated incident report
Open `3_Incident_Report.docx` to see the final SOC-standard report generated from AI analysis.

### Prerequisites
- Access to ChatGPT (free tier works)
- Access to Google Gemini (free)
- Access to Microsoft Copilot (free via Edge browser)
- No coding required

## 🧠 Tools Used
- ChatGPT
- Gemini
- Microsoft Copilot
- Claude

## ⚙️ Workflow
Suspicious Email → AI Analysis → Phishing Detection → Incident Report → Awareness Presentation

## 🚨 Scenario
A user receives a suspicious email claiming account suspension and requesting immediate verification.

## Key Features

### 1. Multi-model AI phishing analysis
Analyzed the same phishing email across ChatGPT, Gemini, and Copilot simultaneously. Compared outputs for detection accuracy, IOC extraction quality, and response structure. **Finding: ChatGPT produced the most detailed IOC list; Gemini had the fastest risk classification.**

### 2. Structured prompt engineering for SOC workflows
Designed 3 purpose-built prompt types:
- **Detection prompt** — asks the model to identify phishing indicators, attacker intent, and risk level
- **Incident report prompt** — generates a structured SOC report with IOCs, risk score, and mitigation steps
- **Awareness prompt** — creates user-facing education content explaining the red flags found

### 3. IOC extraction and MITRE ATT&CK mapping
Extracted the following IOCs from the test email:
- Suspicious URL: `http://secure-login-alert.com` (non-official domain)
- Social engineering: urgency language + generic greeting ("Dear User")
- Missing: company branding, official sender domain

**MITRE ATT&CK mapping:** T1566.001 (Spearphishing Link) — Initial Access tactic

### 4. AI-generated incident report (SOC-standard format)
Auto-generated reports include:
- Incident summary
- IOC list with evidence
- Risk level (High/Medium/Low) with justification
- Recommended mitigation steps

### 5. Red Flag Awareness Presentation
Created a visual "Red Flags in the Email" slide for security awareness training, demonstrating how to educate non-technical users about phishing indicators.

## Results & Outcomes

| Metric | Result |
|--------|--------|
| Phishing emails analyzed | 5 samples |
| AI models compared | 3 (ChatGPT, Gemini, Copilot) |
| Prompt types engineered | 3 (Detection, Report, Awareness) |
| IOCs extracted per email | 4–6 indicators |
| Report generation time (AI-assisted) | ~2 minutes vs ~15 minutes manual |
| MITRE ATT&CK techniques mapped | 3 techniques |

**Key finding:** AI-assisted phishing analysis reduced report generation time by approximately 85% compared to manual SOC documentation, while producing consistent, structured threat intelligence output across all test samples.

## 📸 Screenshots

**Prompt Engineering**

![Prompt Engineering](Screenshots/prompt-engineering.png)

**AI Analysis**

![AI Analysis](Screenshots/ai-analysis.png)

**Incident Report**

![Incident Report](Screenshots/incident-report.png)

**Workflow**

![Workflow](Screenshots/workflow-diagram.png)

**Awareness**

![Awareness](Screenshots/awareness-slides.png)

## MITRE ATT&CK Coverage

| Tactic | Technique | ID | How detected in this project |
|--------|-----------|-----|------------------------------|
| Initial Access | Spearphishing Link | T1566.001 | Suspicious URL in email body |
| Initial Access | Spearphishing Attachment | T1566.002 | Urgency-based social engineering |
| Credential Access | Phishing for Information | T1598 | Request for account verification |

## What I Learned

**Prompt engineering is a force multiplier in SOC work.**
A well-structured prompt consistently produced structured, actionable output — while a vague prompt returned generic analysis. The difference in output quality between "Is this email phishing?" and a role-based detection prompt with specific output requirements was significant.

**Multi-model comparison revealed tool-specific strengths.**
- ChatGPT: Best for detailed IOC extraction and structured report format
- Gemini: Fastest response, good at risk classification, less detail in IOCs
- Copilot: Good integration with enterprise context, most conservative risk ratings

**What I would add in a real SOC environment:**
- Automated email ingestion via API (no manual copy-paste)
- Integration with VirusTotal API to verify suspicious URLs
- Splunk integration to log AI-generated IOCs directly into SIEM dashboards
- A feedback loop where analyst corrections improve future prompt accuracy

## Skills Demonstrated

`Prompt Engineering` `Phishing Analysis` `IOC Extraction` `MITRE ATT&CK` `Incident Report Writing` `Multi-LLM Comparison` `SOC Workflow Design` `Security Awareness Content`

## 🎯 Conclusion
This project demonstrates how AI tools can assist cybersecurity analysts in detecting phishing emails, analyzing threats, and improving security workflows.

## 🔗 Project Link
[Click here to view the full project](https://github.com/ManeeshMSVK/Projects/tree/main/AI-SOC-Phishing-Detection)
