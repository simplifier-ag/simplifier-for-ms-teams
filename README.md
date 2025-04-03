# simplifier-for-ms-teams
A MS Teams App to integrate Simplifier Launchpad / AdminUI in Teams

Using the Simplifier Teams App
This guide explains how to install and use the Simplifier Teams App in Microsoft Teams. The app embeds a single Simplifier instance (e.g., Production) into a personal Teams tab for quick access — directly within your Microsoft Teams workspace.

Overview
The Simplifier Teams App is a lightweight Microsoft Teams Tab App that allows users to access a predefined Simplifier instance without leaving Teams. This is perfect for:

Simplifying access to your main Simplifier environment

Reducing context-switching between browser tabs and tools

Improving adoption of Simplifier within Teams

What You’ll Get
Once installed, the app will:

Appear in your Teams sidebar

Load the specified Simplifier URL directly inside Teams

Enable login and full functionality (if Simplifier allows embedding in iframes)

Installation Guide
1. Clone or Download the App
git clone https://github.com/your-org/simplifier-teams-app.git
Or download the .zip package directly from GitHub.

2. Update the Manifest File
Open manifest.json in a code editor and locate the following fields:

Field	Set This To
contentUrl	The URL of your Simplifier instance (e.g., https://simplifier.example.com)
websiteUrl	Same as contentUrl
validDomains	Add the domain of your Simplifier instance (e.g., simplifier.example.com)
name.short	"Simplifier" or your preferred name
description.short	e.g., "Access Simplifier inside Teams"
3. Create Your App Package
The Teams app package is a .zip file containing:

manifest.json

color-icon.png (192x192px)

outline-icon.png (32x32px)

Icons are required and must be PNG format.

Compress these three files into a .zip archive.

4. Upload to Microsoft Teams
Open Microsoft Teams

Click Apps > Manage your apps

Select Upload a custom app

Upload your .zip file

Once uploaded, the app will appear under your personal apps.

Using the App
Open the app from the Teams sidebar

Your Simplifier instance will load inside a tab

Log in and begin using Simplifier — no separate browser needed

Requirements
HTTPS hosting for your Simplifier instance

Embedding support: Ensure the Simplifier server allows embedding (i.e., no X-Frame-Options: DENY or restrictive Content-Security-Policy)

Microsoft Teams (desktop or web)

FAQs
Q: Can I link to different environments?
A: This version links to one instance only. For multiple environments, you can create and upload separate app packages (e.g., "Simplifier Dev", "Simplifier QA").

Q: Can I publish this company-wide?
A: Yes. Ask your Microsoft 365 Admin to publish it to your organization's App Catalog.

Q: Does this require backend code?
A: No. The app is entirely frontend and based on a static manifest.json with a contentUrl.

Support
For questions or help with setup, reach out to your internal IT team or the Simplifier administrator.
