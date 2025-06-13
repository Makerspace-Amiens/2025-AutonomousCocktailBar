---
layout: default
nav_order: 5
title: Conception et prototypage
---

# Conception et prototypage
Cette section décrit la conception mécanique, électronique et logicielle du bar à cocktail automatique. Elle regroupe les plans, schémas et choix retenus pour assurer un fonctionnement fiable et cohérent.

1. Conception mécanique
🔹 Structure
Réalisée à partir de profilés aluminium V-slot pour leur modularité, solidité et compatibilité avec les roues de guidage.

Longueur totale : environ 660 cm de profilés, découpés pour former un rail linéaire sur lequel le support du verre peut se déplacer.

🔹 Support de verre
Conçu pour maintenir fermement le verre tout en étant assez léger pour ne pas surcharger le moteur.

Fixé à une courroie crantée qui transmet le mouvement via une poulie entraînée par le moteur pas à pas.

🔹 Guidage
Utilisation de roues V-slot pour un glissement fluide du support sur le rail.

Le système permet un déplacement linéaire précis et silencieux.

2. Conception électronique
🔹 Schéma de principe
Microcontrôleur : ESP32 NodeMCU.

Driver moteur : TMC2209 connecté en mode STEP/DIR.

Alimentation moteur : source 12V dédiée.

Alimentation ESP32 : via USB ou régulateur 5V.

Condensateur de filtrage : pour stabiliser la tension moteur.

Broches utilisées :

DIR_PIN = GPIO12 → direction du moteur

STEP_PIN = GPIO14 → impulsions de déplacement

🔹 Sécurité
Possibilité d'ajouter ultérieurement des capteurs de fin de course ou de blocage via StallGuard.

Alimentation séparée pour éviter les pics de courant sur l’ESP32.

3. Conception logicielle
🔹 Fonctionnalités
Serveur web intégré dans l’ESP32, accessible en Wi-Fi.

Interface web intuitive avec deux boutons : Service à gauche et Service à droite.

Commande directe du moteur via impulsions STEP/DIR selon la direction souhaitée.

🔹 Interaction utilisateur
L'utilisateur se connecte au Wi-Fi « ESP32-BarAuto ».

Il accède à l’interface en ouvrant http://192.168.4.1 dans son navigateur.

Une page HTML stylisée s’affiche avec les deux boutons.

En cliquant, une requête est envoyée à l’ESP32 qui déclenche le déplacement du verre.

