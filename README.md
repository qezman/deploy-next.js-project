# Next.js Authentication Deployment

![Next.js](https://img.shields.io/badge/Next.js-14-black)
![Node.js](https://img.shields.io/badge/Node.js-22-green)
![PM2](https://img.shields.io/badge/PM2-Process%20Manager-blue)
![Status](https://img.shields.io/badge/Deployment-Success-brightgreen)

## Project Overview

This project demonstrates the deployment of a **Next.js authentication application** in a production-ready environment.
The objective was to simulate a real-world deployment workflow including:

* Installing dependencies
* Building the application for production
* Running the production server
* Managing the application using **PM2**
* Verifying that the application runs successfully

The application was successfully built and deployed and is accessible locally via:

http://localhost:3000/dashboard

---

## Deployment Architecture

```
Developer Machine
       │
       │ npm install
       ▼
Install Dependencies
       │
       │ npm run build
       ▼
Production Build (.next)
       │
       │ PM2 Process Manager
       ▼
Next.js Production Server
       │
       ▼
Application running on Port 3000
```

---

## Quick Start

Clone repository

```
git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
cd authentication-flow
```

Install dependencies

```
npm install
```

Build application

```
npm run build
```

Start production server

```
pm2 start node --name "next-app" -- ./node_modules/next/dist/bin/next start
```

Open browser

```
http://localhost:3000
```

---

# Technologies Used

* **Next.js 14**
* **Node.js**
* **PM2 Process Manager**
* **Git / GitHub**
* **NPM Package Manager**

---

# Project Structure

After building the application, the project directory contains:

```
authentication-flow/
│
├── node_modules/
├── public/
├── src/
├── .next/
├── package.json
├── package-lock.json
├── next.config.js
└── README.md
```

---

# Deployment Steps

## 1. Confirm Project Files

Verify the project structure exists.

```
ls
```

Expected output includes:

* package.json
* next.config.js
* public/
* src/

Screenshot: **project-files.png**

---

# 2. Install Application Dependencies

Install required packages from the npm registry.

```
npm install
```

This downloads all required dependencies and creates the **node_modules** directory.

Screenshot: **dependencies-installed.png**

---

# 3. Build the Application

Create an optimized production build.

```
npm run build
```

This compiles the Next.js application and generates the **.next** directory.

Screenshot: **next-build.png**

---

# 4. Start the Production Server

The production server is started using **PM2** to ensure the application runs in the background.

```
pm2 start node --name "next-app" -- ./node_modules/next/dist/bin/next start
```

PM2 manages the application process and keeps it running even if the terminal is closed.

Verify the process:

```
pm2 list
```

Screenshot: **pm2-status.png**

---

# 5. Verify Application Deployment

Once the server is running, the application can be accessed in the browser:

```
http://localhost:3000
```

Example route used in the project:

```
http://localhost:3000/dashboard
```

Screenshot: **app-live.png**

---

# PM2 Process Management

Useful commands:

Start app

```
pm2 start node --name "next-app" -- ./node_modules/next/dist/bin/next start
```

View running processes

```
pm2 list
```

View logs

```
pm2 logs next-app
```

Stop application

```
pm2 stop next-app
```

Restart application

```
pm2 restart next-app
```

Save process list

```
pm2 save
```

---

# Screenshots Included

The following screenshots demonstrate successful deployment:

1. **project-files.png**
   Shows project structure and configuration files.

2. **dependencies-installed.png**
   Shows node_modules after dependency installation.

3. **next-build.png**
   Shows .next directory after build.

4. **pm2-status.png**
   Shows the application running with PM2.

5. **app-live.png**
   Shows the application running in the browser.

---

# GitHub Repository

Source code is version-controlled using Git and hosted on GitHub.

Important files pushed to the repository include:

* src/
* public/
* package.json
* package-lock.json
* next.config.js
* README.md

Excluded from GitHub using `.gitignore`:

```
node_modules/
.next/
.env
```

---

# Conclusion

The Next.js application was successfully deployed using a production build and managed using PM2.

Key achievements:

* Production build created successfully
* Dependencies installed
* Application server running
* Process managed with PM2
* Application verified via browser

This demonstrates a complete **Next.js production deployment workflow**.
