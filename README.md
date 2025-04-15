# 📊 Automated Status Report Generator
Automatically generate project status reports in PowerPoint format from YAML updates using GitHub Actions and Python.
## ✨ Features
- Reads weekly updates from YAML files
- Automatically generates PowerPoint reports
- Scheduled with GitHub Actions (Fridays at 9am UTC)
- Downloadable from GitHub Action artifacts
## 🚀 Getting Started
- Clone this repo
- Add your project updates to `weekly-reports/*.yaml`
- Push to GitHub or trigger the workflow manually
- Download the PowerPoint report from GitHub Actions
## Working example
- Project: Psychometric assessment system integration.
- Status: 🟡 At Risk
- Summary: Vendor delays are impacting the integration timeline. Internal approvals also take time to obtain.
- Next_steps: Escalate to procurement, finalize new vendor. Ensure senior stakeholders are aware of timelines and time sensitivity on key strategic project.
- Risks: Senior stakeholders do not approve key details on time, budget has been exceeded, missed delivery deadline.
## ⚙️ How It Works
- The Python script (`main.py`) reads all YAML files in `weekly-reports/`
- It generates a PowerPoint slide per project
- The GitHub Action runs every Friday and uploads the `.pptx` file
## Can modify the following
- Update the cron time in `.github/workflows/generate-status-report.yml`
- Modify `main.py` to adjust slide format or data fields
## Contributing or issues
- Reach out for any feedback or issues.
- This was a bit of fun (as well as very serious!) as status reporting is the bane of many Project Manager's existence. Due to this, I wanted to see if a viable solution could be created via GitHub.
