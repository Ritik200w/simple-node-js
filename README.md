Simple Node.js Web Application 🚀

This project demonstrates how to build and deploy a simple Node.js web application using Docker. The application is built using Express.js and Dockerized for container-based deployment.


    Table of Contents 📋

    
    Project Overview
    Prerequisites
    Installation
    Running the Application
    Dockerizing the Application
    Accessing the Application
    Important Notes

Project Overview 🌟

This project provides a simple "Hello, World!" Node.js application served by an Express.js server. It demonstrates how to containerize a Node.js app using Docker, making it easy to build, test, and deploy in any environment.
Prerequisites ⚙️

Make sure you have the following installed before running the project:

    Node.js: Download Node.js
    Docker: Get Docker

Installation 💻

    Clone the repository:

    bash

git clone https://github.com/<your-username>/simple-node-app.git
cd simple-node-app

Install dependencies:

bash

    npm install

Running the Application 🏃‍♂️

To start the application locally without Docker, use the following command:

bash

node app.js

The app will be running on http://localhost:3000.
Dockerizing the Application 🐳
Step 1: Build Docker Image

To create a Docker image for the app, run the following command:

bash

docker build -t simple-node-app .

Step 2: Run Docker Container

Run the application inside a Docker container:

bash

docker run -p 3000:3000 simple-node-app

The app should now be accessible at http://localhost:3000.
Accessing the Application 🌐

After running the Docker container, open your browser and visit:

bash

http://localhost:3000

You should see the "Hello, World!" message! 🎉
Important Notes ⚠️

    Node.js Version: The application uses the official node:14 Docker image. Ensure compatibility with Node.js 14.x.
    Ports: The container exposes port 3000. Ensure no other applications are using this port when you run the container.
    Dockerfile: The Dockerfile sets up a minimal container image, which installs dependencies and runs the application in a production-ready environment.
    .gitignore: The .gitignore file ensures that node_modules and unnecessary files like npm-debug.log are not included in the repository or Docker image.
