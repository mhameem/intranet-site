<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Intranet Pro BTS SIO</title>
  <style>
    body { font-family: Arial, sans-serif; margin: 0; padding: 0; background-color: #f5f5f5; }
    header { background-color: #1f2937; color: white; padding: 1rem 2rem; text-align: center; }
    main { padding: 2rem; }
    section { background: white; padding: 1.5rem; margin-bottom: 2rem; border-radius: 8px; box-shadow: 0 0 10px rgba(0,0,0,0.1); }
    h1, h2 { margin-top: 0; }
    ul { list-style: disc; padding-left: 1.5rem; }
    .btn { padding: 0.5rem 1rem; background-color: #2563eb; color: white; border: none; border-radius: 5px; cursor: pointer; }
    .btn:hover { background-color: #1d4ed8; }
    input, textarea { width: 100%; padding: 0.5rem; margin-bottom: 1rem; border: 1px solid #ccc; border-radius: 5px; }
    .hidden { display: none; color: red; }
  </style>
</head>
<body>
  <header>
    <h1>Intranet - Projet BTS SIO SISR</h1>
  </header>

  <main>
    <section>
      <h2>🔗 Liens utiles</h2>
      <ul>
        <li><a href="#">GLPI - Gestion des tickets</a></li>
        <li><a href="#">Active Directory</a></li>
        <li><a href="#">Webmail Office 365</a></li>
        <li><a href="#">Documentation interne</a></li>
      </ul>
    </section>

    <section>
      <h2>📰 Actualités internes</h2>
      <ul>
        <li>✅ Mise à jour de l'antivirus vendredi soir</li>
        <li>✅ Nouvelle procédure de sauvegarde disponible</li>
        <li>✅ VPN accessible pour les utilisateurs à distance</li>
      </ul>
    </section>

    <section>
      <h2>📩 Contacter l'équipe IT</h2>
      <input type="text" id="inputNom" placeholder="Votre nom">
      <input type="email" id="inputEmail" placeholder="Votre adresse e-mail">
      <textarea id="inputMessage" rows="4" placeholder="Votre message"></textarea>
      <button class="btn" onclick="envoyerMessage()">Envoyer</button>
      <p id="msgEnvoye" class="hidden">✅ Message envoyé !</p>
      <p id="msgErreur" class="hidden">⚠️ Merci de remplir tous les champs.</p>
    </section>
  </main>

  <script>
    function envoyerMessage() {
      const nom = document.getElementById("inputNom").value.trim();
      const email = document.getElementById("inputEmail").value.trim();
      const message = document.getElementById("inputMessage").value.trim();
      const msgEnvoye = document.getElementById("msgEnvoye");
      const msgErreur = document.getElementById("msgErreur");

      if (!nom || !email || !message) {
        msgErreur.style.display = "block";
        msgEnvoye.style.display = "none";
      } else {
        msgErreur.style.display = "none";
        msgEnvoye.style.display = "block";
      }
    }
  </script>
</body>
</html>
