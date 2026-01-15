# Cloud Resume & Project Portfolio

This is the source code behind **[dustinumphress.com](https://dustinumphress.com)**.

It started as a standard **Cloud Resume Challenge** implementation (AWS SAM, DynamoDB, Python Lambda backend) but has evolved into a home for my other engineering projects too.

## What's Under the Hood?

-   **Frontend**: Vanilla HTML/CSS. No frameworks, no build steps (except the deployment pipeline). Fast and simple.
-   **Backend**: AWS Lambda (Python 3.12) + DynamoDB for the view counter.
-   **Infrastructure**: AWS SAM (Serverless Application Model) because clicking around the console is for amateurs (and connection debuggers).
-   **CI/CD**: GitHub Actions. Push to `main` -> Tests run -> Infrastructure updates -> Site deploys to S3/CloudFront.

## Key Projects

### 1. [Medical Compliance Engine](https://dustinumphress.com/hallucination-free-medical-compliance-engine/)
A "serious business" project. It's a deterministic auditing system for medical claims that uses LLMs *only* for explanation, blocking them from hallucinating rules.

### 2. [Satisfactory on AWS](https://dustinumphress.com/satisfactory-on-aws/)
A "fun business" project. Running a dedicated game server on AWS without going broke. Uses event-driven architecture to shut itself down when nobody is playing.

## Local Dev

If you really want to run this locally:

```bash
# Backend
cd backend
pip install -r requirements.txt
pytest

# Frontend
# Just open index.html in a browser. It's that simple.
```

---
*Built by Dustin Umphress. Deployed on AWS.*
