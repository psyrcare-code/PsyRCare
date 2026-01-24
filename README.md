<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PsyRCare - Register</title>

<style>
body {
  margin: 0;
  background: black;
  color: white;
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  font-family: Arial, sans-serif;
}

.container {
  text-align: center;
  width: 320px;
}

h1 {
  margin-bottom: 10px;
  font-size: 36px;
}

p {
  color: #ccc;
  margin-bottom: 30px;
  font-size: 14px;
}

input {
  width: 100%;
  padding: 12px;
  margin: 10px 0;
  background: black;
  border: 1px solid white;
  color: white;
  outline: none;
}

input::placeholder {
  color: #777;
}

.btn {
  margin-top: 20px;
  border: 1px solid white;
  padding: 12px;
  cursor: pointer;
  transition: 0.3s;
}

.btn:hover {
  background: white;
  color: black;
}
</style>
</head>

<body>

<div class="container">
  <h1>Welcome</h1>
  <p>Before we begin, tell us a little about you.</p>

  <input type="text" id="name" placeholder="Your name">
  <input type="email" id="email" placeholder="Your email">

  <div class="btn" onclick="continueToOffers()">Continue</div>
</div>

<script>
function continueToOffers() {
  const name = document.getElementById("name").value;
  const email = document.getElementById("email").value;

  if (name === "" || email === "") {
    alert("Please fill in your name and email.");
    return;
  }

  // حفظ البيانات مؤقتًا (اختياري)
  localStorage.setItem("userName", name);
  localStorage.setItem("userEmail", email);

  // الانتقال إلى صفحة العروض
  window.location.href = "offers.html";
}
</script>

</body>
</html>
