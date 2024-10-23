# Chat Application

## Overview

This is a simple Java-based chat application where multiple clients can communicate with each other through a central server. The server handles client connections, assigns unique IDs to each client, and broadcasts messages to all connected users.

## Features

### Server:
- Listens for client connections on a specific port (12345).
- Manages multiple client connections using threads.
- Broadcasts messages from one client to all others.
- Automatically assigns unique IDs to clients.
- Handles disconnection and notifies other clients when someone leaves.

### Client:
- Connects to the chat server using a specified address and port.
- Allows users to send and receive messages.
- Validates user input, ensuring that usernames contain only letters and spaces.
- Supports graceful disconnection using the “exit” command.

## Requirements

- Java Development Kit (JDK 8 or above)
- A terminal or command prompt to run the server and client applications.

## Getting Started

### Step 1: Compile the Code

1. Open a terminal and navigate to the directory containing the source files.
2. Run the following commands to compile the server and client code:

   ```bash
   javac server/ChatServer.java
   javac client/ChatClient.java

Step 2: Run the Server

In the terminal, run the following command to start the chat server:

java server.ChatServer

The server will listen for connections on port 12345.

Step 3: Run Multiple Clients

	1.	Open separate terminal windows for each client.
	2.	Run the following command to start each client:

java client.ChatClient


	3.	The client will prompt for a username, and once connected, they can send messages to the chat room.

Step 4: Test Communication

After connecting multiple clients, test by sending messages. Each client should see the messages sent by others in real-time.

Usage Instructions

	•	Send Messages:
	•	Type a message and press Enter. The message will be broadcast to all connected clients.
	•	Check for Duplicate Messages:
	•	Ensure that each message is broadcast once to all clients without duplication.
	•	Disconnect a Client:
	•	Type exit to gracefully disconnect a client from the chat. The server will notify other clients that this user has left.

Implementation Details

Server (ChatServer.java)

	•	Package: server

Key Features:

	•	Manages a set of connected client output streams (connectedClientsWriters).
	•	Assigns a unique client ID to each user upon connection.
	•	Uses threads to handle client connections concurrently.
	•	Broadcasts messages to all clients.
	•	When a client disconnects, removes them from the connected clients list and notifies other users.

Client (ChatClient.java)

	•	Package: client

Key Features:

	•	Connects to the server using localhost and port 12345.
	•	Prompts the user to enter a valid username (letters and spaces only).
	•	Receives and displays messages from other clients.
	•	Sends user messages to the server for broadcasting.
	•	Allows users to type exit to disconnect.

Troubleshooting

Connection Issues:

	•	Ensure the server is running before starting the clients.
	•	Verify that the server and clients are running on the same machine or network.

Empty Messages:

	•	The client prevents sending empty messages. Ensure to type valid input before pressing Enter.

Server Not Responding:

	•	Check if the server is running on the correct port and hasn’t encountered any exceptions.

Client Disconnects Unexpectedly:

	•	If a client disconnects due to network issues, other clients may not be immediately notified. The server will clean up resources when it detects the disconnection.
