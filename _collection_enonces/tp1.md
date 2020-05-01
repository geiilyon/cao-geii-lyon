---
title: Introduction
layout: page
excerpt: Installation de Kicad. Configuration du projet
---

# Installation de Kicad

Télécharger la version de Kicad correspondant à votre système sur le [site officiel](https://www.kicad-pcb.org/download/) et suivre les consignes du [fichier PDF lié]({% include file_link.html file="Installation_KICAD.pdf" %}).


# Configuration du projet

1. Créer un dossier `CAO_IUT` dans votre dossier `Documents`
1. Lancer le logiciel Kicad et créer un nouveau projet que vous nommerez en respectant le format suivant : `G20x_Nom_TP_CAO` en remplçaçant Nom par votre nom de famille.

    Le dossier `CAO_IUT` doit maintenant contenir un sous-dossier `G20x_Nom_TP_CAO` qui contient à son tour 3 fichiers `G20x_Nom_TP_CAO.kicad_pcb`, `G20x_Nom_TP_CAO.pro` et `G20x_Nom_TP_CAO.sch`
    
    ```
    .
    └── Documents
        └── G20x_Nom_TP_CAO
            ├── G20x_Nom_TP_CAO.kicad_pcb
            ├── G20x_Nom_TP_CAO.pro
            └── G20x_Nom_TP_CAO.sch
    ```

3. Télécharger l'archive contenant les librairies suivante : [librairies]({% include file_link.html file="librairies.zip" %})
4. Décompresser cette archive dans le dossier `G20x_Nom_TP_CAO`.
 

{% include local_video.html file_name="extraction_librairies.mp4" %}


L'arborescence des fichiers et dossiers doit maintenant se présenter de la manière suivante :

```
    .
    └── Documents
        └── G20x_Nom_TP_CAO
            ├── G20x_Nom_TP_CAO.kicad_pcb
            ├── G20x_Nom_TP_CAO.pro
            ├── G20x_Nom_TP_CAO.sch
            ├── IUT_empreintes.pretty
            │   ├── 162B.kicad_mod
            │   ├── C_Disc_D4.7mm_W2.5mm_P5.00mm.kicad_mod
            │   ├── C_Radial_D5.0mm_H11.0mm_P2.00mm.kicad_mod
            │   ├── CP_Radial_D6.3mm_P2.50mm.kicad_mod
            │   ├── DSUB-9_Male_Horizontal_P2.77x2.84mm_EdgePinOffset7.70mm_Housed_MountingHolesOffset9.12mm.kicad_mod
            │   ├── LED_D5.0mm.kicad_mod
            │   ├── PicKit_4_Snap_1x08_P2.54mm_Vertical.kicad_mod
            │   ├── PinHeader_1x06_P2.54mm_Vertical.kicad_mod
            │   ├── PinHeader_1x08_P2.54mm_Vertical.kicad_mod
            │   ├── Potentiometer_Bourns_3306F_Vertical.kicad_mod
            │   ├── Potentiometer_Bourns_3306P_Vertical.kicad_mod
            │   ├── SW_DIP_SPSTx02_Slide_7.5x7.01mm_W7.62mm_P2.54mm_LowProfile.kicad_mod
            │   └── SW_TH_Tactile_Omron_B3F-10xx.kicad_mod
            └── librairies_symboles
                ├── IUT_CAO_LIB_SYMBOLES.lib
                └── IUT_CAO_LIB_SYMBOLES.dcm
```

## Présentation succincte du rôle des principaux fichiers qui constituent un project kicad :

| File                      | Description                                                                                                                    |
| ------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| G20x_Nom_TP_CAO.pro       | Fichier du projet (contient en particulier les chemins des librairies)                                                         |
| G20x_Nom_TP_CAO.sch       | Schéma principal                                                                                                               |
| G20x_Nom_TP_CAO.kicad_pcb | Tracé du circuit imprimé                                                                                                       |
| G20x_Nom_TP_CAO.net       | Netlist                                                                                                                        |
| G20x_Nom_TP_CAO-cache.lib | Fichier automatiquement créé et utilisé par l'éditeur de schéma contenant une copie des composants utilisés dans le schéma     |
| xyz.kicad_mod             | Fichier contenant l'empreinte d'un composant                                                                                   |
| une_librairie.lib         | Fichier librairie de symboles (composants de schémas), contenant la représentation graphique du composant (forme, pattes, ...) |
| une_librairie.dcm         | Fichier de documentation de la librairie de symboles, contenant les commentaires, mots clés, liens vers la datasheet           |

Un même projet peut contenir plusieurs librairies d'empreintes et de symboles, plusieurs schémas, ...

# Ajout de la bibliothèque GEII de symboles au projet

Les bibliothèques précédemment téléchargées et décompressées doivent être ajoutées au projet. 

Dans Kicad on peut configurer des librairies globales

{% include local_video.html file_name="Ajout librairie symboles IUT.mp4" %}

# Création d'une bibliothèque de composants


Tuto_1 :
Saisie du schéma
Création de la bibliothèque (schématique)
Création/modification d’un composant 
162B à partir du 1602
Eventuellement le PIC16F1788 (à partir du PIC16F886 avec gestion des alias)
Annotation des composants (Reprendre la numérotation des composants pour qu’elle corresponde à notre numérotation).
Contrôle des erreurs électriques.


[Suite...]({{site.baseurl}}/enonces/tp2)