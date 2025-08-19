# Deployment App Template

This repository provides a complete multi-platform deployment setup with GitHub Actions workflows for:

## 🚀 Deployment Platforms
- **Netlify** - Static sites and JAMstack applications
- **Heroku** - Web applications and APIs
- **AWS** - Cloud deployments (S3, Lambda, etc.)

## 📁 Project Structure
```
.
├── .github/workflows/     # GitHub Actions workflows
│   ├── deploy-netlify.yml # Netlify deployment
│   ├── deploy-heroku.yml  # Heroku deployment
│   └── deploy-aws.yml     # AWS deployment
├── src/                   # Source code
├── dist/                  # Build output
└── package.json          # Project dependencies
```

## ⚙️ Setup Instructions

### 1. Repository Secrets
Add these secrets in your GitHub repository settings:

**For Netlify:**
- `NETLIFY_AUTH_TOKEN` - Your Netlify personal access token
- `NETLIFY_SITE_ID` - Your Netlify site ID

**For Heroku:**
- `HEROKU_API_KEY` - Your Heroku API key
- `HEROKU_APP_NAME` - Your Heroku app name

**For AWS:**
- `AWS_ACCESS_KEY_ID` - Your AWS access key
- `AWS_SECRET_ACCESS_KEY` - Your AWS secret key
- `AWS_REGION` - Your AWS region (e.g., us-east-1)

### 2. Deployment Triggers
- **Automatic**: Push to `main` or `develop` branch
- **Manual**: Use workflow dispatch in GitHub Actions tab
- **Pull Request**: Preview deployments for PRs

### 3. Environment Configuration
Each workflow supports:
- Production deployments (main branch)
- Staging deployments (develop branch)
- Manual environment selection

## 🔧 Customization
1. Update build commands in workflow files
2. Modify deployment directories
3. Add environment-specific configurations
4. Configure notification settings

## 📝 Usage
1. Clone this repository
2. Add your application code to `src/`
3. Configure build scripts in `package.json`
4. Set up repository secrets
5. Push to trigger deployments

## 🤝 Contributing
This template is designed to be forked and customized for your specific deployment needs.