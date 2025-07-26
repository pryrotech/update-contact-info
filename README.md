# 📨 Update Contact Info Flow

This Power Automate flow helps organizations ensure staff contact details are current. It pulls data from SharePoint, compares it to Microsoft Entra ID (Azure AD) profiles, and sends reminder emails to users whose information hasn't been updated.

---

## 📂 Package Contents

| File Name             | Description |
|----------------------|-------------|
| `manifest.json`       | Basic metadata and flow asset paths |
| `definition.json`     | Complete flow logic, including triggers and actions |
| `apisMap.json`        | Connector-to-GUID mapping (sanitized) |
| `connectionsMap.json` | Connection references (sanitized) |

---

## 🔐 Sanitization Notes

All personal, tenant-specific, and environment-specific data (e.g. GUIDs, email addresses, SharePoint URLs) have been redacted using generic placeholders like:

- `REDACTED_EMAIL`
- `REDACTED_GUID_X`
- `REDACTED_CONN_X`
- `REDACTED_URL`

---

## ✨ Flow Highlights

- **Trigger Type**: Manual button
- **Connectors Used**: Office 365 Outlook, Microsoft Entra ID, SharePoint
- **Logic**:
  - Loops through AD group members
  - Retrieves matching SharePoint records
  - Compares names and details
  - Sends emails to non-updating users
  - Updates AD profiles for accurate entries

---

## 🛠️ Setup Instructions

1. Import the `.zip` package into Power Automate
2. Reconfigure connections using your tenant’s credentials
3. Adjust SharePoint site and list details
4. Optionally customize the email template and business logic

---

## 💡 Credits

Created by [Colby Pryor](https://github.com/pryrotech)  
Sanitized and documented with the help of Microsoft Copilot 😊

---

## 📜 License

You’re welcome to remix, reuse, and adapt under the [MIT License](https://opensource.org/licenses/MIT).

