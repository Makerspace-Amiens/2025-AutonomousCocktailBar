---
layout: default
nav_order: 5
title: Conception et prototypage
---

# Conception et prototypage
1. 🛠️ Conception mécanique
🔹 Structure
La structure du système est construite à partir de profilés aluminium V-slot, choisis pour leur solidité, leur modularité et leur compatibilité avec les systèmes de guidage à roulettes.
Environ 6,6 mètres de profilés ont été découpés pour former un rail linéaire permettant le déplacement du support de verre.

🔹 Support de verre
Le support est conçu pour maintenir le verre de manière stable, tout en étant suffisamment léger pour ne pas surcharger le moteur. Il est fixé à une courroie crantée, entraînée par une poulie connectée au moteur pas à pas.

🔹 Guidage
Le support se déplace le long du rail grâce à des roues V-slot, assurant un mouvement fluide, silencieux et linéaire. Ce système garantit un déplacement précis et sans vibrations.

2. ⚡ Conception électronique
🔹 Schéma de principe
Microcontrôleur : ESP32 NodeMCU

Driver moteur : TMC2209, connecté en mode STEP/DIR

Alimentation moteur : source 12V dédiée

Alimentation de l’ESP32 : via USB ou régulateur 5V

Condensateur de filtrage : utilisé pour stabiliser la tension côté moteur

![Capture d'écran 2025-06-12 134458](https://github.com/user-attachments/assets/ca00c66c-009b-499a-8ebf-0c6cd8e9b7cd)

🔹 Broches utilisées (ESP32) :
DIR_PIN = GPIO12 → définit la direction du moteur

STEP_PIN = GPIO14 → envoie les impulsions de déplacement
![1000010292](https://github.com/user-attachments/assets/e588fd2f-590b-4be2-8898-19f78f92294d)

🔹 Sécurité
L’architecture prévoit la possibilité d’ajouter des capteurs de fin de course ou un système de détection de blocage via la technologie StallGuard du TMC2209.

L’alimentation du moteur est séparée de celle de l’ESP32, afin d’éviter tout pic de courant sur le microcontrôleur.

3. 💻 Conception logicielle
🔹 Fonctionnalités
Le système intègre un serveur web embarqué directement sur l’ESP32, accessible via Wi-Fi.
L’interface propose deux actions principales :

Service à gauche

Service à droite
Chaque action déclenche le déplacement du verre dans la direction correspondante à l’aide d’impulsions STEP/DIR.

🔹 Interaction utilisateur
L’utilisateur se connecte au réseau Wi-Fi créé par l’ESP32 : « ESP32-BarAuto »

Il accède à l’interface web via l'adresse ip de l'ESP 32

Une page HTML, stylisée en CSS, s’affiche avec deux boutons de commande

Lorsqu’un bouton est cliqué, une requête HTTP est envoyée à l’ESP32, qui pilote le moteur en conséquence
