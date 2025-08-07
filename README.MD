# Go CI/CD Example with GitHub Actions

This repository demonstrates a simple Go application using the Echo web framework, containerized with Docker, and integrated with GitHub Actions for continuous integration and deployment. Docker images are pushed to AWS Elastic Container Registry (ECR).

## Technologies Used

- **Golang** – Application language
- **Echo** – Web framework
- **Docker** – Containerization
- **GitHub Actions** – CI/CD automation
- **AWS Elastic Container Registry (ECR)** – Image storage

## Prerequisites

- Go installed (v1.18+ recommended)
- Docker installed and running
- AWS account with ECR access
- GitHub account

## Getting Started

1. **Clone the Repository**
   ```bash
   git clone https://github.com/reganputra/go-ci-cd.git
   cd go-ci-cd
   ```

2. **Run Locally**
   ```bash
   go run main.go
   ```
   The application should be accessible at `http://localhost:8080`.

3. **Build Docker Image**
   ```bash
   docker build -t go-ci-cd .
   ```

## Continuous Integration & Deployment

This project uses GitHub Actions to:

- Build and test your Go application on every push
- Build a Docker image
- Push the Docker image to AWS ECR

You can find the workflow configuration in `.github/workflows/`.

## Setting Up AWS ECR

1. Create an ECR repository in AWS.
2. Update your repository secrets in GitHub:
   - `AWS_ACCESS_KEY_ID`
   - `AWS_SECRET_ACCESS_KEY`
   - `AWS_REGION`
   - `ECR_REPOSITORY`

## License

This project is licensed under the MIT License.
