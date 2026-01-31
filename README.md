<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PsyRCare - Order</title>

<style>
body {
  margin: 0;
  background: black;
  color: white;
  font-family: Arial, sans-serif;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.container {
  width: 450px;
  text-align: center;
  border: 1px solid #333;
  padding: 35px 30px;
  border-radius: 14px;
}

h1 {
  font-size: 26px;
  font-weight: 300;
  margin-bottom: 25px;
}

.details {
  text-align: left;
  font-size: 15px;
  line-height: 1.8;
  margin-bottom: 30px;
  opacity: 0.95;
}

.details span {
  opacity: 0.7;
}

.note {
  font-size: 13px;
  opacity: 0.7;
  margin-bottom: 25px;
  text-align: center;
}

button {
  width: 100%;
  padding: 12px;
  margin: 8px 0;
  border-radius: 30px;
  border: 1px solid white;
  background: transparent;
  color: white;
  cursor: pointer;
  transition: 0.3s;
  font-size: 14px;
}

button:hover {
  background: white;
  color: black;
}
</style>
</head>

<body>

<div class="container">

  <h1>Your session details</h1>

  <div class="details" id="sessionDetails">
    Loading...
  </div>

  <div class="note">
    Payment and session scheduling will be completed via WhatsApp.<br>
    You will receive a reply within 24 hours.
  </div>

  <button onclick="continueWhatsApp()">Continue on WhatsApp</button>
  <button onclick="goToOffers()">Back to offers</button>
  <button onclick="goToConversation()">Conversation page</button>

</div>

<script>
const name = localStorage.getItem("offerName");
const duration = localStorage.getItem("offerDuration");
const description = localStorage.getItem("offerDescription");
const price = localStorage.getItem("offerPrice");
const username = localStorage.getItem("username");

const sessionDetails = document.getElementById("sessionDetails");

if (name && duration && description && price !== null) {
  sessionDetails.innerHTML = `
    <strong>Session:</strong> ${name}<br>
    <strong>Duration:</strong> ${duration}<br>
    <strong>Description:</strong><br>
    <span>${description}</span><br><br>
    <strong>Price:</strong> $${price}
  `;
} else {
  sessionDetails.innerHTML = "No session selected.";
}

function continueWhatsApp() {
  let message =
    `Hello PsyRCare, my name is ${username}. I would like to book the following session:\n\n` +
    `Session: ${name}\n` +
    `Duration: ${duration}\n` +
    `Price: $${price}`;

  let url = "https://wa.me/212722288965?text=" + encodeURIComponent(message);
  window.open(url, "_blank");
}

function goToOffers() {
  window.location.href = "offers.html";
}

function goToConversation() {
  window.location.href = "about.html";
}
</script>

</body>
</html>
 

   
 
