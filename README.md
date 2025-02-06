
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Trisha's Inbox</title>
    <style>
        body {
            font-family: 'Courier New', monospace;
            text-align: center;
            margin: 100px;
            background-color: #ffd1dc;
            color: #880e4f;
        }
        .container {
            max-width: 400px;
            margin: auto;
            padding: 20px;
            border: 2px solid #ff4081;
            border-radius: 15px;
            box-shadow: 4px 4px 15px rgba(0,0,0,0.2);
            background-color: #fff0f6;
        }
        input {
            width: 80%;
            padding: 10px;
            margin: 10px 0;
            border: 2px solid #ff80ab;
            border-radius: 5px;
            background-color: #ffe6eb;
            color: #880e4f;
        }
        button {
            padding: 10px 20px;
            background-color: #ff4081;
            color: white;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: bold;
        }
        button:hover {
            background-color: #d81b60;
        }
        .hidden {
            display: none;
        }
    </style>
</head>
<body>
    <div class="container" id="loginScreen">
        <h2>💌 Welcome to Trisha's Inbox</h2>
        <p>Enter your password to access new messages:</p>
        <input type="password" id="passwordInput" placeholder="Enter password">
        <button onclick="checkPassword()">💖 Unlock 💖</button>
        <p id="errorMessage" style="color: red; display: none;">Incorrect password. Try again.</p>
    </div>

    <div class="container hidden" id="messageScreen">
        <h2>📨 New Message</h2>
        <p><strong>From: Nixon</strong></p>
        <p>💗 Will you be my valentine? 💗</p>
    </div>

    <script>
        function checkPassword() {
            var input = document.getElementById("passwordInput").value;
            if (input === "200518") {
                document.getElementById("loginScreen").style.display = "none";
                document.getElementById("messageScreen").classList.remove("hidden");
            } else {
                document.getElementById("errorMessage").style.display = "block";
            }
        }
    </script>
</body>
</html>
