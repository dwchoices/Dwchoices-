
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mon Portfolio</title>
    <style>
        /* CSS intégré */
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f8f8f8;
            margin: 0;
            padding: 0;
        }

        header {
            background-color: #232f3e;
            color: white;
            padding: 20px;
            text-align: center;
        }

        nav {
            display: flex;
            justify-content: center;
            gap: 20px;
            background-color: #ff9900;
            padding: 10px;
        }

        nav a {
            color: white;
            text-decoration: none;
            font-size: 18px;
        }

        nav a:hover {
            color: #232f3e;
        }

        section {
            padding: 20px;
            background-color: white;
            margin: 20px auto;
            border-radius: 10px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            width: 80%;
        }

        footer {
            background-color: #232f3e;
            color: white;
            padding: 20px;
            text-align: center;
        }

        button {
            background-color: #ff9900;
            border: none;
            color: white;
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background-color: #232f3e;
        }

        form {
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <header>
        <img src="https://via.placeholder.com/150" alt="Logo" style="height: 50px;">
        
      <h1>Bienvenue sur l'espace numerique de Dwchoices</h1>
      
    <header>
        <h1>TAMEKLO Komlan Mawuli - Spécialiste en Machine Learning & Développement Web</h1>
    </header>
    </header>
    
    <nav>
        <a href="#accueil">Accueil</a>
        <a href="#about">À propos</a>
        <a href="#services">Nos Services</a>
        <a href="#contact">Contact</a>
        </nav>

    <section id="accueil">
        <h2>Présentation</h2>
        <p>Je suis un développeur fullstack passionné spécialisé dans les technologies modernes comme Python, HTML, JavaScripts,PHP et la plupart des bibioteques et framworks
          <p>Specialiste de la technogie pythons , je met toutes mes competances aux services du client .</p>
        </section>
        <button onclick="window.location.href='#services'"> Nos services</button>
    </section>

    <section id="about">
        <h2>À propos de moi</h2>
        <p>Je m'appelle TAMEKLO Komlan Mawuli, un développeur et créateur de contenu avec une expertise en développement web et machine learning.</p>
      

            <p>Diplômé en électronique et en science informatique au Togo, et spécialisé en machine learning à l'université de Harvard. J'ai une expertise avancée en Python, HTML, JavaScript, CSS, et bien plus. Mon objectif est d'aider les entreprises à exploiter les données et l'IA pour optimiser leurs processus et améliorer leurs décisions.</p>
            <p>Je suis passionné par l'innovation technologique et je m'engage à fournir des solutions de haute qualité qui répondent aux besoins uniques de mes clients.</p>
      
    </section>

    <section id="services">
        <h2>Nos Services</h2>
        <ul>
            <li>Développement Web</li>
            <li>Services d'IA et de Machine Learning</li>
            <li>Création de contenu numérique</li>
        </ul>
        <!-- Section Vidéos -->
<section id="videos" class="portfolio">
    <h2>Vidéos</h2>
    <div class="project-item">
        <h3>Projet 1 : Analyse de Données pour une Entreprise</h3>
        <video width="100%" heighnt="315" controls>
            <source src="https://player.vimeo.com/external/385217054.hd.mp4?s=7a79ec573e2c42e1e24eb4ec8f1d86d2b8d51c6b&profile_id=174" type="video/mp4">
            Votre navigateur ne supporte pas la lecture de cette vidéo.
        </video>
        <p>Une vidéo démontrant l'analyse des données pour améliorer la prise de décision.</p>
    </div>
    <div class="project-item">
        <h3>Projet 2 : Automatisation des Tâches avec Python</h3>
        <video width="100%" height="315" controls>
            <source src="https://player.vimeo.com/external/395380470.hd.mp4?s=7a79ec573e2c42e1e24eb4ec8f1d86d2b8d51c6b&profile_id=174" type="video/mp4">
            Votre navigateur ne supporte pas la lecture de cette vidéo.
        </video>
        <p>Une vidéo montrant le script Python créé pour automatiser les processus d'une entreprise.</p>
    </div>
    <div class="project-item">
        <h3>Projet 3 : Développement d'une Application Web d'IA</h3>
        <video width="100%" height="315" controls>
            <source src="https://player.vimeo.com/external/396748043.hd.mp4?s=7a79ec573e2c42e1e24eb4ec8f1d86d2b8d51c6b&profile_id=174" type="video/mp4">
            Votre navigateur ne supporte pas la lecture de cette vidéo.
        </video>
        <p>Une vidéo présentant l'application web utilisant des modèles d'apprentissage automatique.</p>
    </div>
</section>
    </section>

    <section id="contact">
        <h2>Contact</h2>
        <p>Email : clautameklo@hotmail.fr</p>
        <p>Téléphone : +228 71210208</p>
       <div class="chat-container">
        <div class="chat-box" id="chat-box"></div>
        <div style="display: flex;">
            <input type="text" id="message-input" placeholder="Tapez votre message...">
            <button id="send-button">Envoyer</button>
        </div>
    </div>

    <script>
        // Écouteur d'événement pour le bouton d'envoi
        document.getElementById('send-button').addEventListener('click', function() {
            const messageInput = document.getElementById('message-input');
            const messageText = messageInput.value.trim();

            if (messageText !== '') {
                addMessage(messageText, 'user');
                messageInput.value = '';
                
                // Appel de la fonction pour obtenir la réponse automatique
                const response = getResponse(messageText);
                setTimeout(() => {
                    addMessage(response, 'bot');
                }, 1000);
            }
        });

        // Fonction pour ajouter un message à la boîte de chat
        function addMessage(text, sender) {
            const chatBox = document.getElementById('chat-box');
            const messageElement = document.createElement('div');
            messageElement.className = 'message ' + sender;
            messageElement.textContent = text;
            chatBox.appendChild(messageElement);
            chatBox.scrollTop = chatBox.scrollHeight; // Faire défiler vers le haut
        }

        // Fonction pour obtenir la réponse automatique en fonction du message
        function getResponse(message) {
            switch (message.toLowerCase()) {
                case '1 message':
              return'Bienvenu dans le monde de la nouvel technologie Nous somme á votre service';
                case '2 message':
                    return 'Votre requête a été notée. Nous vous recontaterons dans de bref de.';
                case '3 message':
                    return 'Merci de nous laisser un message. Nous allons traiter votre demande.';
                default:
                    return 'Merci de votre message. Nous sommes ici pour vous aider.';
            }
        }
    </script>
</body>
</html>
 
    </section>

    <section id="upload">
        <h2>Upload Vidéo</h2>
        <form>
            <input type="file" name="file">
            <button type="submit">Télécharger</button>
        </form>
    </section>

    <section id="login">
        <h2>Connexion</h2>
        <button onclick="loginWithGoogle()">Connexion avec Google</button>
        <button onclick="loginWithFacebook()">Connexion avec Facebook</button>
    </section>

    <footer>
        <p>&copy; 2024 Mon Portfolio. Tous droits réservés.</p>
    </footer>

    <script>
        // JavaScript intégré
        function loginWithGoogle() {
            alert("Redirection vers Google...");
        }
<!-- Section Vidéos -->
<section id="videos" class="portfolio">
    <h2>Vidéos</h2>
    <div class="project-item">
        <h3>Projet 1 : Analyse de Données pour une Entreprise</h3>
        <video width="100%" height="315" controls>
            <source src="https://player.vimeo.com/external/385217054.hd.mp4?s=7a79ec573e2c42e1e24eb4ec8f1d86d2b8d51c6b&profile_id=174" type="video/mp4">
            Votre navigateur ne supporte pas la lecture de cette vidéo.
        </video>
        <p>Une vidéo démontrant l'analyse des données pour améliorer la prise de décision.</p>
    </div>
    <div class="project-item">
        <h3>Projet 2 : Automatisation des Tâches avec Python</h3>
        <video width="100%" height="315" controls>
            <source src="https://player.vimeo.com/external/395380470.hd.mp4?s=7a79ec573e2c42e1e24eb4ec8f1d86d2b8d51c6b&profile_id=174" type="video/mp4">
            Votre navigateur ne supporte pas la lecture de cette vidéo.
        </video>
        <p>Une vidéo montrant le script Python créé pour automatiser les processus d'une entreprise.</p>
    </div>
    <div class="project-item">
        <h3>Projet 3 : Développement d'une Application Web d'IA</h3>
        <video width="100%" height="315" controls>
            <source src="https://player.vimeo.com/external/396748043.hd.mp4?s=7a79ec573e2c42e1e24eb4ec8f1d86d2b8d51c6b&profile_id=174" type="video/mp4">
            Votre navigateur ne supporte pas la lecture de cette vidéo.
        </video>
        <p>Une vidéo présentant l'application web utilisant des modèles d'apprentissage automatique.</p>
    </div>
</section>
        function loginWithFacebook() {
            alert("Redirection vers Facebook...");
        }

        document.addEventListener("DOMContentLoaded", function() {
            const uploadForm = document.querySelector("form");
            if (uploadForm) {
                uploadForm.addEventListener("submit", function(event) {
                    event.preventDefault();
                    alert("Votre fichier a été téléchargé avec succès (simulation).");
                });
            }
        });
    </script>
</body>
</html>
        
   
<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Portfolio de TAMEKLO Komlan Mawuli, Spécialiste en Machine Learning et Développement Web">
    <title>TAMEKLO Komlan Mawuli - Portfolio</title>
    <link rel="stylesheet" href="styles.css">
    <style>
        /* Styles basiques pour le portfolio */
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f9f9f9;
        }

        header {
            background-color: #007acc;
            color: #fff;
            padding: 20px;
            text-align: center;
        }

        header h1 {
            margin: 0;
        }

        nav {
            display: flex;
            justify-content: center;
            background-color: #005f99;
            padding: 10px 0;
        }

        nav a {
            color: #fff;
            padding: 14px 20px;
            text-decoration: none;
            transition: background-color 0.3s;
        }

        nav a:hover {
            background-color: #004477;
        }

        .container {
            padding: 20px;
            max-width: 1200px;
            margin: auto;
        }

        .about, .services, .portfolio, .contact, .testimonials, .chat {
            margin-bottom: 40px;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
        }

        h2 {
            color: #007acc;
            text-align: center;
        }

        .service-item, .project-item {
            background-color: #e6f7ff;
            padding: 20px;
            margin: 10px 0;
            border-radius: 8px;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .service-item h3, .project-item h3 {
            margin: 0 0 10px 0;
            color: #005f99;
        }

        .project-item img {
            max-width: 100%;
            border-radius: 8px;
        }

        .contact-form {
            display: flex;
            flex-direction: column;
            max-width: 600px;
            margin: 0 auto;
        }

        .contact-form input, .contact-form textarea {
            padding: 10px;
            margin: 10px 0;
            border-radius: 4px;
            border: 1px solid #ccc;
        }

        .contact-form button {
            padding: 10px;
            background-color: #007acc;
            color: #fff;
            border: none;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .contact-form button:hover {
            background-color: #005f99;
        }

        footer {
            background-color: #007acc;
            color: #fff;
            text-align: center;
            padding: 20px;
        }

        /* Styles pour la section témoignages */
        .testimonial {
            margin: 10px 0;
            font-style: italic;
            border-left: 3px solid #007acc;
            padding-left: 10px;
        }

        /* Styles pour la section chat */
        .chat {
            display: flex;
            flex-direction: column;
            max-width: 600px;
            margin: 0 auto;
        }

        .chat-message {
            padding: 10px;
            margin: 5px 0;
            border-radius: 4px;
        }

        .chat-message.user {
            background-color: #e0ffe0; /* Couleur pour les messages de l'utilisateur */
            align-self: flex-end;
        }

        .chat-message.bot {
            background-color: #e0e0ff; /* Couleur pour les messages du bot */
            align-self: flex-start;
        }

        .chat-form {
            display: flex;
            margin-top: 10px;
        }

        .chat-form input {
            flex: 1;
            padding: 10px;
            border: 1px solid #ccc;
            border-radius: 4px;
            margin-right: 5px;
        }

        .chat-form button {
            padding: 10px;
            background-color: #007acc;
            color: #fff;
            border: none;
            cursor: pointer;
        }

        .chat-form button:hover {
            background-color: #005f99;
        }
    </style>
</head>
<body>

    <header>
        <h1>TAMEKLO Komlan Mawuli - Spécialiste en Machine Learning & Développement Web</h1>
    </header>

    <nav>
        <a href="#about">À propos</a>
        <a href="#services">Services</a>
        
        <a href="#contact">Contact</a>
    </nav>

    <dadius: 8px;
            display: flex;
            flex-direction: column;
            box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
            overflow: hidden;
        }

        /* Boîte de chat */
        .chat-box {
            flex: 1;
            padding: 15px;
            overflow-y: auto;
            border-bottom: 1px solid #ffff;
        }

        /* Styles des messages */
        .message {
            margin: 10px 0;
            padding: 8px 12px;
            border-radius: 20px;
            max-width: 75%;
            display: inline-block;
        }

        .message.user {
            background-color: #dcf8c6;
            align-self: flex-end;
        }

        .message.bot {
            background-color: #f1f0f0;
            align-self: flex-start;
        }

        /* Champ de saisie et bouton */
        input[type="text"] {
            padding: 15px;
            border: none;
            border-top: 1px solid #ffff;
            width: calc(100% - 100px);
            border-radius: 0 0 0 20px;
            box-sizing: border-box;
        }

        button {
            padding: 15px;
            border: none;
            background-color: #007bff;
            color: white;
            cursor: pointer;
            border-radius: 0 0 20px 0;
        }

        button:hover {
            background-color: #0056b3;
        }
  