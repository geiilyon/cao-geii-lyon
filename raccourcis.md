---
layout: page
title: Raccourcis
excerpt: Raccourcis claviers et astuces.
permalink: /raccourcis/
---

# Utilisation de la souris

Double-cliquer sur un élement ouvre la boîte de dialogue permettant son édition.


# Raccourcis clavier

Kicad possède un concept d'*accelerator key* et de *hotkey*.

*accelerator key* : équivalent d'un clic sur l'icône de la barre de menu
*hotkey* : équivalent d'un clic sur l'icône de la barre de menu suivi d'un clic gauche de la souris à l'emplacement du curseur.

Les raccourcis de type *accelerator key* utilisent la même touche que la *hotkey* combiné avec la touche <kbd>Shift</kbd> (parfois également appelée <kbd>Maj</kbd> de symbole <kbd>⇧</kbd>).

Exemple : le raccourci  <kbd>Shift</kbd>+<kbd>w</kbd> permet de basculer en mode dessin de fil lors de la saisie du schéma et il est ensuite nécessaire de cliquer sur la souris pour démarrer une connexion. L'appui sur <kbd>w</kbd> démarre immédiatement le tracé d'une connexion depuis l'emplacement courant de la souris.

![]({% include img_link.html file="hotkeys.gif" %})


## Editeur de schéma (Eeschema)

| Fonction                                           | Raccourcis                   |
| -------------------------------------------------- | ---------------------------- |
| Retour au mode de sélection (flèche)               | <kbd>Esc</kbd>               |
| Ajouter un symbole                                 | <kbd>a</kbd>                 |
| Déplacer un élément (move)                         | <kbd>m</kbd>                 |
| Copier un symbole ou un label                      | <kbd>c</kbd>                 |
| Ajouter une équipotentielle d'alimentation (Power) | <kbd>p</kbd>                 |
| Commencer un fil (wire)                            | <kbd>w</kbd>                 |
| Editer un élément (symbole, référence, valeur,...) | <kbd>e</kbd>                 |
| Ajouteur du texte (graphique)                      | <kbd>t</kbd>                 |
| Déplacer un item en maintenant les liens (drag)    | <kbd>g</kbd>                 |
| Supprimer un élément                               | <kbd>Del</kbd>               |
| Rotation d'un élément                              | <kbd>r</kbd>                 |
| Miroir X                                           | <kbd>x</kbd>                 |
| Miroir Y                                           | <kbd>y</kbd>                 |
| Copier un bloc                                     | <kbd>Ctrl</kbd>+<kbd>C</kbd> |
| Coller un bloc                                     | <kbd>Ctrl</kbd>+<kbd>V</kbd> |
| Couper un bloc                                     | <kbd>Ctrl</kbd>+<kbd>X</kbd> |
| Editer la valeur d'un symbole                      | <kbd>v</kbd>                 |
| Editer l'empreinte (Footprint) d'un symbole        | <kbd>f</kbd>                 |
| Editer la référence d'un symbole                   | <kbd>u</kbd>                 |
| Trouver un élément                                 | <kbd>Ctrl</kbd>+<kbd>F</kbd> |
| Déplacer un bloc en maintenant les liens (Drag)    | <kbd>Tab</kbd>               |

## Editeur de circuit imprimé (Pcbnew)

| Fonction                                                | Raccourcis                    |
| ------------------------------------------------------- | ----------------------------- |
| Retour au mode de sélection (flèche)                    | <kbd>Esc</kbd>                |
| Passer en mode routage d'une piste simple               | <kbd>Shift</kbd>+<kbd>X</kbd> |
| Démarrer le routage d'une piste simple                  | <kbd>X</kbd>                  |
| Changer de couche (place un via si en routage en cours) | <kbd>v</kbd>                  |
| Origine des coordonnées relatives                       | <kbd>Espace</kbd>             |
| Déplacer une piste à 45° (drag)                         | <kbd>d</kbd>                  |
| Déplacer une piste à angle quelconque (drag)            | <kbd>g</kbd>                  |
| Déplacer un composant (move)                            | <kbd>M</kbd>                  |
| Faire tourner un composant (rotate)                     | <kbd>R</kbd>                  |
| Sélectionner le segment de piste (entre 2 pastilles)    | <kbd>U</kbd>                  |
| Sélectionner toutes les pistes connectées (même noeud)  | <kbd>I</kbd>                  |

## Editeur de symbole

*à venir*


# Zoom et pan en utilisant le trackpad ou la souris

{% include youtube_video.html youtube_id="lao9N2P1w0s" %}

Pour recentrer l'affichage sur la totalité du schéma, il faut appuyer sur la touche <kbd>Home</kbd> (<kbd>↖︎</kbd>)