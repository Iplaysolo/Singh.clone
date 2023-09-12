# Singh.clone
Using HTMIL and CSS and JAVA SCRIPT
<!DOCTYPE html>
<html>
<head>
  <title>Login and Registration Form </title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <h1>Login and Registration Form </h1>

  <div class="form-container">
    <form id="loginForm">
      <h2>Login</h2>
      <div>
        <label for="loginUsername">Username</label>
        <input type="text" id="loginUsername" required>
      </div>
      <div>
        <label for="loginPassword">Password</label>
        <input type="password" id="loginPassword" required>
      </div>
      <button type="submit">Log In</button>
    </form>

    <form id="registrationForm">
      <h2>Registration</h2>
      <div>
        <label for="regUsername">Username</label>
        <input type="text" id="regUsername" required>
      </div>
      <div>
        <label for="regEmail">Email</label>
        <input type="email" id="regEmail" required>
      </div>
      <div>
        <label for="regPassword">Password</label>
        <input type="password" id="regPassword" required>
      </div>
      <div>
        <label for="regConfirmPassword">Confirm Password</label>
        <input type="password" id="regConfirmPassword" required>
      </div>
      <button type="submit">Register</button>
    </form>
  </div>

  <script data-two_delay_id="two_650036716205c" data-two_delay_src="script.js"></script>
</body>
</html>

style.css
body {
    font-family: Arial, sans-serif;
    background-color: #f5f5f5;
    text-align: center;
    padding: 20px;
  }
  
  h1 {
    color: #333;
  }
  
  .form-container {
    display: flex;
    justify-content: space-around;
    margin-top: 30px;
  }
  
  form {
    background-color: #fff;
    border-radius: 5px;
    padding: 20px;
    width: 300px;
  }
  
  h2 {
    margin-top: 0;
    color: #333;
  }
  
  label {
    display: block;
    margin-bottom: 5px;
  }
  
  input {
    width: 100%;
    padding: 8px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
  }
  
  button {
    width: 100%;
    padding: 10px;
    background-color: #4caf50;
    color: #fff;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #45a049;
  }
  Script.js
  document.getElementById('loginForm').addEventListener('submit', function(event) {
    event.preventDefault();
    const username = document.getElementById('loginUsername').value;
    const password = document.getElementById('loginPassword').value;
  
    // Check if username and password are valid
    if (username === 'admin' && password === 'password') {
      // Successful login
      alert('Login Successful');
    } else {
      // Invalid login
      alert('Invalid username or password');
    }
  });
  
  document.getElementById('registrationForm').addEventListener('submit', function(event) {
    event.preventDefault();
    const username = document.getElementById('regUsername').value;
    const email = document.getElementById('regEmail').value;
    const password = document.getElementById('regPassword').value;
    const confirmPassword = document.getElementById('regConfirmPassword').value;
  
    // Check if all fields are filled
    if (username && email && password && confirmPassword) {
      // Check if passwords match
      if (password === confirmPassword) {
        // Successful registration
        alert('Registration Successful');
        // Reset the form
        document.getElementById('registrationForm').reset();
      } else {
        // Passwords don't match
        alert('Passwords do not match');
      }
    } else {
      // Missing fields
      alert('Please fill in all fields');
    }
  });
