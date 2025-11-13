# Docker Chat Bot

Lihtne Flask chat bot Docker'is (Ubuntu Server VM, VirtualBox NAT).

## Kiirkäivitamine
docker build -t chatbot-app .
docker run -d -p 5000:5000 --name chatbot chatbot-app
Ava: http://localhost:5000

## Docker Compose + Nginx
docker compose up -d
Ava: http://localhost:8088

## API
GET /            -> HTML UI
POST /api/chat   -> body: {"message":"tere"}
GET /api/stats   -> container info

## Docker Hub
Image: https://hub.docker.com/r/[username]/chatbot-app

## Refleksioon
(5 vastust, 2-3 lauset iga teema kohta…)
