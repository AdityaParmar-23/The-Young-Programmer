<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Parmar Tech - Chat Room</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: 'Roboto', sans-serif;
    }

    body, html {
      height: 100%;
      overflow: hidden;
    }

    body {
      display: flex;
      background: #1e1e2f;
      color: #fff;
      position: relative;
    }

    .animated-bg {
      position: absolute;
      top: 0; left: 0; right: 0; bottom: 0;
      background: linear-gradient(-45deg, #0f2027, #203a43, #2c5364);
      background-size: 400% 400%;
      animation: gradientFlow 15s ease infinite;
      z-index: -1;
    }

    @keyframes gradientFlow {
      0% {background-position: 0% 50%;}
      50% {background-position: 100% 50%;}
      100% {background-position: 0% 50%;}
    }

    .sidebar {
      width: 250px;
      background: rgba(0, 0, 0, 0.6);
      padding: 2em 1em;
      display: flex;
      flex-direction: column;
      align-items: center;
      backdrop-filter: blur(10px);
      box-shadow: 2px 0 10px rgba(0,0,0,0.3);
    }

    .sidebar h2 {
      margin-bottom: 2em;
    }

    .sidebar button {
      background: #00c6ff;
      border: none;
      padding: 0.75em 1.5em;
      margin: 0.5em 0;
      color: white;
      font-weight: bold;
      cursor: pointer;
      border-radius: 25px;
      width: 100%;
      transition: background 0.3s ease;
    }

    .sidebar button:hover {
      background: #0099cc;
    }

    .chat-container {
      flex: 1;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      padding: 1.5em;
      position: relative;
    }

    .chat-box {
      flex: 1;
      overflow-y: auto;
      margin-bottom: 1em;
      display: flex;
      flex-direction: column;
      gap: 1em;
      padding-right: 0.5em;
    }

    .chat-message {
      background: rgba(255, 255, 255, 0.1);
      padding: 1em;
      border-radius: 12px;
      max-width: 70%;
      position: relative;
      box-shadow: 0 4px 10px rgba(0,0,0,0.4);
      transform: perspective(800px) translateZ(0);
      backdrop-filter: blur(5px);
    }

    .chat-message.me {
      align-self: flex-end;
      background: #0072ff;
    }

    .chat-message.other {
      align-self: flex-start;
      background: #2c3e50;
    }

    .chat-input {
      display: flex;
      align-items: center;
      gap: 1em;
    }

    .chat-input input {
      flex: 1;
      padding: 0.75em 1em;
      border-radius: 25px;
      border: none;
      font-size: 1em;
    }

    .chat-input button {
      padding: 0.75em 1.5em;
      border: none;
      background: #00c6ff;
      color: white;
      border-radius: 25px;
      cursor: pointer;
      font-weight: bold;
      transition: background 0.3s ease;
    }

    .chat-input button:hover {
      background: #0099cc;
    }

    .user-profile {
      display: flex;
      flex-direction: column;
      align-items: center;
      margin-bottom: 2em;
    }

    .user-profile img {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      margin-bottom: 1em;
      object-fit: cover;
      border: 3px solid #00c6ff;
    }

    .user-profile h3 {
      margin-bottom: 0.2em;
    }

    .user-profile p {
      font-size: 0.9em;
      color: #ccc;
    }
  </style>
</head>
<body>
  <div class="animated-bg"></div>

  <div class="sidebar">
    <div class="user-profile">
      <img src="https://via.placeholder.com/100x100.png?text=User" alt="User">
      <h3>Username</h3>
      <p>Online</p>
    </div>
    <button>General Chat</button>
    <button>Tech Talk</button>
    <button>Gaming Zone</button>
    <button>Logout</button>
  </div>

  <div class="chat-container">
    <div class="chat-box" id="chatBox">
      <div class="chat-message other">Hey there! 👋</div>
      <div class="chat-message me">Hello! How can I help?</div>
    </div>

    <div class="chat-input">
      <input type="text" id="messageInput" placeholder="Type your message..." />
      <button onclick="sendMessage()">Send</button>
    </div>
  </div>

  <script>
    function sendMessage() {
      const input = document.getElementById("messageInput");
      const message = input.value.trim();
      if (message === "") return;

      const chatBox = document.getElementById("chatBox");
      const msgEl = document.createElement("div");
      msgEl.className = "chat-message me";
      msgEl.textContent = message;
      chatBox.appendChild(msgEl);

      input.value = "";
      chatBox.scrollTop = chatBox.scrollHeight;
    }
  </script>
</body>
</html>
