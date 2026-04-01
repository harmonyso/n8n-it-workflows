# 🔧 n8n-it-workflows

> A growing collection of ready-to-use n8n workflows built for IT teams. Stop doing repetitive tasks manually, automate them.

Whether you're onboarding a new hire, resetting an MFA token, or hunting down shadow IT, there's a workflow here for you. Import, tweak, ship.

---

## 📋 Table of Contents

- [Getting Started](#-getting-started)
- [Workflows](#️-workflows)
- [Contributing](#-contributing)

---

## 🚀 Getting Started

### Prerequisites

- [n8n](https://n8n.io/): self-hosted or cloud (v1.0+ recommended)
- Credentials configured for the services your workflows use (e.g. Active Directory, Google Workspace, Slack, Jira, etc.)

### How to import a workflow

1. Open your n8n instance
2. Go to **Workflows → Import from file**
3. Select the `.json` file from this repo
4. Configure any credentials or variables marked with `⚠️ CONFIGURE ME`
5. Activate and run 🎉

> **Tip:** Each workflow folder contains a `README.md` with setup notes, required credentials, and example inputs/outputs.

---

## 🗂️ Workflows

### 👤 Onboarding
Automate new hire setup end-to-end: create accounts, assign licenses, send welcome emails, and notify the team.

### 🚪 Offboarding
Revoke access, disable accounts, archive data, and notify relevant stakeholders when someone leaves.

### 🔑 Password Reset
Self-service or IT-triggered password resets with identity verification and audit logging.

### 📱 MFA Reset
Safely reset MFA/2FA tokens with an approval step to prevent unauthorized access.

### 🖥️ Hardware Checking & Fixing
Query device inventory, check compliance status, and trigger remote fixes or alerts.

### 🕵️ Shadow IT Detection
Detect unauthorized apps and services being used across your org and route alerts to the right team.

### ☁️ SaaS Management
Track SaaS subscriptions, audit user access, and automate license provisioning/deprovisioning.

### ➕ More coming soon...
Got a workflow idea? [Open an issue](../../issues) or submit a PR!

---

## 🤝 Contributing

Contributions are welcome and encouraged! Here's how to get involved:

### Submitting a workflow

1. Fork this repo
2. Create a branch: `git checkout -b workflow/your-workflow-name`
3. Add your workflow JSON to the appropriate category folder (or create a new one)
4. Include a `README.md` in the folder with:
   - What the workflow does
   - Required credentials/integrations
   - Any configuration steps
5. Open a Pull Request with a clear description

### Guidelines

- Keep workflows focused: one workflow, one job
- Use sticky notes inside n8n to document complex logic
- Sanitize any credentials or sensitive data before exporting
- Test your workflow before submitting

### Reporting issues or ideas

Found a bug or have a workflow idea? [Open an issue](../../issues): all feedback is appreciated.

---

## 📄 License

MIT: use it, fork it, improve it.

---

*Built by IT people, for IT people. ⚙️*
