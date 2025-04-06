# My Calculator - Dockerized Web App

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)

## 📋 Project Overview
**My Calculator** is a Dockerized web application developed for **Deakin University's SIT323/SIT737** (Task 5.1P). Features:
- Interactive HTML interface
- Basic arithmetic operations (+, -, *, /)
- Client-side error handling
- Containerized with Docker

🔗 **Live Demo**: [http://localhost:3000](http://localhost:3000) (after deployment)

## 🚀 Quick Start

### Prerequisites
- [Docker](https://docs.docker.com/get-docker/)
- [Node.js](https://nodejs.org/) (v14+)

### Deployment
```bash
git clone https://github.com/PranavGoyal69/sit323-2025-prac5p.git
cd sit323-2025-prac5p
docker-compose up -d

Access the calculator at: http://localhost:3000

🧮 Application Features
Operations:


+ Addition
- Subtraction
* Multiplication
/ Division
Error Handling:

Division by zero alerts

Invalid input detection

Empty field prevention

🐋 Docker Configuration
Dockerfile
dockerfile

FROM node:14-alpine
WORKDIR /app
COPY package*.json ./
RUN npm install
COPY . .
EXPOSE 3000
CMD ["node", "server.js"]


📂 Project Structure

sit323-2025-prac5p/
├── app/
│   ├── public/
│   │   ├── index.html    # Calculator UI
│   │   └── script.js     # Client-side logic
│   ├── server.js         # Express server
│   └── package.json
├── Dockerfile
├── docker-compose.yml
└── README.md
