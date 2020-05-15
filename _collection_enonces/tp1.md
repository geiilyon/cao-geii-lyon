---
title: Introduction
layout: page
excerpt: Création, configuration du projet et installation des bibliothèques (commencer ici)
---

# Installation de Kicad

Télécharger la version de Kicad correspondant à votre système sur le [site officiel](https://www.kicad-pcb.org/download/) et suivre les consignes du [fichier PDF lié]({% include file_link.html file="Installation_KICAD.pdf" %}).


# Configuration du projet

1. Créer un dossier `CAO_IUT` dans votre dossier `Documents`
1. Lancer le logiciel Kicad et créer un nouveau projet que vous nommerez en respectant le format suivant : `G20x_Nom_TP_CAO` en remplaçant le x par votre numéro de groupe et Nom par votre nom de famille.

    Le dossier `CAO_IUT` doit maintenant contenir un sous-dossier `G20x_Nom_TP_CAO` qui contient à son tour 3 fichiers `G20x_Nom_TP_CAO.kicad_pcb`, `G20x_Nom_TP_CAO.pro` et `G20x_Nom_TP_CAO.sch`. 
    
    L'image ci-dessous montre la vue du projet depuis l'application Kicad et le contenu du dossier vu depuis l'explorateur de fichiers de windows (il peut être utile de rafraichir l'affichage dans Kicad en cliquant sur les flèches ![]({% include img_link.html file="refresh_arrows.png" %}) :
    
    ![]({% include img_link.html file="ExplorerKicadWindowsAfterProjectCreation.png" %})

3. Télécharger [l'archive contenant les librairies]({% include file_link.html file="librairies.zip" %})
4. Décompresser cette archive dans le dossier `G20x_Nom_TP_CAO`.
 

{% include youtube_video.html youtube_id="3XBW52TihB0" %}

L'arborescence des fichiers et dossiers doit maintenant se présenter de la manière suivante :

![]({% include img_link.html file="ExplorerKicadWindowsAfterLibrariesUnarchiving.png" %})

## Rôle des principaux fichiers d'un projet kicad

| File                      | Description                                                                                                                    |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| G20x_Nom_TP_CAO.pro       | Fichier du projet (contient en particulier les chemins des librairies)                                                         |
| G20x_Nom_TP_CAO.sch       | Schéma principal                                                                                                               |
| G20x_Nom_TP_CAO.kicad_pcb | Tracé du circuit imprimé                                                                                                       |
| G20x_Nom_TP_CAO.net       | Netlist                                                                                                                        |
| G20x_Nom_TP_CAO-cache.lib | Fichier automatiquement créé et utilisé par l'éditeur de schéma contenant une copie des composants utilisés dans le schéma     |
| xyz.kicad_mod             | Fichier contenant l'empreinte d'un composant                                                                                   |
| une_librairie.lib         | Fichier librairie de symboles (composants de schémas), contenant la représentation graphique du composant (forme, pattes, ...) |
| une_librairie.dcm         | Fichier de documentation de la librairie de symboles, contenant les commentaires, mots clés, liens vers les datasheets         |

Un même projet peut contenir plusieurs librairies d'empreintes et de symboles, plusieurs schémas, ...

# Ajout de la bibliothèque GEII de symboles au projet

Les bibliothèques précédemment téléchargées et décompressées doivent être ajoutées au projet.

Dans Kicad on peut configurer des librairies globales (accessibles pour tous les projets) et des librairies spécifiques au projet.

Nous allons ajouter ici la librairie GEII spécifique au projet en cours.

{% include youtube_video.html youtube_id="U7eUwGet6XM" %}

Lors du premier lancement de Kicad, une boîte de dialogue s'ouvre pour demander quelles librairies globales copier. Il faut choisir l'option recommandée :

![]({% include img_link.html file="Copie_table_globale_premier_lancement.png" %})

# Création d'une bibliothèque de symboles

Créer une bibliothèque de symboles de composants nommée G20x_Nom_symboles en suivant la procédure présentée dans la vidéo ci-dessous,

{% include youtube_video.html youtube_id="_1GroStnVkE" %}


[Suite...]({{site.baseurl}}/enonces/tp2)