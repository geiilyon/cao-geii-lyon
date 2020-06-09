---
title: Placement et routage
layout: page
excerpt: Utilisation de l'outil Pcbnew
---

# Génération et chargement de la netliste

L'export de la netliste ![]({% include img_link.html file="icone_netlist.png" %}) depuis Eeschema et son import depuis Pcbnew sont décrits dans la vidéo suivante :

{% include youtube_video.html youtube_id="oWO_kHt8-X8" %}

Remarque : il est également possible d'utiliser l'outil *mise à jour du PCB à partir du schéma* ![]({% include img_link.html file="icone_maj_pcb_depuis_schema.png" %}) de Pcbnew pour importer les composants du schéma ou effectuer une mise à jour suite à une modification du schéma.

# Dessin du contour de la carte

Le tracé du contour se fait sur la couche nommée *Edge.Cuts* qui est utilisée pour la découpe  lors de la fabrication du circuit imprimé.

La carte à réaliser sera de format rectangulaire (12x8 cm). La vidéo suivante présente la marche à suivre pour effectuer le tracé du circuit imprimé et l'ajout de 4 trous de fixation dans les coins de la carte :

{% include youtube_video.html youtube_id="qSiSEWnJr-E" %}

# Spécification des règles de routage

La vidéo ci-dessous présente l'utilisation du menu *Options du CI* ![]({% include img_link.html file="icone_options_ci.png" %}) permettant de spécifier les différentes règles de routage :

{% include youtube_video.html youtube_id="cfshMq2tAx0" %}

Sommaire de la vidéo (pour un accès direct) :

* <a href="https://www.youtube.com/watch?v=cfshMq2tAx0&t=31s" target="_blank">Présentations des différentes couches (layers)</a>
* <a href="https://www.youtube.com/watch?v=cfshMq2tAx0&t=213s" target="_blank">Configuration des règles de conception</a>

Les règles de routage utilisées dans le cours sont rappelées ci-dessous :

![]({% include img_link.html file="regles_conception.png" %})

![]({% include img_link.html file="classes_equipots.png" %})

# Placement des composants et routage

Les deux vidéos suivantes faites par Eric Peronnin (IUT de Nantes) permettent d'illustrer l'utilisation des différents outils de Pcbnew. Elles servent à illustrer le fonctionnement du logiciel afin de vous permettre de router votre carte par la suite **en respectant les contraintes de placement données plus loin**. Faites particulièrement attention à l'utilisation des grilles pour placer et aligner précisément les composants.

La première vidéo présente :

* <a href="https://www.youtube.com/watch?v=udtxzxKdEQ8" target="_blank">l'édition du cartouche (côté Pcbnew)</a>
* <a href="https://www.youtube.com/watch?v=udtxzxKdEQ8&t=91s" target="_blank">l'importation de la netliste</a> (déjà vue dans la vidéo précédente)
* <a href="https://www.youtube.com/watch?v=udtxzxKdEQ8&t=153s" target="_blank">le tracé du contour de la carte</a> (déjà vu dans la vidéo précédente)
* <a href="https://www.youtube.com/watch?v=udtxzxKdEQ8&t=282s" target="_blank">le tracé des dimensions du contour</a> (déjà vu dans la vidéo précédente)
* <a href="https://www.youtube.com/watch?v=udtxzxKdEQ8&t=383s" target="_blank">le placement des composants</a>

{% include youtube_video.html youtube_id="udtxzxKdEQ8" %}

Et enfin, cette dernière vidéo présente les outils de routage à partir de la 4ème minute (le début de la vidéo reprend la spécification des règles de routage **que nous avons déjà faite et que nous avons réglée à des valeurs légèrement différentes**) :

{% include youtube_video.html youtube_id="-PCrFnJr3mg" %}

En se servant de ces vidéos, placer et router les composants de la carte PIC en respectant la disposition suivante et en tenant compte des contraintes ci-dessous :

![]({% include img_link.html file="PlacementComposants.png" %})

On veillera également à respecter les contraintes suivantes (l'origine des coordonnées relatives (dx, dy) à (0, 0) est prise au coin supérieur droit de la carte) :

* La pastille 1 de l'afficheur LCD sera positionnée en (dx, dy) = (-35, 10)
* La pastille 1 du connecteur d'alimentation J1 sera positionnée en (dx, dy) = (-4, 25)
* Le connecteur DB9 doit être orienté vers l'extérieur de la carte avec la partie connecteur qui déborde de la carte (pastille 1 en dx = -109 et dy libre). La partie de l'empreinte dessinée sur la couche sérigraphie ne doit pas déborder du bord de la carte, c'est la raison pour laquelle le connecteur est dessiné sur la couche mécanique.

![]({% include img_link.html file="DB9_Orientation.png" %})

* Les condensateurs de découplage doivent être placés au plus près des composants à découpler
* Straps en ligne droite (horizontaux ou verticaux) : pas de virage, pas de diagonale sur la couche F.Cu. Un strap est matérialisé par une piste sur la couche F.Cu (rouge) entre 2 vias (on ne peut pas partir de la patte d'un composant car cela supposerait de mettre la patte du composant et le strap dans le même trou)
* Pas de straps sous les composants
* Pas de straps à travers les composants
Remarques : 
* le connecteur J5 (PICKit) définit une grande zone d'occupation mécanique (Ctyd) mais vu la forme du connecteur il pourra chevaucher les trous de fixations
  
  ![]({% include img_link.html file="pickit.png" %})

* le LCD sera également surélevé et peut lui aussi chevaucher un trou de fixation

# Vérification des erreurs de design (DRC : Design Rule Check)

Cliquer sur l'icône qui représente une coccinelle ![]({% include img_link.html file="debug_coccinelle.png" %}) puis choisir *Exécuter DRC*.

A ce stade les seules erreurs acceptables sont les chevauchements des zones d'occupation du LCD avec les trous de fixation et du connecteur J5 (PICKit) avec le trou de fixation :

```
Zones d'occupation d'empreintes chevauchantes
@(yyy.yyy mm, zzz.zzz mm): Empreinte <pas de référence> sur F.Cu
@(yyy.yyy mm, zzz.zzz mm): Empreinte J5 sur F.Cu
```

[Suite...]({{site.baseurl}}/enonces/tp6)