# ☁️ SaaS Management Workflows

> Automate the full lifecycle of SaaS tools across your org - from provisioning licenses to auditing access and tracking costs - all without leaving n8n.

---

## 🔌 Integrations

These workflows are built to work with:

| Tool | Used for |
|---|---|
| ![Google Workspace](https://img.shields.io/badge/Google_Workspace-4285F4?style=flat&logo=google&logoColor=white) | User & license management, Drive, Gmail |
| ![Microsoft 365](https://img.shields.io/badge/Microsoft_365-D83B01?style=flat&logo=microsoft&logoColor=white) | Azure AD users, Teams, SharePoint |
| ![Okta](https://img.shields.io/badge/Okta_/_Azure_AD-00297A?style=flat&logo=okta&logoColor=white) | Identity, SSO, access policies |
| ![Slack](https://img.shields.io/badge/Slack_/_Teams-4A154B?style=flat&logo=slack&logoColor=white) | Notifications, approval requests, alerts |

---

## 🚀 Getting Started

### 1. Import a workflow

1. Open your n8n instance
2. Go to **Workflows → Import from file**
3. Select the `.json` file you want to use
4. Set up credentials (see below)
5. Activate ✅

### 2. Configure credentials

Each workflow uses one or more of the following credential types. Set them up in **n8n → Credentials** before activating:

- **Google Workspace** - OAuth2 via Google Cloud Console (requires Admin SDK scope)
- **Microsoft 365** - OAuth2 via Azure App Registration
- **Okta** - API Token from your Okta Admin Console
- **Slack / Teams** - Bot Token (Slack) or Incoming Webhook (Teams)

### 3. Look for `⚠️ CONFIGURE ME` nodes

Each workflow has sticky notes and nodes marked with `⚠️ CONFIGURE ME` where you need to plug in:
- Your domain (e.g. `yourcompany.com`)
- Org-specific IDs, group names, or email addresses
- Notification channel names or webhook URLs

---

## 💡 Tips & Best Practices

- **Run audits on a schedule** - the access review and usage tracking workflows work best as weekly or monthly cron jobs
- **Use the approval step** - license provisioning/deprovisioning workflows include an optional Slack/Teams approval gate before making changes; don't skip it in production
- **Log everything** - all workflows write to a log node by default; connect it to your preferred storage (Airtable, Google Sheets, Notion, etc.)
- **Test in dry-run mode first** - set the `DRY_RUN` variable to `true` to simulate runs without making real changes

---

*Part of [n8n-it-workflows](../README.md) - built by IT people, for IT people. ⚙️*
