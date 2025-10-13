# Org Repos Manifest and SBOM Collector

## Overview
This tool automates the collection of **manifest** and **SBOM (Software Bill of Materials)** files from a defined list of GitHub repositories across an organization. It’s designed to help security and DevOps teams centralize visibility into dependency data and software composition for compliance, auditing, and vulnerability management.

## Purpose
The primary goal of this application is to:
- Collect SBOM and manifest files (e.g., `package-lock.json`, `requirements.txt`, `sbom.json`) from repositories within a specified GitHub organization or list.
- Consolidate collected files into a structured dataset for analysis or storage.
- The top level flder called menifest, and each subfolder identifed teh repo name and it contained the collected sobm & manifest files
- Enable integration with security tooling for SBOM ingestion or inventory tracking.

## Prerequisites
Before running this tool, make sure the following are set up:

### 1. GitHub Personal Access Token (GHPAT_TOKEN) for Github Action run
You’ll need a GitHub Personal Access Token (PAT) with **read access** to the repositories you plan to scan.
- 1. Go to your repository on GitHub
- 2. Settings → Secrets and variables → Actions
- 3. New repository secret
- 4. Name: GHPAT_TOKEN
- 5. Value: your_github_personal_access_token_here

#### How to setup you github token:
- Go to [GitHub → Settings → Developer settings → Personal access tokens → Tokens (classic)](https://github.com/settings/tokens)
- Generate a new token with the following scopes:
  - `repo` (to read private repositories)
  - `read:org` (to access organization metadata)
