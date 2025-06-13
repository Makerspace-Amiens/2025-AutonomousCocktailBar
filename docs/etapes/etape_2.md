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
| Problème                                   | Cause probable                              | Solution                                          |
| ------------------------------------------ | ------------------------------------------- | ------------------------------------------------- |
| Les pièces ne s’emboîtent pas correctement | Découpe imprécise ou mauvais alignement     | Vérifiez les dimensions et réalignez les éléments |
| La courroie glisse ou saute                | Mauvaise tension ou poulie mal fixée        | Ajustez la tension et resserrez la poulie         |
| Le support de verre se bloque              | Roues mal montées ou profilés mal alignés   | Resserrer les roues et réaligner les rails        |
| Le moteur ne réagit pas                    | Mauvais câblage ou alimentation défectueuse | Refaire les connexions, tester avec un multimètre |


