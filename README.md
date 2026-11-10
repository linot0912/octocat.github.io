# octocat.github.io

<!DOCTYPE html>
<html lang="fr">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Simulation Outlook</title>
<style>
* { box-sizing: border-box; }
body {
  margin: 0;
  font-family: "Segoe UI", Arial, sans-serif;
  background: #f3f5f8;
  min-height: 100vh;
  display: grid;
  place-items: center;
  color: #242424;
}
.card {
  background: white;
  width: min(420px, 92%);
  padding: 38px;
  box-shadow: 0 3px 15px #0002;
}
.logo { font-size: 25px; font-weight: 600; margin-bottom: 30px; }
.logo span { color: #0879c9; }
h1 { font-size: 24px; font-weight: 600; }
p { font-size: 14px; color: #555; }
input {
  width: 100%; padding: 12px 2px;
  border: 0; border-bottom: 1px solid #777;
  margin: 15px 0 25px; font-size: 16px;
  outline: none;
}
input:focus { border-bottom: 2px solid #0879c9; }
button {
  width: 100%; padding: 12px;
  background: #0879c9; color: white;
  border: 0; font-size: 15px; cursor: pointer;
}
button:hover { background: #0666a8; }
.notice {
  margin-top: 25px; padding: 12px;
  background: #fff4ce; color: #684d00;
  font-size: 12px;
}
#result { display: none; margin-top: 20px; }
</style>
</head>
<body>
<main class="card">
  <div class="logo">▣ <span>Outlook</span></div>
  <h1>Se connecter</h1>
  <p>Simulation pédagogique de connexion.</p>

  <form id="demo">
    <label for="email">Adresse e-mail fictive</label>
    <input id="email" type="email"
      placeholder="exemple@entreprise.fr" required>

    <label for="password">Mot de passe fictif</label>
    <input id="password" type="password"
      placeholder="Saisie de démonstration" required>

    <button type="submit">Tester la simulation</button>
  </form>

  <div id="result">
    <strong>Simulation terminée.</strong>
    <p>Aucune donnée n'a été enregistrée ou transmise.</p>
  </div>

  <div class="notice">
    EXERCICE DE SENSIBILISATION — Cette page n'est pas un
    service Microsoft et ne permet aucune authentification.
  </div>
</main>

<script>
document.getElementById("demo").addEventListener("submit", function(e) {
  e.preventDefault();
  document.getElementById("demo").reset();
  document.getElementById("result").style.display = "block";
});
</script>
</body>
</html>
