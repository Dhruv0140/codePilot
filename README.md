<div align="center">
<h1>
⚡ CodePilot
</h1>
<p>
<strong>
An AI-powered code generation tool that helps you build web apps faster using natural language.
</strong>
</p>
<p>
Describe what you want to build, and CodePilot instantly generates working code directly in your browser.
</p>
<br />
<p>
<img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT" />
<img src="https://img.shields.io/badge/pnpm-v9.x-orange.svg" alt="pnpm" />
<img src="https://img.shields.io/badge/React-v18.x-blue.svg" alt="React" />
<img src="https://img.shields.io/badge/Node.js-v18.x-green.svg" alt="Node.js" />
</p>
</div>

📖 Table of Contents

✨ Features

🛠️ Tech Stack

🚀 Getting Started

🐳 Docker Deployment

🧩 Project Structure

💡 Future Improvements

🏷️ License

✨ Features

🧠 AI-Powered: Generate code from simple, natural language text prompts.

⚡ Real-time Preview: Instantly see a live preview of the code you generate.

🎨 Modern UI: Built with React, TypeScript, and TailwindCSS for a sleek, responsive interface.

💾 No Setup Required: Works directly in the browser—no complex installation needed.

🐳 Docker Support: Easily deploy your own instance with the included Dockerfile.

🔗 Open-Source: Fully open-source and customizable to fit your needs.

🛠️ Tech Stack

Area

Technology

Frontend

React (Vite + TypeScript)

Backend

Node.js (Runtime)

Styling

TailwindCSS

AI Engine

Bolt SDK / OpenAI

Build

Vite

Package

pnpm

Container

Docker

🚀 Getting Started

Follow these steps to get a local copy up and running.

Clone the repository:

git clone [https://github.com/Dhruv0140/CodePilot.git](https://github.com/Dhruv0140/CodePilot.git)


Navigate to the project directory:

cd CodePilot


Install dependencies:
(Using pnpm as specified in the tech stack)

pnpm install


Run the development server:

pnpm dev


Open your browser:
Navigate to http://localhost:5173.

🐳 Docker Deployment

You can also run CodePilot using Docker for a self-contained environment.

Build the Docker image:

docker build -t codepilot .


Run the container:

docker run -d -p 5173:5173 codepilot


Open your browser:
Once running, navigate to http://localhost:5173.

Example Dockerfile

Here is the Dockerfile used for the build:

# Use an official Node.js runtime as a parent image
FROM node:18-alpine

# Set the working directory in the container
WORKDIR /app

# Copy package.json and pnpm-lock.yaml
COPY package.json pnpm-lock.yaml ./

# Install pnpm and dependencies
RUN npm install -g pnpm && pnpm install

# Copy the rest of the application source code
COPY . .

# Build the app for production
RUN pnpm build

# Expose the port the app runs on
EXPOSE 5173

# Define the command to run the app
CMD ["pnpm", "preview", "--host"]


🧩 Project Structure

Here is an overview of the project's file structure:

CodePilot/
│
├── src/
│   ├── components/   # Reusable UI components
│   ├── pages/        # Page layouts
│   ├── assets/       # Static images and icons
│   ├── App.tsx       # Main application component
│   └── main.tsx      # React entry point
│
├── public/           # Public files and favicon
│
├── .gitignore        # Files to ignore by Git
├── Dockerfile        # Docker container configuration
├── package.json      # Project metadata and dependencies
├── pnpm-lock.yaml    # Lockfile for pnpm
├── README.md         # You are here!
└── tsconfig.json     # TypeScript configuration


💡 Future Improvements

[ ] Add support for more AI models (e.g., Gemini, Claude).

[ ] Enable saving and downloading of generated projects.

[ ] Implement user authentication and cloud-based project storage.

[ ] Continuously improve code generation accuracy and speed.

🏷️ License

This project is for academic and learning purposes.