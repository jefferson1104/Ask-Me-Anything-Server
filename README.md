<div align="center" style="margin-bottom: 20px;">
  <div>
    <h1>AMA API - Ask Me Anything</h1>
  </div>

  <div align="center">
    <img alt="technology" src="https://img.shields.io/badge/go-%2300ADD8.svg?style=for-the-badge&logo=go&logoColor=white">
    <img alt="technology" src="https://img.shields.io/badge/postgres-%23316192.svg?style=for-the-badge&logo=postgresql&logoColor=white">
    <img alt="technology" src="https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white">
  </div>
</div>

## :memo: About project

This is an API developed in Go for an AMA (Ask Me Anything) project, where users can create rooms, ask questions, and interact in real-time. The API includes both REST endpoints and WebSocket to ensure real-time communication.

## 🛠️ Features

- **Room Creation**: Users can create different rooms to hold Q&A sessions.
- **Question Management**: Within each room, users can ask questions, which can receive likes and be marked as answered.
- **Real-Time Interaction**: Using WebSocket, all interactions, such as new questions and likes, are updated in real-time for all participants in the room.

## ⚡ Technologies Used

- **Go (Golang)**: Programming language used to develop the API.
- **PostgreSQL**: Relational database used to store room, question, and interaction data.
- **WebSocket**: Implemented to provide real-time updates between clients and the server.
- **Docker Compose**: Used to simplify the setup and management of the development environment, including the PostgreSQL container configuration.

## :cyclone: Run this project

```bash

# clone this repository
git clone https://github.com/jefferson1104/Ask-Me-Anything-Server

# go to the folder
cd Ask-Me-Anything-Server

# environment file
rename the .env.example file to .env

# Run docker file
$ docker compose up -d

# Run go server
go run ./cmd/ama/main.go
```
