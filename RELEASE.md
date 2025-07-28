# Release Guide

Simple steps to publish ml-graphy using GitHub releases.

## Prerequisites

1. **Set up PyPI API Token**:
   - Go to [PyPI Account Settings](https://pypi.org/manage/account/)
   - Create an API token
   - Copy the token (starts with `pypi-`)

2. **Add Token to GitHub Secrets**:
   - Go to your GitHub repository
   - Settings → Secrets and variables → Actions
   - Click "New repository secret"
   - Name: `PYPI_API_TOKEN`
   - Value: Your PyPI token

## Publishing Process

1. **Update Version** (if needed):
   ```toml
   # In pyproject.toml
   version = "0.1.1"  # Increment version
   ```

2. **Commit and Push Changes**:
   ```bash
   git add .
   git commit -m "Release v0.1.1"
   git push origin main
   ```

3. **Create GitHub Release**:
   - Go to your GitHub repository
   - Click "Releases" → "Create a new release"
   - Tag: `v0.1.1` (match your version)
   - Title: `Release v0.1.1`
   - Description: Describe changes
   - Click "Publish release"

4. **Automatic Publishing**:
   - GitHub Actions will automatically:
     - Run tests across Python versions
     - Build the package
     - Publish to PyPI
   - Check the "Actions" tab to monitor progress

## Verification

After successful publishing:
```bash
pip install ml-graphy
```

## Version Management

Follow semantic versioning:
- `0.1.1` → Bug fixes
- `0.2.0` → New features
- `1.0.0` → Major release
