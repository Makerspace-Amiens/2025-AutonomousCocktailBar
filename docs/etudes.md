---
layout: default
nav_order: 4
title: Études et choix techniques
---

# Études et choix techniques

Le développement du bar à cocktail automatique repose sur des choix techniques adaptés aux contraintes du projet : précision de dosage, compacité, connectivité sans fil, coût réduit et simplicité d’usage. Cette section présente les différentes solutions étudiées et justifie les choix retenus, répartis en trois sous-systèmes : mécanique, électronique et logiciel.

1. 🛠️ Système de motorisation et déplacement
🔍 Étude des solutions :
Plusieurs types de motorisation ont été envisagés pour assurer le déplacement du verre :

Moteur DC : rotation continue mais nécessite un codeur pour connaître la position.

Servo-moteur : précis, mais limité en angle (généralement 180°).

Moteur pas à pas : permet un déplacement précis sans capteur, idéal pour le mouvement linéaire.

✅ Choix retenu : Moteur pas à pas NEMA 17
Offrant un bon couple et une précision de positionnement.

Compatible avec des systèmes de guidage linéaire par courroie.

Adapté aux mouvements discrets et répétables du support de verre.

![Capture d'écran 2025-06-12 130628](https://github.com/user-attachments/assets/2db0f274-1c60-4c39-b6f7-e56a1bb87078)
---
( photo du moteur) 
2. 🔌 Pilotage moteur
🔍 Étude des drivers disponibles :
A4988 : économique, mais bruyant et limité en options.

DRV8825 : plus puissant, mais sans fonctions avancées.

TMC2209 : silencieux, intelligent, faible consommation.

✅ Choix retenu : TMC2209
StallGuard : détecte les blocages du moteur sans capteur externe.

CoolStep : réduit automatiquement le courant pour économiser l’énergie.

StealthChop2 : garantit un fonctionnement silencieux et fluide.

Parfaitement compatible avec l’ESP32 en mode STEP/DIR.

![Capture d'écran 2025-06-12 131431](https://github.com/user-attachments/assets/f55a1ed0-11e2-4e6b-9e96-9b2195e9bc25)
---
(photo TMC2209)
3. ⚡ Architecture électronique
🔍 Solutions étudiées :
Arduino Uno : limité en mémoire et sans Wi-Fi.

Raspberry Pi : trop puissant pour l’application et plus coûteux.

ESP32 : puissant, compact, économique, et Wi-Fi intégré.

✅ Choix retenu : ESP32 NodeMCU
Double cœur, jusqu’à 240 MHz, permet la gestion simultanée du web et du moteur.

Wi-Fi intégré pour piloter le bar via une interface web locale.

Nombreuses entrées/sorties compatibles avec les capteurs, moteurs et drivers.
![Capture d'écran 2025-06-12 131614](https://github.com/user-attachments/assets/0c802511-6e39-47a3-bc38-38ce220e1d6d)
(photo esp 32)

---


4. 🔧 Structure mécanique
🔍 Alternatives étudiées :
Bois ou contreplaqué : simple mais peu durable.

Pièces imprimées en 3D : légères mais fragiles pour les charges dynamiques.

Profilés aluminium V-slot : robustes, modulaires et compatibles avec des guidages précis.

✅ Choix retenu : profilés aluminium V-slot
Permettent un montage précis et évolutif.

Compatibles avec des roues V-slot pour un mouvement fluide.

Offrent une bonne rigidité pour supporter le mouvement du verre et le poids de la mécanique.

5. 🌐 Interface utilisateur
🔍 Options envisagées :
Écran OLED local : plus complexe à implémenter et usage limité.

Application mobile : nécessite développement externe et app à installer.

Interface web locale : légère, rapide, accessible via navigateur.

✅ Choix retenu : interface web embarquée dans l’ESP32
Création d’un point d’accès Wi-Fi local : « ESP32-BarAuto ».

Interface HTML/CSS simple, hébergée sur l’ESP32, avec deux boutons de commande.

Pas besoin d’Internet ni d’installation externe → utilisation immédiate depuis un smartphone ou un PC.
