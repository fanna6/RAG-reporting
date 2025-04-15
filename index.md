---
title: Automated Status Report Generator
layout: default
---

# 🚀 Automated Status Report Generator

This project automates the creation of weekly status reports in PowerPoint format using GitHub Actions and Python.

## 📁 Folder Structure

```
.
├── main.py
├── weekly-reports/
│   └── project-apollo.yaml
└── .github/
    └── workflows/
        └── generate-status-report.yml
```

## 📝 How to Use

1. **Add YAML Updates**  
   Each team member should create a YAML file in `weekly-reports/`.

   ```yaml
   project: Apollo CRM
   status: 🟡 At Risk
   summary: Vendor delays are impacting the integration timeline.
   next_steps: Escalate to procurement, finalize new vendor.
   risks: Budget overrun, missed delivery.
   ```

2. **GitHub Action**  
   Every Friday at 3 PM UTC, or on manual trigger, GitHub Actions will:
   - Run the Python script
   - Create a PowerPoint report
   - Upload it as an artifact

3. **Download the Report**  
   Navigate to **GitHub → Actions → Generate Status Report → Run → Artifacts** to download the PPTX file.

## 📦 Dependencies

- `python-pptx`
- `pyyaml`
