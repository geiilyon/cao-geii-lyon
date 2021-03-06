---
title: Création d'empreintes
layout: page
excerpt: Utilisation de l'éditeur d'empreintes
---

# Création d'une librairie d'empreintes

Lors de la configuration du projet, on avait ajouté la librairie d'empreintes de l'IUT (dossier `IUT_CAO_empreintes.pretty`).
Dans cette partie nous allons créer une nouvelle bibliothèque nommée `G20x_Nom_empreintes.pretty` dans laquelle seront stockées les empreintes que vous allez créer.

{% include youtube_video.html youtube_id="En3QR7WStKk" %}

Pour créer une empreinte on a le choix entre :
* partir d'une empreinte existante et la modifier 
* créer l'empreinte de toutes pièces

# Création d'une empreinte à partir d'une empreinte existante

Remarque : si vous avez le message "Measurement Tool not available in legacy toolset" en voulant utiliser l'outil pied à coulisse, il faut aller dans le menu `Préférences` et choisir `Affichage moderne (Accéléré)` (raccourci <kbd>F11</kbd>)

## Exemple de la LED

La vidéo suivante montre l'exemple de la modification de l'empreinte de la LED qui servira de modèle à la modification de l'empreinte des résistances dans la partie suivante.

{% include youtube_video.html youtube_id="AfDIjXtJF6k" %}

## Création de l'empreinte des résistances

Les résistances choisies sont des résistances 1/4 W à couches de carbone dont les dimemsions sont données dans la [documentation constructeur]({% include file_link.html file="Multicomp%20Carbon%20Film%20Fixed%20Resistor%20Axial%20Leaded.pdf" %}). Un extrait de cette documentation est donné dans la figure ci-dessous :


![]({% include img_link.html file="resistor_drawing.png" %})

![]({% include img_link.html file="resistor_dim_table.png" %})

Il s'agit d'une résistance axiale que nous allons monter à l'horizontale. En tapant `resistor tht axial horizontal` on peut afficher les empreintes disponibles qui sont toutes nommées en suivant une convention faisant apparaître : la longueur du corps (L), le diamètre du corps (D) et l'espace entre les pastilles (P : pas ou *pitch*). Etant donnée la longueur du corps (6,8 mm), l'espace entre les pastilles sera choisi autour de 1 cm pour ne pas replier les pattes trop près du corps on peut donc ajouter `P10` au filtre, on identifie l'empreinte la plus proche de celle recherchée :

```
R_Axial_DIN0207_L6.3mm_D2.5mm_P10.16mm_Horizontal
```

La longueur n'est pas exactement celle de notre résistance (erreur de 0,5 mm) mais il n'est pas nécessaire  de la modifier, le critère fondamental dans une empreinte est la distance entre les pastilles. Il faut par contre modifier cette empreinte pour avoir des pastilles dont le diamètre est de 2 mm (le diamètre de perçage est de 0,8 mm - on ne perce pas en dessous à l'IUT car les forêts plus fins sont trop fragiles).

Créez maintenant cette empreinte dans votre librairie.

Remarque : si vous avez le message "Measurement Tool not available in legacy toolset" en voulant utiliser l'outil pied à coulisse, il faut aller dans le menu `Préférences` et choisir `Affichage moderne (Accéléré)` (raccourci <kbd>F11</kbd>)

![]({% include img_link.html file="affichage_moderne.png" %})

# Création de l'empreinte du bornier

## Exemple d'un bornier à vis 3 points

Dans cette vidéo, nous allons voir toutes les étapes de la création d'une nouvelle empreinte : celle d'un bornier à vis à 3 points ([documentation]({% include file_link.html file="Bornier%20KRM.pdf" %})). Cette vidéo est inspirée de la [vidéo d'Eric Peronnin](https://youtu.be/U0zn2dS4Jac) (IUT de Nantes).

{% include youtube_video.html youtube_id="wQZBoFJdPsI" %}


Sommaire de la vidéo (pour un accès direct aux principales étapes) :

1. <a href="https://www.youtube.com/watch?v=wQZBoFJdPsI" target="_blank">Recherche dans les librairies</a>
2. <a href="https://www.youtube.com/watch?v=wQZBoFJdPsI&t=96s" target="_blank">Nommage de la nouvelle empreinte</a>
3. <a href="https://www.youtube.com/watch?v=wQZBoFJdPsI&t=298s" target="_blank">Placement des pastilles (pads)</a>
4. <a href="https://www.youtube.com/watch?v=wQZBoFJdPsI&t=385s" target="_blank">Edition des pastilles</a>
5. <a href="https://www.youtube.com/watch?v=wQZBoFJdPsI&t=610s" target="_blank">Tracé de la sérigraphie (F.SilkS : Front Silkscreen)</a>
6. <a href="https://www.youtube.com/watch?v=wQZBoFJdPsI&t=698s" target="_blank">Mesure des dimensions</a>
7. <a href="https://www.youtube.com/watch?v=wQZBoFJdPsI&t=786s" target="_blank">Sauvegarde en librairie</a>
8. <a href="https://www.youtube.com/watch?v=wQZBoFJdPsI&t=812s" target="_blank">Dessin de l'occupation physique du composant (F.CrtYd)</a>
9. <a href="https://www.youtube.com/watch?v=wQZBoFJdPsI&t=833s" target="_blank">Dessin de la couche de fabrication</a>
10. <a href="https://www.youtube.com/watch?v=wQZBoFJdPsI&t=888s" target="_blank">Affichage/Masquage des couches</a>
11. <a href="https://www.youtube.com/watch?v=wQZBoFJdPsI&t=908s" target="_blank">Propriétés de l'empreinte</a>

## Création de l'empreinte du bornier à vis 2 points

En suivant le modèle de la vidéo précédente, créez l'empreinte du bornier à vis 2 points qui servira pour amener l'alimentation sur la carte. Dans sa version 2 points, le bornier a une longueur de 10 mm, on le nommera `Bornier_1x02_L10mm_W7.5mm_P5mm`. Toutes les dimensions sont données dans la [documentation technique](http://www.farnell.com/datasheets/2047458.pdf).

[Suite...]({{site.baseurl}}/enonces/tp4)