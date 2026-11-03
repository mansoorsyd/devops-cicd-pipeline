# DevOps CI/CD Pipeline

![CI](https://github.com/mansoorsyd/devops-cicd-pipeline/actions/workflows/ci.yml/badge.svg)

A small Flask web app with a fully automated CI/CD pipeline.

## What it does
- Runs automated tests on every push and pull request
- Builds a Docker image of the app
- Publishes the image to GitHub Container Registry (ghcr.io)

## Tools used
Python, Flask, pytest, Docker, GitHub Actions

## Project structure
    app.py                    # Flask application
    tests/test_app.py         # Automated test
    Dockerfile                # Container build instructions
    .github/workflows/ci.yml  # CI/CD pipeline

## Run locally
    docker build -t demo-app .
    docker run -p 5000:5000 demo-app

Open http://localhost:5000 in your browser.

## What I learned
- How a CI/CD pipeline works from commit to published image
- Writing a Dockerfile that runs as a non-root user
- Using GitHub Actions and GITHUB_TOKEN
