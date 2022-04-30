# v2ray proxy quick and simple 

## Pre-requisites
1. docker
2. docker-compose
3. git

## How to setup the server

1. Register a new domain name pointing to your public address
2. Edit `Caddifile` replacing **server.example.com** with your domain name
3. Replace the id on line **7** in `v2ray-server.json` with a new id
4. Start the server `docker-compose up`

## How to setup the client

1. Replace **server.example.com** with your domain name in `client-config.json`
2. Replace the id with your uuid in `client-config.json`
3. Get the **vmess** address with `echo vmess://$(cat client-config.json | base64 -w 0)`
4. Load this in your favorite client