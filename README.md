<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>PsyRCare - Register</title>

<link href="https://fonts.googleapis.com/css2?family=Playfair+Display&display=swap" rel="stylesheet">

<style>
body {
  margin: 0;
  background: black;
  color: white;
  font-family: 'Playfair Display', serif;
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.container {
  width: 400px;
  text-align: center;
}

h1 {
  font-size: 32px;
  margin-bottom: 30px;
  font-weight: normal;
}

input {
  width: 100%;
  padding: 12px;
  margin: 10px 0;
  background: transparent;
  border: 1px solid #555;
  color: white;
  border-radius: 6px;
  outline: none;
  font-size: 14px;
}

input:focus {
  border-color: white;
}

.error {
  color: #ff6b6b;
  font-size: 12px;
  display: none;
  text-align: left;
}

button {
  margin-top: 20px;
  padding: 12px 30px;
  border: 1px solid white;
  background: transparent;
  color: white;
  cursor: pointer;
  border-radius: 8px;
  font-size: 14px;
  transition: 0.3s;
  opacity: 0.5;
}

button:hover {
  background: white;
  color: black;
}

button:disabled {
  cursor: not-allowed;
}
</style>
</head>

<body>

<div class="container">
  <h1>Join PsyRCare</h1>

  <input type="text" id="name" placeholder="Your name">

  <input type="email" id="email" placeholder="Your email">
  <div id="emailError" class="error">Please enter a valid email address.</div>

  <button id="continueBtn" disabled>Continue</button>
</div>

<script>
const nameInput = document.getElementById("name");
const emailInput = document.getElementById("email");
const continueBtn = document.getElementById("continueBtn");
const emailError = document.getElementById("emailError");

function isValidEmail(email) {
  return /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(email);
}

function checkForm() {
  const name = nameInput.value.trim();
  const email = emailInput.value.trim();

  if (name.length > 1 && isValidEmail(email)) {
    continueBtn.disabled = false;
    continueBtn.style.opacity = "1";
    emailError.style.display = "none";
  } else {
    continueBtn.disabled = true;
    continueBtn.style.opacity = "0.5";
    if (email.length > 0 && !isValidEmail(email)) {
      emailError.style.display = "block";
    } else {
      emailError.style.display = "none";
    }
  }
}

nameInput.addEventListener("input", checkForm);
emailInput.addEventListener("input", checkForm);

continueBtn.addEventListener("click", function() {
  const name = nameInput.value.trim();
  const email = emailInput.value.trim();

  // حفظ البيانات
  localStorage.setItem("userName", name);
  localStorage.setItem("userEmail", email);

  // الانتقال إلى صفحة العروض
  window.location.href = "offers.html";
});
</script>

</body>
</html>








  
