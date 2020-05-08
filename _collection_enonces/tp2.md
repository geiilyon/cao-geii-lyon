---
title: Saisie du schéma
layout: page
excerpt: Utilisation de l'éditeur de schéma et création de composants avec l'éditeur de symboles
---

# Schéma de la carte

La carte réalisée dans ce module est une carte utilisant un microcontrôleur PIC (PIC16F1788) autour duquel on trouvera différentes entrées/sorties :

* 2 boutons poussoirs
* 2 interrupteurs
* 4 LEDs
* Une liaison série
* Un LCD 2x16 caractères

La carte contient également un connecteur permettant de brancher un programmateur/débugger (PICKIT 3 ou 4, SNAP, ...).

Cette carte pourra servir de point de départ pour le projet de deuxième année.

Le schéma de la carte est le suivant :

![]({% include img_link.html file="Carte_PIC_CAO.png" %})

Il est également disponible en [PDF]({% include file_link.html file="Carte_PIC_CAO.pdf" %}).

# Personnalisation du cartouche du schéma

Compléter le cartouche du schéma avec les informations suivantes en se référant à la vidéo ci-dessous :

| Champ        | Contenu                                       |
| ------------ | --------------------------------------------- |
| Date         | Mettre la date du jour en cliquant sur \<\<\< |
| Révision     | 1.0                                           |
| Titre        | Carte PIC - TP CAO                            |
| Société      | IUT LYON 1 - GEII                             |
| Commentaire1 | NOM Prenom                                    |
| Commentaire2 | G20x                                          |

{% include youtube_video.html youtube_id="yXfSvNJac3c" %}


# Saisie du schéma

Pour la saisie du schéma, il faut au préalable regarder la première vidéo du tutoriel d'Eric Peronnin (enseignant à l'IUT de Nantes) sur l'utilisation de l'éditeur de schéma pour se former à l'utilisation d'EESchema.
<span style="font-weight: bold;color:red">Le schéma que vous devrez saisir sera différent</span>.

{% include youtube_video.html youtube_id="C9EWrKw9Qz8" %}

Pour compléter le schéma vous aurez besoin de la liste des noms des symboles (**tableau ci-dessous**) et des outils suivants :
* Les alimentations (+5V, GND) ainsi que les POWER_FLAG se placent avec l'outil ![]({% include img_link.html file="icone_placer_symbole_power.png" %})
* Les labels globaux ![]({% include img_link.html file="label_global_pot2.png" %}), ![]({% include img_link.html file="label_global_LCD_D4.png" %}) se placent avec l'outil ![]({% include img_link.html file="icone_placer_label_global.png" %}) (la barre au dessus de MCLR est obtenue en tapant `~MCLR`)
* Les pattes non connectées ![]({% include img_link.html file="patte_NC.png" %}) se placent avec l'outil ![]({% include img_link.html file="icone_NC.png" %})
* Les lignes bleues se dessinent avec l'outil ![]({% include img_link.html file="icone_placer_lignes_polygone_graphiques.png" %}) (pour les modifier il faut utilser la commande *drag*, raccourci : touche <kbd>g</kbd>)

Vous devez maintenant réaliser la saisie du [schéma]({% include file_link.html file="Carte_PIC_CAO.pdf" %}) de la carte avec le PIC présenté en début de page en laissant de côté l'afficheur LCD (DS1). Ce composant sera créé dans la partie suivante. Il faut utiliser les symboles listés dans le tableau ci-dessous, la deuxième colonne précise le nom de la bibliothèque et la troisième le nom du symbole. Dans le champ de filtre de recherche on peut taper des bouts des noms des librairies, des symboles ou encore des mots clés.

| Reference(s)         | Nom de la librairie | Nom du symbole                                                                     |
| -------------------- | ------------------- | ---------------------------------------------------------------------------------- |
| C1, C6, C7, C8       | Device              | C                                                                                  |
| C2, C4, C5, C9, C10  | Device              | C                                                                                  |
| C3                   | Device              | CP_Small                                                                           |
| D1, D2               | Device              | LED                                                                                |
| D3, D4               | Device              | LED                                                                                |
| DS1                  | G20x_Nom_symboles   | <span style="font-weight: bold;color:red">composant qui sera créé plus tard</span> |
| J1                   | Connector           | Screw_Terminal_01x02                                                               |
| J2                   | Connector_Generic   | Conn_01x06                                                                         |
| J3                   | Connector           | DB9_Male_MountingHoles                                                             |
| J4                   | Connector_Generic   | Conn_01x08                                                                         |
| J5                   | Connector           | Conn_PIC_ICSP_ICD                                                                  |
| R1, R3, R5, R6, R14  | Device              | R                                                                                  |
| R2, R4, R11          | Device              | R                                                                                  |
| R7, R8, R9, R10, R13 | Device              | R                                                                                  |
| R12                  | Device              | R                                                                                  |
| RV1, RV2             | Device              | R_POT                                                                              |
| SW1, SW2             | Switch              | SW_Push                                                                            |
| SW3                  | Switch              | SW_DIP_x02                                                                         |
| U1                   | Interface_UART      | MAX232                                                                             |
| U2                   | IUT_CAO_symboles    | PIC16F1788-xSP                                                                     |

# Création des symboles non disponibles

## Exemple de création d'un symbole (PIC16F1788)

La bibliothèque Kicad contient de nombreuses références de composants mais il arrive que le composant cherché ne soit pas présent. Certains composants de la bibliothèque peuvent présenter des erreurs ou bien avoir un schéma ne correspondant pas à ce que l'on souhaite.

Quand cela arrive, on peut effectuer une recherche internet pour voir si quelqu'un d'autre a déjà créé le composant ou utiliser l'éditeur de symboles pour créer son propre composant.

La vidéo suivante montre les étapes de la création du symbole du microcontrôleur PIC16F1788 utilisé sur la carte développée.
<span style="font-weight: bold;color:red">Ce composant est déjà présent dans la librairie que vous avez téléchargée mais la procédure servira de modèle à la création du symbole du LCD que vous devrez faire dans la prochaine partie</span>.

Les informations nécessaires à la création de ce composant sont présentes dans la [datasheet](http://ww1.microchip.com/downloads/en/DeviceDoc/40001675C.pdf), en particulier les informations suivantes :

| -------------- | ------------------------------------------------------------- |
| Nom du symbole | PIC16F1788-xSP                                                |
| Description    | 16KB Flash, 2KB SRAM, 256B EEPROM, XLP, DIP28                 |
| Mots           | Flash-Based 8-Bit CMOS Microcontroller                        |
| Documentation  | http://ww1.microchip.com/downloads/en/DeviceDoc/40001675C.pdf |

{% include youtube_video.html youtube_id="we7QEF_KYRw" %}

Sommaire de la vidéo (pour un accès direct aux principales étapes) :

1. <a href="https://www.youtube.com/watch?v=we7QEF_KYRw&t=34s" target="_blank">Recherche dans les librairies</a>
1. <a href="https://www.youtube.com/watch?v=we7QEF_KYRw&t=60s" target="_blank">Utilisation du filtre de recherche</a>
1. <a href="https://www.youtube.com/watch?v=we7QEF_KYRw&t=179s" target="_blank">Notion d'alias de composant</a>
1. <a href="https://www.youtube.com/watch?v=we7QEF_KYRw&t=210s" target="_blank">Copie dans la librairie personnelle</a>
1. <a href="https://www.youtube.com/watch?v=we7QEF_KYRw&t=243s" target="_blank">Edition des propriétés du symbole</a>
1. <a href="https://www.youtube.com/watch?v=we7QEF_KYRw&t=310s" target="_blank">Suppression des alias</a>
1. <a href="https://www.youtube.com/watch?v=we7QEF_KYRw&t=360s" target="_blank">Types de pattes</a>
1. <a href="https://www.youtube.com/watch?v=we7QEF_KYRw&t=421s" target="_blank">Edition des pattes</a>
1. <a href="https://www.youtube.com/watch?v=we7QEF_KYRw&t=522s" target="_blank">Modification du rectangle</a>
1. <a href="https://www.youtube.com/watch?v=we7QEF_KYRw&t=606s" target="_blank">Vérification du composant</a>

## Création du symbole du LCD

Créer un symbole de schématique (afficheur LCD 162B) à partir d’un symbole existant (HY1602E) et le sauvegarder dans votre bibliothèque schématique personnelle (G20x_Nom_symboles.lib) en utilisant les informations dans le tableau ci-dessous.

L'empreinte étant présente dans la librairie d'empreintes de l'IUT, il faut d'abord l'ajouter à la table des librairies spécifiques au projet (sur le même modèle que ce que nous avons fait pour la librairie de symboles).

{% include youtube_video.html youtube_id="aVPmBOjBtfw" %}

Remarques importantes pour la création du LCD :

* le symbole HY1602E ne possède pas d'alias, il n'est donc pas nécessaire de les supprimer.
* il y a une différence entre le HY1602E et le 162B (LED de rétroéclairage sur les pattes 1 et 2).

| Reference      | DS                                                                                          |
| -------------- | ------------------------------------------------------------------------------------------- |
| Valeur         | 162B-CC-BC-3LP                                                                              |
| Empreinte      | IUT_CAO_empreintes:162B                                                                     |
| Documentation  | https://cdn.displaytech-us.com/sites/default/files/display-data-sheet/162B%20series-v21.pdf |
| Nom du symbole | 162B-CC-BC-3LP                                                                              |
| Description    | LCD 16x2 Alphanumeric 16pin Blue/Yellow/Green Backlight 8bit parallel 5V VDD                |
| Mots clé       | display LCD 7-segment                                                                       |

![]({% include img_link.html file="lcd_162b.png" %})

Finir la saisie du schéma en utilisant le symbole LCD que vous venez de créer.

## Annotation des différents composants schématiques

Utiliser l'annotation automatique ![]({% include img_link.html file="icone_annotation.png" %}) et vérifier que l'option "Trier les composants par position X" est selectionnée.

![]({% include img_link.html file="annotation_auto.png" %})

Attention, si la position des composants sur votre schéma est légèrement différente par rapport au schéma de référence il peut y avoir des différences dans les annotations.
Les références peuvent être modifiées manuellement en plaçant la souris au dessus de la référence et en tapant sur la touche <kbd>e</kbd> du clavier.

## Vérification des règles électriques

Une fois la saisie terminée, il faut lancer une vérification des règles électriques ERC (*Electrical Rules Check*) en cliquant sur l'icône qui représente une coccinelle ![]({% include img_link.html file="debug_coccinelle.png" %}) puis sur le bouton **Exécuter**.
Attendre que le texte *fini* appraisse dans la fenêtre des messages et vérifier que la liste des erreurs est vide.
