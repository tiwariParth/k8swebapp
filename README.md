# Simple Web App

A basic web application built with Node.js and Express.js, containerized using Docker, and deployed on a Kubernetes cluster using Kind.

## Features

- Express.js server serving a "Hello, World!" message.
- Dockerized for easy deployment.
- Kubernetes deployment configurations.

## Prerequisites

- Docker
- Kind
- kubectl

## Installation

1. Clone the repository:
git clone https://github.com/your-username/simple-web-app.git
cd simple-web-app


2. Build the Docker image:
docker build -t your-dockerhub-username/simple-web-app .


3. Push the Docker image to Docker Hub:
docker push your-dockerhub-username/simple-web-app


## Usage

1. Run the application locally:
node app.js


Access it at `http://localhost:3000`.

## Kubernetes Deployment

1. Create a Kind cluster:
kind create cluster --name my-kind-cluster


2. Deploy to Kubernetes:
kubectl apply -f k8s/deployment.yaml
kubectl apply -f k8s/service.yaml


3. Access the application:
kubectl port-forward service/simple-web-app-service 8080:80


Open `http://localhost:8080` in your browser.

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## License

MIT License. See the LICENSE file for details.
You can copy and paste this text into a README.md file in your project directory. Customize the placeholders like your-username and your-dockerhub-username with your actual details.
