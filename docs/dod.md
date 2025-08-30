# 📌 Definition of Done (DoD)

A task/feature is considered "Done" when:

1. **Code**
   - Code is written, reviewed, and merged into `main`
   - Code passes validation (linting, formatting, IaC validation)

2. **Testing**
   - App or infra changes tested successfully
   - No broken dependencies introduced

3. **Documentation**
   - README/docs updated with new instructions if needed
   - Architecture/runbook reflects changes

4. **Security**
   - IAM roles, SGs, and other configs follow least privilege
   - No hardcoded secrets in code or config files

5. **Deployment**
   - Feature works in deployed environment
   - Verified by at least one team member (peer review)
