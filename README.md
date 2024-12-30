<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Protégée</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin-top: 100px;
        }
        input {
            padding: 10px;
            margin: 10px;
            font-size: 16px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
        }
    </style>
</head>
<body>
    <h1>Accès à la page protégée</h1>
    <p>Entrez le code pour accéder :</p>
    <input type="password" id="codeInput" placeholder="Code">
    <button onclick="checkCode()">Valider</button>

    <p id="message" style="color: red; font-weight: bold;"></p>

    <script>
        function checkCode() {
            const enteredCode = document.getElementById('codeInput').value;
            const correctCode = "12345"; // Remplace par ton code

            if (enteredCode === correctCode) {
                window.location.href = "protected.html"; // Page protégée
            } else {
                document.getElementById('message').innerText = "Code incorrect !";
            }
        }
    </script>
</body>
</html>
