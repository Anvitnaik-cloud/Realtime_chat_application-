## Real-Time Chat Application

This is a simple, functional real-time chat application named **`real-time-chat`** built with **Node.js** and **Socket.io**. It enables instant, bi-directional messaging between connected users.

-----

## ✨ Features

  * **Instant Messaging:** Utilizes WebSockets via **Socket.io** for real-time message delivery.
  * **Minimalist UI:** A clean, single-screen chat interface defined in `index.html`.
  * **Asynchronous Display:** Messages are instantly displayed, differentiating between messages you **sent** (shown on the right) and messages you **received** (shown on the left).
  * **Standard Frameworks:** Built on **Express** and **Node.js**.

-----

## 🛠️ Technologies Used

  * **Server:**  **Node.js**
  * **Web Framework:** **Express.js** (`^5.1.0`)
  * **Real-time Communication:** **Socket.io** (`^4.8.1`)
  * **Frontend:** **HTML**, **Inline CSS**, and **Vanilla JavaScript** (client-side logic is embedded directly in `index.html`).

-----

## 🚀 Getting Started

Follow these instructions to set up and run the application on your local machine.

### Prerequisites

You must have **Node.js** and **npm** (Node Package Manager) installed.

### Installation

1.  **Clone the repository** (if applicable) or ensure you have the project files.

2.  **Install dependencies** listed in `package.json`:

    ```bash
    npm install
    ```

### Running the Application

1.  **Start the server** using Node.js:

    ```bash
    node server.js
    ```

    The server console will display: `Server running on http://localhost:3000`

2.  **Access the application:**
    Open your web browser and navigate to: **`http://localhost:3000`**

    To test the real-time feature, open this URL in multiple browser tabs or windows and start chatting.

-----

## 📂 Project Structure

This project follows a simple structure, with `server.js` handling the backend and serving the static frontend files from the **`public`** directory.

```
├── node_modules/
├── public/                   # Static files served by Express
│   └── index.html            # Main chat interface (HTML/CSS/Client-side JS)
├── package.json
├── package-lock.json
└── server.js                 # Backend setup, Express routes, and Socket.io configuration
```

### Key Logic

| File | Description |
| :--- | :--- |
| **`server.js`** | Sets up the Express server and HTTP server on port **3000**. It serves `index.html` and configures Socket.io to **broadcast** received messages to all *other* connected clients (`socket.broadcast.emit`). |
| **`index.html`** | Contains the full chat UI and client-side logic. It initializes the Socket.io connection, captures user input, emits the `chat message` event to the server, and handles displaying incoming messages. |

-----

## ⚙️ Configuration Notes

The server is configured to run on port **3000**. This can be changed by modifying the `server.js` file:

```javascript
// server.js
// ...
server.listen(3000, () => {
  console.log("Server running on http://localhost:3000");
});
```
