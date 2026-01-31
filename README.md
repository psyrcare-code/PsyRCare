<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PsyRCare - Admin</title>

<style>
body {
  margin: 0;
  background: #0b0b0b;
  color: white;
  font-family: Arial, sans-serif;
  display: flex;
  height: 100vh;
}

/* Users list */
.users {
  width: 30%;
  border-right: 1px solid #333;
  padding: 20px;
  overflow-y: auto;
}

.users h2 {
  font-weight: 300;
  margin-bottom: 15px;
}

.user {
  padding: 10px;
  border-bottom: 1px solid #222;
  cursor: pointer;
  font-size: 14px;
}

.user:hover {
  background: #1a1a1a;
}

/* Chat */
.chat {
  width: 70%;
  display: flex;
  flex-direction: column;
}

.chat-header {
  padding: 15px;
  border-bottom: 1px solid #333;
  font-size: 14px;
  opacity: 0.8;
}

.messages {
  flex: 1;
  padding: 20px;
  overflow-y: auto;
}

.msg {
  margin-bottom: 10px;
  font-size: 14px;
}

.msg.user {
  color: #bbb;
}

.msg.admin {
  color: white;
}

/* Controls */
.controls {
  border-top: 1px solid #333;
  padding: 15px;
  display: flex;
  gap: 10px;
}

input {
  flex: 1;
  padding: 10px;
  background: transparent;
  border: 1px solid #444;
  color: white;
  border-radius: 6px;
}

button {
  padding: 10px 18px;
  background: transparent;
  border: 1px solid white;
  color: white;
  cursor: pointer;
  border-radius: 20px;
}

button:hover {
  background: white;
  color: black;
}
</style>
</head>

<body>

<div class="users">
  <h2>Users</h2>
  <div id="usersList"></div>
</div>

<div class="chat">
  <div class="chat-header" id="chatHeader">
    Select a user to view conversation
  </div>

  <div class="messages" id="messages"></div>

  <div class="controls">
    <input type="text" id="adminMsg" placeholder="Write a message..." disabled>
    <button onclick="sendAdminMsg()" disabled id="sendBtn">Send</button>
    <button onclick="toggleSession()" id="toggleBtn" disabled>Open Session</button>
  </div>
</div>

<script>
let users = JSON.parse(localStorage.getItem("usersList")) || [];
let currentUser = null;

const usersList = document.getElementById("usersList");
const messagesDiv = document.getElementById("messages");
const chatHeader = document.getElementById("chatHeader");
const adminMsg = document.getElementById("adminMsg");
const sendBtn = document.getElementById("sendBtn");
const toggleBtn = document.getElementById("toggleBtn");

// عرض المستخدمين
users.forEach(email => {
  let div = document.createElement("div");
  div.className = "user";
  div.textContent = email;
  div.onclick = () => openChat(email);
  usersList.appendChild(div);
});

function openChat(email) {
  currentUser = email;
  chatHeader.textContent = "Chat with " + email;
  adminMsg.disabled = false;
  sendBtn.disabled = false;
  toggleBtn.disabled = false;
  loadMessages();
  updateToggleText();
}

function loadMessages() {
  messagesDiv.innerHTML = "";
  let msgs = JSON.parse(localStorage.getItem("chat_" + currentUser)) || [];
  msgs.forEach(m => {
    let div = document.createElement("div");
    div.className = "msg " + m.from;
    div.textContent = m.text;
    messagesDiv.appendChild(div);
  });
  messagesDiv.scrollTop = messagesDiv.scrollHeight;
}

function sendAdminMsg() {
  if (!adminMsg.value.trim()) return;

  let msgs = JSON.parse(localStorage.getItem("chat_" + currentUser)) || [];
  msgs.push({ from: "admin", text: adminMsg.value });
  localStorage.setItem("chat_" + currentUser, JSON.stringify(msgs));

  adminMsg.value = "";
  loadMessages();
}

function toggleSession() {
  let key = "sessionOpen_" + currentUser;
  let isOpen = localStorage.getItem(key) === "true";
  localStorage.setItem(key, (!isOpen).toString());
  updateToggleText();
}

function updateToggleText() {
  let isOpen = localStorage.getItem("sessionOpen_" + currentUser) === "true";
  toggleBtn.textContent = isOpen ? "Close Session" : "Open Session";
}
</script>

</body>
</html>

