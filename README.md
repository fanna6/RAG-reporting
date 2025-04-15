
# 🚀 Automated Status Report Generator

This repository automates the creation of weekly status reports in PowerPoint format using GitHub Actions and Python.

## 📁 Folder Structure

```
.
├── main.py                        # Script to generate the PowerPoint
├── weekly-reports/               # Folder for team YAML updates
│   └── project-apollo.yaml       # Example project status file
└── .github/
    └── workflows/
        └── generate-status-report.yml  # GitHub Action for automation
```

## 📝 How to Use

1. **Add YAML Updates**  
   Each team member should create a YAML file in `weekly-reports/`.  
   Example: `weekly-reports/project-apollo.yaml`

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

Make sure these packages are available (GitHub Actions handles this automatically):

- `python-pptx`
- `pyyaml`

## 🛠️ Customize

- Adjust the `cron` schedule in `.github/workflows/generate-status-report.yml` to change the report timing.
- Modify `main.py` to change slide formatting, content layout, etc.

---

Built for project managers who want to save time on manual reporting. 📊✨
