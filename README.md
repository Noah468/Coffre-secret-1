<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Coffre secret</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      margin-top: 20%;
    }
    input[type="text"], button {
      padding: 10px;
      margin: 10px;
      font-size: 16px;
    }
    #result {
      font-weight: bold;
      color: red;
      margin-top: 10px;
    }
  </style>
</head>
<body>
  <h1>Dernière étape !</h1>
  <p>Entrez le mot de passe :</p>
  <input type="text" id="password" maxlength="4" placeholder="****">
  <button onclick="checkPassword()">Valider</button>
  <p id="result"></p>

  <script>
    const correctPassword = "TRIP"; // Le mot de passe ici
    function checkPassword() {
      const enteredPassword = document.getElementById("password").value;
      const result = document.getElementById("result");
      if (enteredPassword === correctPassword) {
        result.style.color = "green";
        result.textContent = "Félicitation! tu peux maintenant t'emparer de la clé du coffre 😊";
      } else {
        result.style.color = "red";
        result.textContent = "Erreur, réessaye !";
      }
    }
  </script>
</body>
</html>
