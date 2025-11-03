# ci-cd-testing-demo
Automating tasks using Pipelines 

# CI/CD Testing Demo

This project demonstrates automated testing in a CI/CD pipeline using GitHub Actions.

## Features
- ✅ Dockerfile linting with Hadolint
- ✅ Security scanning with Trivy
- ✅ Python unit tests with pytest
- ✅ Automated Docker builds

## Automated Tests

The pipeline runs on every push and includes:

1. **Dockerfile Lint**: Checks Dockerfile for best practices
2. **Security Scan**: Scans for vulnerabilities with Trivy
3. **Python Tests**: Runs unit tests with pytest
4. **Docker Build Test**: Builds and tests the Docker container

## Local Testing

### Run tests locally
```bash
pip install -r requirements.txt
pytest tests/ -v
```

### Lint Dockerfile locally
```bash
hadolint Dockerfile
```

### Build and run Docker container
```bash
docker build -t demo-app .
docker run -p 8080:80 demo-app
```

Then visit http://localhost:8080

## Project Structure
```
.
├── .github/
│   └── workflows/
│       └── test.yaml       # CI/CD pipeline definition
├── tests/
│   └── test_app.py         # Unit tests
├── app.py                  # Flask application
├── Dockerfile              # Docker configuration
├── requirements.txt        # Python dependencies
├── pytest.ini              # Pytest configuration
├── .hadolint.yaml          # Hadolint configuration
└── .gitignore              # Git ignore rules
```
```

**Why:** Good documentation helps others (and your future self) understand the project.

## Your Final Structure Should Look Like:
```
ci-cd-testing-demo/
├── .github/
│   └── workflows/
│       └── test.yaml          ✅ (you already have this)
├── tests/
│   └── test_app.py           ← CREATE
├── .gitignore                ← CREATE
├── .hadolint.yaml            ← CREATE
├── pytest.ini                ← CREATE
├── Dockerfile                ← CREATE
├── app.py                    ← CREATE
├── requirements.txt          ← CREATE
└── README.md                 ← UPDATE