# Octopus Node

TypeScript WebSocket server built on Express and `ws`.

## Features
- WebSocket message routing by `mainType` and `subType`.
- HTTP health route at `/`.

## Requirements
- Node.js 18+ (Dockerfile uses Node 22).

## Install
```
npm install
```

## Development
```
npm run dev
```

## Build & Run
```
npm run build
npm start
```

## Docker
```
docker build -t octopus-node .
docker run --rm -p 8080:8080 octopus-node
```

## Environment
- `PORT`: HTTP/WebSocket server port (default: `8080`).

## WebSocket Payload
Messages are JSON objects with `mainType`, `subType`, and `data`.
```
{
  "mainType": "room",
  "subType": "join",
  "data": {}
}
```

Handlers live under `src/ws/handlers`.
