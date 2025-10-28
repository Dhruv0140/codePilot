<div align="center">
  <h1>⚡ CodePilot</h1>
  <p><strong>An AI-powered code generation tool that helps you build web apps faster using natural language.</strong></p>
  <p>Describe what you want to build, and CodePilot instantly generates working code directly in your browser.</p>
  <br />
  <p>
    <img src="https://img.shields.io/badge/license-MIT-blue.svg" alt="License: MIT" />
    <img src="https://img.shields.io/badge/pnpm-v9.x-orange.svg" alt="pnpm" />
    <img src="https://img.shields.io/badge/React-v18.x-blue.svg" alt="React" />
    <img src="https://img.shields.io/badge/Node.js-v18.x-green.svg" alt="Node.js" />
  </p>
</div>

---

## 📖 Table of Contents
- ✨ [Features](#-features)
- 🛠️ [Tech Stack](#️-tech-stack)
- 🚀 [Getting Started](#-getting-started)
- 🐳 [Docker Deployment](#-docker-deployment)
- 🧩 [Project Structure](#-project-structure)
- 💡 [Future Improvements](#-future-improvements)
- 🏷️ [License](#️-license)

---

## ✨ Features
- 🧠 **AI-Powered:** Generate code from simple, natural language text prompts.  
- ⚡ **Real-time Preview:** Instantly see a live preview of the generated code.  
- 🎨 **Modern UI:** Built with React, TypeScript, and TailwindCSS for a sleek, responsive interface.  
- 💾 **No Setup Required:** Works directly in the browser — no installation needed.  
- 🐳 **Docker Support:** Easily deploy your own instance with the included Dockerfile.  
- 🔗 **Open Source:** Fully customizable and free to use.

---

## 🛠️ Tech Stack

| Area | Technology |
|------|-------------|
| Frontend | React (Vite + TypeScript) |
| Backend | Node.js (Runtime) |
| Styling | TailwindCSS |
| AI Engine | Bolt SDK / OpenAI |
| Build | Vite |
| Package | pnpm |
| Container | Docker |

---

## 🚀 Getting Started

Follow these steps to get a local copy up and running.

### 1️⃣ Clone the repository
```bash
git clone https://github.com/Dhruv0140/CodePilot.git
cd CodePilot
```

### 2️⃣ Install dependencies
```bash
pnpm install
```
### 3️⃣ Run the development server
```bash
pnpm dev
```

### 4️⃣ Open your browser
Visit http://localhost:5173


## 🐳 Docker Deployment

You can also run CodePilot using Docker for a self-contained environment.

### 1️⃣ Build the Docker image
```bash
docker build -t codepilot .
```
### 2️⃣ Run the container
```bash
docker run -d -p 5173:5173 codepilot
```
### 3️⃣ Open your browser
```bash
Once running, visit http://localhost:5173
```
### 🧱 Example Dockerfile
```
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
```

## 🧩 Project Structure
``` text
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
```
## 💻 project workflow 
<img width="5656" height="3644" alt="diagram" src="https://github.com/user-attachments/assets/626f6997-f313-4664-8f5e-d9e0df3614cc" />


## 💡 Future Improvements

   Add support for more AI models (e.g., Gemini, Claude)

   Enable saving and downloading of generated projects

   Implement user authentication and cloud-based project storage

   Continuously improve code generation accuracy and speed

## 🏷️ License

This project is for academic and learning purposes.
