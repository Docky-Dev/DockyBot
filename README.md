# 📊 Fetch MrBeast Subs (via GitHub App)

**Fetch MrBeast Subs** is a GitHub Actions workflow that automatically retrieves the **YouTube subscriber count of MrBeast** every 5 minutes, using a **custom GitHub App**.
The data is then saved to a `mrbeast.json` file and pushed to the repository, allowing real-time tracking of the subscriber count.

---

## 🚀 How It Works

The script uses:

* **Mixerno API** → to fetch the subscriber count of MrBeast’s YouTube channel
* **GitHub App** → to authenticate and push updates automatically
* **GitHub Actions (cron)** → to run the task every 5 minutes without manual action

---

## ⚙️ Setup

### 1. Add Secrets to Your Repository

In your GitHub repository, go to **Settings → Secrets → Actions** and add the following three values:

| Secret Name       | Description                                        |
| ----------------- | -------------------------------------------------- |
| `APP_ID`          | Your GitHub App’s ID                               |
| `INSTALLATION_ID` | The installation ID of your App on your repository |
| `PRIVATE_KEY`     | The private key (in PEM format) of your App        |

---

## 📁 Output

A file named `mrbeast.json` containing the latest fetched value:

```json
{
  "subscriberCount": "268512345"
}
```

---

## 💡 Purpose

This project demonstrates how to:

* use a **GitHub App** inside a workflow,
* automate the update of external data,
* store and track real-time statistics directly within a GitHub repository.

---

## 👤 Author

**Project developed by [DevXCat](https://github.com/DevXCat)**
GitHub App used: **DockyBot**
