# Docker Chat Bot

Lihtne Flask chat bot Docker'is (Ubuntu Server VM, VirtualBox NAT).

## Kiirkäivitamine
docker build -t chatbot-app .
docker run -d -p 5001:5000 --name chatbot chatbot-app
Ava: http://localhost:5000

## Docker Compose + Nginx
docker compose up -d
Ava: http://localhost:8088

## API
GET /            -> HTML UI
POST /api/chat   -> body: {"message":"tere"}
GET /api/stats   -> container info

## Docker Hub
Image: https://hub.docker.com/r/steve380/chatbot-app

## Refleksioon
- Kõige keerulisem oli alguses Docker Compose’i tööle saamine, sest puudus compose-plugin ning tuli repo’d taastada ja/või lisada Docker’i ametlik APT repo.
- .dockerignore vähendas build-context’i ja kiirendas build’i. Väldib, et prahifailid satuks image’i.
- Panin image’ile latest ja semver-tag’i (nt v1.0). See teeb reprodutseerimise ja tagasipööramise lihtsaks.
