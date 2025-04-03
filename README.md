# simplifier-for-ms-teams

A Microsoft Teams App to integrate the **Simplifier Launchpad / AdminUI** directly into Microsoft Teams.

---

## 🧭 Using the Simplifier Teams App

This guide explains how to install and use the Simplifier Teams App in Microsoft Teams. The app embeds a single Simplifier instance (e.g., Production) into a personal Teams tab for quick access — directly within your Microsoft Teams workspace.

---

## 📌 Overview

The Simplifier Teams App is a lightweight Microsoft Teams Tab App that allows users to access a predefined Simplifier instance without leaving Teams. This is perfect for:

- ✅ Simplifying access to your main Simplifier environment  
- 🔄 Reducing context-switching between browser tabs and tools  
- 🚀 Improving adoption of Simplifier within Teams

---

## 🎯 What You’ll Get

Once installed, the app will:

- 📂 Appear in your Teams sidebar  
- 🌐 Load the specified Simplifier URL directly inside Teams  
- 🔐 Enable login and full functionality (if Simplifier allows embedding in iframes)

---

## 🛠 Installation Guide

### 1. Clone or Download the App

```bash
git clone https://github.com/your-org/simplifier-teams-app.git
```

Or download the `.zip` package directly from GitHub.

---

### 2. Update the Manifest File

Open `manifest.json` in a code editor and locate the following fields:

| Field               | Set This To                                                             |
|--------------------|--------------------------------------------------------------------------|
| `contentUrl`       | The URL of your Simplifier instance (e.g., `https://simplifier.example.com`) |
| `websiteUrl`       | Same as `contentUrl`                                                    |
| `validDomains`     | Domain of your Simplifier instance (e.g., `simplifier.example.com`)     |
| `name.short`       | `"Simplifier"` or your preferred name                                   |
| `description.short`| e.g., `"Access Simplifier inside Teams"`                                |

---

### 3. Create Your App Package

The Teams app package is a `.zip` file containing:

- `manifest.json`
- `color-icon.png` (192x192px)
- `outline-icon.png` (32x32px)

> 🎨 Icons must be in **PNG format** and the correct dimensions.

Compress these three files into a `.zip` archive.  
**Note**: Do *not* zip the folder — only the files!

---

### 4. Upload to Microsoft Teams

1. Open **Microsoft Teams**
2. Go to **Apps** → **Manage your apps**
3. Click **Upload a custom app**
4. Select and upload your `.zip` file

The app will now appear under your **personal apps**.

---

## 🚀 Using the App

1. Open the Simplifier app from the Teams sidebar  
2. Your Simplifier instance will load inside a tab  
3. Log in and begin using Simplifier — no separate browser needed  

---

## ✅ Requirements

- ✔️ HTTPS hosting for your Simplifier instance  
- ✔️ Embedding support (`X-Frame-Options` must not be `DENY`, and CSP must allow framing)  
- ✔️ Microsoft Teams (desktop or web client)

---

## ❓ FAQs

**Q: Can I link to different environments?**  
**A:** This version links to one instance only. For multiple environments, create and upload separate app packages (e.g., "Simplifier Dev", "Simplifier QA").

**Q: Can I publish this app company-wide?**  
**A:** Yes. Ask your Microsoft 365 Admin to publish it to your organization's App Catalog.

**Q: Does this require backend code?**  
**A:** No. The app is completely frontend-based and uses a static `manifest.json`.

---

## 🆘 Support

For questions or setup help, reach out to your internal IT team or the Simplifier administrator.
