---
title: Saisie du schéma
layout: page
excerpt: Utilisation de l'éditeur de schéma et de création de composants avec l'éditeur de symboles.
---

# Schéma de la carte

La carte réalisée dans ce module est une carte utilisant un microcontrôleur PIC (PIC16F1788) autour duquel on trouvera différentes entrées/sorties :

* 2 boutons poussoirs
* 2 interrupteurs
* 4 LEDs
* Une liaison série
* Un LCD 2x16 caractères

Cette carte pourra servir de point de départ pour le projet de deuxième année.

Le schéma de la carte est le suivant :

![]({% include img_link.html file="Carte_PIC_CAO.png" %})

Il est également disponible en [PDF]({% include file_link.html file="Carte_PIC_CAO.pdf" %}).

# Personnalisation du cartouche du schéma

Compléter le cartouche du schéma avec les informations suivantes en suivant la vidéo ci-dessous :

| Champ        | Contenu                                       |
| ------------ | --------------------------------------------- |
| Date         | Mettre la date du jour en cliquant sur \<\<\< |
| Révision     | 1.0                                           |
| Titre        | Carte PIC - TP CAO                            |
| Société      | IUT LYON 1 - GEII                             |
| Commentaire1 | NOM Prenom                                    |
| Commentaire2 | G20x                                          |

{% include youtube_video.html youtube_id="yXfSvNJac3c" %}

# Création d'un symbole

La bibliothèque Kicad contient de nombreuses références de composants mais il arrive que le composant cherché ne soit pas présent. Certains composants de la bibliothèque peuvent présenter des erreurs ou bien avoir un schéma ne correspondant pas à ce que l'on souhaite.

Quand cela arrive, on peut effectuer une recherche internet pour voir si quelqu'un d'autre a déjà créé le composant ou utiliser l'éditeur de symboles pour créer son propre composant.

La vidéo suivante montre les étapes de la création du symbole du microcontrôleur PIC16F1788 utilisé sur la carte que nous allons créer dans ce module. Ce composant est déjà présent dans la librairie que vous avez téléchargée mais la procédure servira de modèle à la création du symbole du LCD que vous devrez faire dans la prochaine partie.

Les informations nécessaires à la création de ce composant sont présentes dans la [datasheet](http://ww1.microchip.com/downloads/en/DeviceDoc/40001675C.pdf) en particulier les informations suivantes :

| -------------- | ------------------------------------------------------------- |
| Nom du symbole | PIC16F1788-xSP                                                |
| Description    | 16KB Flash, 2KB SRAM, 256B EEPROM, XLP, DIP28                 |
| Mots           | Flash-Based 8-Bit CMOS Microcontroller                        |
| Documentation  | http://ww1.microchip.com/downloads/en/DeviceDoc/40001675C.pdf |

[Suite...]({{site.baseurl}}/enonces/tp3)
