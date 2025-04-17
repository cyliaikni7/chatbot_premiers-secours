# chatbot_premiers-secours
Chatbot-de-premiers-secours : Une solution intelligente basée sur un modèle de langage (LLM)

Description Générale de notre Projet de Chatbot basé sur un LLM :
Titre du Projet : Chatbot pour les Premiers Secours

Contexte et Motivation : Dans le cadre du module sur les modèles de langage de grande taille (LLM), nous avons développé un chatbot intelligent capable de répondre à des questions sur les premiers secours. L'objectif principal est de créer un assistant virtuel fiable qui peut aider les utilisateurs à obtenir des informations cruciales en temps réel sur les pratiques de premiers secours, améliorant ainsi l'accès à des informations vitales de manière rapide et efficace.

Technologies Utilisées :

NLP et Modèle LLM :

BERT (Bidirectional Encoder Representations from Transformers) : Nous avons utilisé BERT pour la classification des intentions en raison de sa capacité à comprendre le contexte bidirectionnel des phrases. BERT est pré-entraîné sur un large corpus de textes, ce qui lui permet de capturer des nuances complexes du langage naturel.
Bibliothèques et Outils :
NLTK (Natural Language Toolkit) : Utilisé pour la tokenisation et la préparation des données de texte. Transformers (Hugging Face) : Fournit une interface pour travailler avec le modèle BERT. PyTorch : Utilisé pour l'entraînement et la manipulation des modèles de machine learning. Gradio : Utilisé pour créer une interface utilisateur simple et interactive.
Étapes du Projet :
1-Chargement des Données :
Nous avons collecté et chargé les intentions de conversation (fichier intents.json) contenant des catégories d'intentions, des motifs de questions, et des réponses associées.
2-Préparation des Données :
Utilisation du tokenizer BERT pour convertir les questions en tokens. Encodage des étiquettes (labels) des intentions pour les convertir en valeurs numériques à utiliser par le modèle.
3-Création du Modèle :
Chargement du modèle B ERT pré-entraîné et ajout de couches de classification. Définition de l'optimiseur AdamW pour la mise à jour des poids du modèle.
4-Entraînement du Modèle :
Entraînement du modèle sur les données préparées, en ajustant les poids pour minimiser la perte. Sauvegarde du modèle entraîné pour une utilisation ultérieure.
5-Développement de l'Interface Utilisateur :
Création d'une interface utilisateur interactive avec Gradio, permettant aux utilisateurs de poser des questions et de recevoir des réponses en temps réel.
6-Fonctionnement du Chatbot :
Prédiction des Intentions : Lorsqu'un utilisateur envoie une question, le message est tokenisé et passé au modèle BERT. Le modèle prédit la catégorie d'intention la plus probable basée sur le contexte de la question. Génération de Réponses : Une fois l'intention prédite, une réponse appropriée est sélectionnée aléatoirement parmi les réponses prédéfinies associées à cette intention.
Exemple de Scénario d'Utilisation :
L'utilisateur pose la question : "Which medicine to take if I get a mild fever?" "fever" Le chatbot tokenise la question et la passe au modèle BERT. Le modèle prédit que l'intention est liée à "fever". Le chatbot renvoie une réponse appropriée, telle que "["To treat a fever at home: 1)Drink plenty of fluids to stay hydrated. 2)Dress in lightweight clothing…."]
Conclusion : Ce projet démontre l'application des modèles de langage de grande taille dans la création de chatbots intelligents capables de comprendre et de répondre à des questions complexes dans un domaine spécifique. En utilisant des technologies avancées comme BERT et en intégrant une interface utilisateur conviviale, nous avons développé un outil précieux pour l'éducation et la diffusion des connaissances en premiers secours.


