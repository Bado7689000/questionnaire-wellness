# Suivi de forme - application installable

Ce dossier contient une Progressive Web App (PWA) autonome.

## Fichiers à publier
Publiez ensemble, sans changer les noms :
- index.html
- manifest.webmanifest
- service-worker.js
- icon-180.png
- icon-192.png
- icon-512.png

Ils doivent être placés sur un hébergement HTTPS. Un simple envoi du ZIP aux sportifs ne permet pas l'installation comme application : le service worker exige une adresse web sécurisée.

## Installation sur iPhone / iPad
1. Ouvrir l'adresse web dans Safari.
2. Appuyer sur Partager.
3. Choisir « Sur l'écran d'accueil ».
4. Appuyer sur Ajouter.

## Installation sur Android
1. Ouvrir l'adresse web dans Chrome.
2. Ouvrir le menu du navigateur.
3. Choisir « Installer l'application » ou « Ajouter à l'écran d'accueil ».

## Fonctionnement autonome
Après une première ouverture avec Internet, le questionnaire fonctionne hors connexion. Les réponses restent sur le téléphone dans le stockage local. Aucune donnée n'est envoyée à un serveur.

Le partage WhatsApp nécessite toutefois une connexion Internet et une validation par le sportif. Le téléphone ouvre sa feuille de partage avec le CSV lorsqu'il accepte ce type de fichier. Sinon, le CSV est téléchargé et WhatsApp est ouvert avec un message prérempli afin que le sportif joigne le fichier.

## Mise à jour
Pour publier une nouvelle version, remplacez les fichiers sur l'hébergement et modifiez la valeur CACHE dans service-worker.js (par exemple suivi-forme-v2).
