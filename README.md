# BRYSS AI — première version

BRYSS AI est une première interface web responsive, avec une identité visuelle noir / violet / bleu.

## Lancer l'interface
- Ouvrez `index.html` dans un navigateur pour tester l'interface en mode aperçu.
- Les messages de démonstration ne sont pas générés par un vrai modèle IA.

## Activer le moteur IA
1. Installez Node.js (version 18 ou plus récente).
2. Dans ce dossier, lancez `npm install`.
3. Copiez `.env.example` vers `.env`.
4. Ajoutez votre clé API dans `OPENAI_API_KEY`.
5. Lancez `npm start`, puis ouvrez http://localhost:3000.

La clé API reste côté serveur et ne doit jamais être ajoutée au HTML ou au JavaScript du navigateur.

## Déjà inclus
- **Robot guide « Bry » + 29 langues** (FR, EN, NL, ES, AR, PT, DE, IT, TR, RU, UK, PL, ZH, JA, KO, HI, BN, UR, FA, ID, VI, TH, SV, EL, HE, RO, CS, HU, SW) avec recherche, arabe/persan/ourdou/hébreu en lecture droite→gauche, et voix du robot en option (synthèse vocale du navigateur). Pour ajouter une langue : ajouter une ligne dans `META` et un objet dans `T` (dans index.html).
- **Animation de bienvenue** au tout premier lancement (5 écrans animés qui présentent BRYSS AI) : affichée une seule fois, bouton « Passer » à tout moment (Échap marche aussi). Elle peut être revue depuis Paramètres → « Revoir la présentation ». Pour la retester : supprimez la clé `bryss_intro_done_v1` du localStorage.
- Application installable (PWA) : icônes, manifest et service worker inclus (fonctionne en https ou sur localhost)
- Interface responsive ordinateur / tablette / mobile
- Historique local dans le navigateur
- Nouvelle conversation
- Dictée vocale si le navigateur la prend en charge
- Sélection de fichiers (aperçu, pas encore d'analyse du contenu)
- Export de conversation en .txt
- Connexion serveur à l'API OpenAI (après configuration)

## À développer ensuite
Recherche web connectée, génération d'images, lecture/analyse réelle des PDF et documents, mémoire synchronisée, authentification, abonnements/paiements et publication sur un hébergement web.

## Publier sur GitHub Pages (mode démo, sans serveur)
Envoyez tout le contenu du dossier dans un dépôt GitHub, puis Settings → Pages → Deploy from branch → `main` / root. L'interface et l'animation fonctionnent ; les vraies réponses IA demandent le serveur Node (`npm start`) hébergé ailleurs (Render, Railway…).

---
BRYSS AI — créé par Issam Akdi & Bryana Lebon
