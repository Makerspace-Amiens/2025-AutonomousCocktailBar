---
layout: default
title: Assemblage
parent: Etapes de fabrication
nav_order: 2
---

# Assemblage
Après la préparation et la vérification des matériaux, vient l’étape d’assemblage. Elle consiste à construire la structure du bar automatique, installer les composants électroniques et s’assurer de la solidité de l’ensemble.

## Étapes d'Assemblage

Organisation

Disposez tous les composants mécaniques et électroniques sur un plan de travail propre et dégagé.

Regroupez les pièces par catégorie (visserie, profilés, électronique) pour gagner en efficacité.

Assemblage initial

Assemblez la structure principale à l’aide des profilés aluminium V-slot, des équerres de fixation et de la visserie.

Installez les roues V-slot sur le support de verre.

Placez la courroie crantée le long du rail et passez-la autour de la poulie du moteur.

Fixation

Montez le moteur pas à pas NEMA 17 sur son support et alignez-le avec la courroie.

Fixez solidement le support de verre au chariot mobile.

Connectez le driver TMC2209 au moteur et raccordez-le à l’ESP32 selon le schéma électronique prévu.
## Vérifications à Effectuer
Alignement :

Vérifiez que la poulie est bien centrée et que la courroie suit un trajet rectiligne.

Le support de verre doit se déplacer librement sans frottement excessif.

Stabilité :

L’ensemble de la structure doit être rigide.

Aucun jeu mécanique ne doit être présent entre les profilés ou les pièces mobiles.

Câblage :

Contrôlez visuellement et à l’aide d’un multimètre la bonne connexion des fils.

Assurez-vous que l’alimentation du moteur et celle de l’ESP32 sont correctement séparées.

## Problèmes Communs et Solutions
Lors de l’assemblage du bar à cocktail automatique, plusieurs problèmes peuvent apparaître. Voici une liste des cas fréquents, avec leurs causes probables et les solutions correspondantes :

Les pièces ne s’emboîtent pas correctement
Cause probable : une découpe imprécise ou un mauvais alignement des éléments.
Solution : vérifier les dimensions et réaligner soigneusement les composants.

La courroie glisse ou saute
Cause probable : tension insuffisante ou poulie mal fixée.
Solution : ajuster correctement la tension de la courroie et resserrer la poulie.

Le support de verre se bloque lors du déplacement
Cause probable : montage incorrect des roues ou mauvais alignement des profilés.
Solution : revisser les roues et vérifier l’alignement des rails.

Le moteur ne réagit pas
Cause probable : câblage incorrect ou problème d’alimentation.
Solution : vérifier et refaire les connexions, puis tester l’alimentation avec un multimètre.
