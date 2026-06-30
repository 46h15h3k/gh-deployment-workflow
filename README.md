# gh-deployment-workflow

A simple project demonstrating **Continuous Integration and Continuous Deployment (CI/CD)** using GitHub Actions to automatically deploy a static website to GitHub Pages.

## 🚀 How It Works

Whenever a change is pushed to the `index.html` file on the `main` branch, a GitHub Actions workflow automatically triggers and deploys the updated site to GitHub Pages — no manual steps needed.

## 📁 Project Structure

```
gh-deployment-workflow/
├── index.html                  # The static website
├── README.md                   # This file
└── .github/
    └── workflows/
        └── deploy.yml          # GitHub Actions CI/CD workflow
```

## ⚙️ Workflow Overview (`.github/workflows/deploy.yml`)

The workflow:
1. **Triggers** only when `index.html` is changed on a push to `main`
2. **Checks out** the repository code
3. **Deploys** the site to GitHub Pages using the official `actions/deploy-pages` action

## 🌐 Live Site

Once deployed, the site is accessible at:
```
https://<your-username>.github.io/gh-deployment-workflow/
```

## 🛠️ Setup Instructions

### 1. Enable GitHub Pages

- Go to your repository **Settings → Pages**
- Under **Source**, select **GitHub Actions**
- Save the settings

### 2. Push a Change to Trigger Deployment

Edit `index.html` and push to `main`:

```bash
git add index.html
git commit -m "Update site content"
git push origin main
```

### 3. Monitor the Workflow

- Go to the **Actions** tab in your repository
- Watch the `Deploy to GitHub Pages` workflow run
- Once complete, visit your GitHub Pages URL

## 📌 Key Concepts Learned

| Concept | Description |
|---|---|
| **CI/CD** | Automating build, test, and deploy on every relevant change |
| **GitHub Actions** | Event-driven automation platform built into GitHub |
| **Path filtering** | Triggering workflows only when specific files change (`paths:`) |
| **GitHub Pages** | Free static site hosting directly from a GitHub repository |
| **Permissions** | Granting workflows the right access (`pages: write`, `id-token: write`) |
