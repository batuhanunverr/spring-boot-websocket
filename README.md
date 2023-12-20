# Spring Boot WebSocket Chat Application

This repository includes a simple chat application developed using WebSocket technology with Spring Boot.

## Project Overview

### ChatController

The `ChatController` class serves as a WebSocket message handler.

- It captures and processes messages arriving at the `/chat` endpoint utilizing the `@MessageMapping("/chat")` annotation.
- Incoming messages are broadcasted to all connected clients through the `/topic` channel.

### WsConfig

The `WsConfig` class facilitates WebSocket configuration.

- The `registerStompEndpoints` method defines the WebSocket endpoint and enables SockJS for communication.
- Configuration for the message broker enabling the `/topic` channel is done within the `configureMessageBroker` method.

### WsMessage

The `WsMessage` class represents messages transmitted over WebSocket.

- It includes fields such as `sender` and `message` to store the username and message content.
  
### SpringBootWebsocketApplication

The `SpringBootWebsocketApplication` class marks the entry point of the application.

## Usage

- The application runs on local.
- Messaging functionality is available via the `/chat` endpoint.
- Users can enter their username, type a message, and send it to start a conversation.


## Dependencies

The project relies on the following core dependencies:

- Spring Boot WebSocket Starter
- Lombok

## Getting Started

1. Clone the project to your local machine.
2. Open the project in your Java development environment.
3. Run the `main` method in the `SpringBootWebsocketApplication` class to start the application.
4. Access [http://localhost:8080] in your browser or open  `resource/test.html` to begin using the chat application.
