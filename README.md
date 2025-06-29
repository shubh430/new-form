# new-form
personal information

index.html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Contact Form</title>
  <link rel="stylesheet" href="style.css" />
</head>
<body>
  <div class="container">
    <h2>Contact Us</h2>
    <form id="contactForm">
      <input type="text" id="name" placeholder="Your Name" required />
      <input type="email" id="email" placeholder="Your Email" required />
      <textarea id="message" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
      <p id="responseMsg"></p>
    </form>
  </div>
  <script src="script.js"></script>
</body>
</html>

style.css
body {
  font-family: Arial, sans-serif;
  background-color: #f5f5f5;
}
.container {
  width: 350px;
  margin: 100px auto;
  background: white;
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0px 0px 10px #ccc;
}
input, textarea {
  width: 100%;
  margin-bottom: 15px;
  padding: 10px;
  border: 1px solid #aaa;
  border-radius: 5px;
}
button {
  background-color: #007bff;
  color: white;
  padding: 10px;
  width: 100%;
  border: none;
  border-radius: 5px;
}
#responseMsg {
  margin-top: 10px;
  color: green;
}

script.js
document.getElementById("contactForm").addEventListener("submit", function (e) {
  e.preventDefault();

  const name = document.getElementById("name").value.trim();
  const email = document.getElementById("email").value.trim();
  const message = document.getElementById("message").value.trim();

  if (name && email && message) {
    document.getElementById("responseMsg").innerText = "Thank you! We'll contact you soon.";
    this.reset();
  } else {
    document.getElementById("responseMsg").innerText = "Please fill in all fields.";
  }
});

