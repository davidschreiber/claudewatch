# ClaudeWatch Server

A Ktor-based backend service for the ClaudeWatch companion notification system.

## Overview

The server receives webhook events and relays them via Firebase Cloud Messaging (FCM) to registered Android devices.

## Current Endpoints

### `GET /health`
Health check endpoint that returns the server status.

**Response:**
```json
{
  "status": "ok"
}
```

## Development

### Prerequisites
- Java 21 or higher
- Gradle (wrapper included)

### Building
```bash
./gradlew :server:build
```

### Running locally
```bash
./gradlew :server:run
```

The server will start on port 8080 by default, or use the `PORT` environment variable if set.

### Testing
```bash
./gradlew :server:test
```

## Deployment

### Railway
The server is designed to be deployed on Railway using Nixpacks auto-detection.

#### Environment Variables
- `PORT`: Server port (automatically set by Railway)
- `FIREBASE_CREDENTIALS_JSON`: FCM service account credentials (JSON format)
- `GOOGLE_APPLICATION_CREDENTIALS`: Alternative path to FCM credentials file

#### Start Command
Railway will auto-detect the Gradle project and use:
```bash
./gradlew :server:shadowJar && java -jar server/build/libs/server-*-all.jar
```

## Architecture

- **Framework**: Ktor with Netty engine
- **Serialization**: Kotlinx Serialization with JSON
- **Build**: Gradle with Shadow plugin for fat JARs
- **Testing**: JUnit 5 with Ktor Test Engine