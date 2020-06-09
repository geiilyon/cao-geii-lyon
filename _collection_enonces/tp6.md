---
title: Finalisation de la carte
layout: page
excerpt: Plan de masse, ajout du nom, sérigraphie, ...
---

La vidéo suivante présente les étapes de finalisation qu'il faudra appliquer à votre carte :

1. <a href="https://www.youtube.com/watch?v=MVSU_0qUOys" target="_blank">Suppression des références des trous de fixation</a>
2. <a href="https://www.youtube.com/watch?v=MVSU_0qUOys&t=132s" target="_blank">Ajout du plan de masse</a>
3. <a href="https://www.youtube.com/watch?v=MVSU_0qUOys&t=292s" target="_blank">Remplissage des zones vides avec du cuivre (pour accélérer la fabrication par gravure laser)</a>
4. <a href="https://www.youtube.com/watch?v=MVSU_0qUOys&t=446s" target="_blank">Ajout du nom sur la couche de cuivre</a>
5. <a href="https://www.youtube.com/watch?v=MVSU_0qUOys&t=558s" target="_blank">Déplacement et rotation des éléments de la couche de sérigraphie</a>
6. <a href="https://www.youtube.com/watch?v=MVSU_0qUOys&t=664s" target="_blank">Ajout de texte sur la couche de Sérigraphie</a>

{% include youtube_video.html youtube_id="MVSU_0qUOys" %}

Le texte qui devra figurer sur la couche de sérigraphie et sur la couche B.Cu devra comporter votre nom et votre numéro de groupe. Ex : `ROBIN - G201`.

Ajouter également le texte `+` et `GND` à côté des pattes du bornier à vis.

Une fois votre routage terminé, il faut rafraîchir le plan de masse en appuyant sur la touche <kbd>B</kbd> (ou bien en passant par le menu *Editer->Remplissage Toutes Zones*) et relancer une vérification des règles de conception DRC ![]({% include img_link.html file="debug_coccinelle.png" %}).

Il reste 6 erreurs résiduelles qui sont :

* les 2 que l'on avait déjà à l'étape précédente : `Zones d'occupation d'empreintes chevauchantes` pour le connecteur du PICKit et le LCD qui chevauchent les trous de fixation.
* 4 erreurs (au 4 coins de carte)  `Zone de cuivre  à l'intérieur d'une zone de cuivre` qui sont liées à l'imbrication des 2 plans utilisés ici pour diminuer la quantité de cuivre à enlever.

Vérifier qu'il ne reste pas de connexions non routées.

Terminer par une inspection visuelle de la carte pour vérifier l'absence de court-circuit, la présence des freins thermiques dans le plan de masse.

Archiver le projet et le remettre à votre enseignant.