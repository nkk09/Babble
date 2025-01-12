# Babble - Python Chat Application

Babble is a simple chat application written in Python that allows users to register, login, send messages, and share files with each other over a network.

## Features:

1. **User Authentication**: Users can register with a username and password or login if they already have an account.
2. **Messaging**: Users can send text messages to other users who are currently online.
3. **File Sharing**: Users can attach files and send them to other users. Received files can be opened directly from the chat interface.
4. **Real-time Updates**: The chat interface updates in real-time with incoming messages and file attachments.
5. **Error Handling**: The application handles various error scenarios gracefully, including invalid credentials, address already in use, and recipient offline.

## Dependencies:

- Python 3.x
- Tkinter (for GUI)
- Socket module
- SQLite3 module (for the server)
- hashlib module (for the server)
- pathlib module (for the server)

## Usage:

1. **Running the Server**: Run the `server.py` script using Python to start the Babble server. The server IP address will be displayed in the terminal.
2. **Running the Client**: Run the `client.py` script using Python to start the Babble client application.
2. **Login or Register**: Enter the server IP, your chosen username, and password. Click on the **Login** button to login or the **Register** button to create a new account.
3. **Chatting**: Once logged in, you can enter the username of the recipient, type your message in the text box, and click on the **Send** button to send messages. You can also attach files by clicking on the **Attach** button.
4. **Receiving Messages**: Incoming messages and file attachments are displayed in the chat interface in real-time.

## Notes:

- The server listens for incoming UDP messages on port 12345 by default.
- Users send and receive messages in a peer-to-peer fashion, the server is used for logging in.
- Users send text messages over UDP with ensured reliability
- Users send files over TCP
- User data is stored in a SQLite database named `chat_app.db`.
- User passwords are secured.
- Closing the application causes the user to log out. Offline users can't receive messages.