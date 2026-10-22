# Automated DevSecOps CI/CD Pipeline

## Project Overview
As part of my cybersecurity training, I implemented an automated DevSecOps CI/CD pipeline using GitHub Actions. I utilized a purposely vulnerable application (OWASP NodeGoat) to demonstrate how automated security gates can prevent flawed code from reaching production.

## Technical Implementation
- **Workflow Automation:** Configured a GitHub Actions `.yml` workflow to trigger automatically on code pushes.
- **Vulnerability Scanning:** Integrated Aqua Security's **Trivy** scanner into the pipeline to analyze the repository filesystem and library dependencies for known CVEs.
- **Security Gates:** Enforced a strict failure condition, configuring the pipeline to block deployment automatically if vulnerabilities with a `HIGH` or `CRITICAL` severity score were detected.

## Results
The automated pipeline successfully analyzed the codebase and triggered the security gate. It identified 57 total vulnerabilities (45 HIGH, 12 CRITICAL) in the legacy dependencies, effectively blocking the vulnerable code from progressing.

### Proof of Execution
<img width="1340" height="682" alt="Screenshot 2026-10-21 220040" src="https://github.com/user-attachments/assets/1cd2d4db-f021-4a79-947d-dd96f8270fe2" />
