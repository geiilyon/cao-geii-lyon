Tuto_2 :
Créer une bibliothèque d’empreinte
Créer une empreinte physique

Tuto_3 :
Associer une empreinte à un composant
Générer la netlist

Tuto_4   :
Importer la netlis
Dessiner le contour du circuit imprimé
Placer les composant

Tuto_5   :
Spécifier les règles de conception
Utiliser le routeur interactif


Création de la bibliothèque d’empreinte
Affectation des empreintes.
Création des empreintes physiques
Créer Bornier à vis et modifier empreinte (uniquement la taille des pastilles) des résistances. 
Générer la netlist
Placement des composants
Routage.
Plan de masse

# Listes des composants

Attention : les références ci-dessous correspondent au schéma fourni. 

Lors de la saisie du schéma, il faut faire annoter manuellement les composants pour s'assurer d'avoir les mêmes que sur le schéma de référence.


| Reference(s)         | Value             | LibPart                          | Footprint                                                                                               | Référence fabricant                                                                                           |
| -------------------- | ----------------- | -------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| C1, C6, C7, C8       | 1u                | Device:C                         | IUT_footprints:C_Radial_D5.0mm_H11.0mm_P2.00mm                                                          | [MCNP35V105M5X11](https://fr.farnell.com/multicomp/mcnp35v105m5x11/condensateur-1-f-35v-20/dp/1236666)        |
| C2, C4, C5, C9, C10  | 100n              | Device:C                         | IUT_footprints:C_Disc_D4.7mm_W2.5mm_P5.00mm                                                             | [K104K15X7RF53H5](http://www.farnell.com/datasheets/2243519.pdf)                                              |
| C3                   | 47u               | Device:CP_Small                  | IUT_footprints:CP_Radial_D6.3mm_P2.50mm                                                                 | [ECA-1HHG470](http://industrial.panasonic.com/cdbs/www-data/pdf/RDF0000/ABA0000C1215.pdf)                     |
| D1, D2               | LED R             | Device:LED                       | IUT_footprints:LED_D5.0mm                                                                               | [MCL053PD](http://www.farnell.com/datasheets/2861525.pdf)                                                     |
| D3, D4               | LED V             | Device:LED                       | IUT_footprints:LED_D5.0mm                                                                               | [MCL053GD](http://www.farnell.com/datasheets/2861527.pdf)                                                     |
| DS1                  | 162B-CC-BC-3LP    | NOM_symboles:162B-CC-BC-3LP      | IUT_footprints:162B                                                                                     | [162B-CC-BC-3LP](https://cdn.displaytech-us.com/sites/default/files/display-data-sheet/162B%20series-v21.pdf) |
| J1                   | Alimentation      | Connector:Screw_Terminal_01x02   | NOM_footprints:Bornier_2pts_L10mm_W7.5mm_P5mm                                                           | [KRM 02](http://www.farnell.com/datasheets/2047458.pdf)                                                       |
| J2                   | Série (TTL)       | Connector_Generic:Conn_01x06     | IUT_footprints:PinHeader_1x06_P2.54mm_Vertical                                                          | [2211S-06G](http://www.farnell.com/datasheets/1518407.pdf)                                                    |
| J3                   | RS-232            | Connector:DB9_Male_MountingHoles | IUT_footprints:DSUB-9_Male_Horizontal_P2.77x2.84mm_EdgePinOffset7.70mm_Housed_MountingHolesOffset9.12mm | [5504F1-09P-02A-03](http://www.farnell.com/datasheets/1850778.pdf)                                            |
| J4                   | PortA             | Connector_Generic:Conn_01x08     | IUT_footprints:PinHeader_1x08_P2.54mm_Vertical                                                          | [2211S-08G](http://www.farnell.com/datasheets/1518407.pdf)                                                    |
| J5                   | Conn_PIC_ICSP_ICD | Connector:Conn_PIC_ICSP_ICD      | IUT_footprints:PicKit_4_Snap_1x08_P2.54mm_Vertical                                                      | [2211S-06G](http://www.farnell.com/datasheets/1518407.pdf)                                                    |
| R1, R3, R5, R6, R14  | 10k               | Device:R                         | NOM_footprints:R_Axial_DIN0207_L6.3mm_D2.5mm_P10.16mm_Horizontal                                        | [MCF 0.25W 10K](http://www.farnell.com/datasheets/2861447.pdf)                                                |
| R2, R4, R11          | 56k               | Device:R                         | NOM_footprints:R_Axial_DIN0207_L6.3mm_D2.5mm_P10.16mm_Horizontal                                        | [MCF 0.25W 56K](http://www.farnell.com/datasheets/2861447.pdf)                                                |
| R7, R8, R9, R10, R13 | 270               | Device:R                         | NOM_footprints:R_Axial_DIN0207_L6.3mm_D2.5mm_P10.16mm_Horizontal                                        | [MCF 0.25W 270R](http://www.farnell.com/datasheets/2861447.pdf)                                               |
| R12                  | 6.8k              | Device:R                         | NOM_footprints:R_Axial_DIN0207_L6.3mm_D2.5mm_P10.16mm_Horizontal                                        | [MCF 0.25W 6K8](http://www.farnell.com/datasheets/2861447.pdf)                                                |
| RV1, RV2             | 10k               | Device:R_POT                     | IUT_footprints:Potentiometer_Bourns_3306F_Vertical                                                      | [3306F-1-103](http://www.farnell.com/datasheets/1815113.pdf)                                                  |
| SW1, SW2             | B3F-1000          | Switch:SW_Push                   | IUT_footprints:SW_TH_Tactile_Omron_B3F-10xx                                                             | [B3F-1000](https://4donline.ihs.com/images/VipMasterIC/IC/OMRN/OMRN-S-A0001309768/OMRN-S-A0001309768-1.pdf)   |
| SW3                  | SW_DIP_x02        | Switch:SW_DIP_x02                | IUT_footprints:SW_DIP_SPSTx02_Slide_7.5x7.01mm_W7.62mm_P2.54mm_LowProfile                               | [ADE02A04](https://docs.rs-online.com/c98b/0900766b810b550f.pdf)                                              |
| U1                   | MAX232            | Interface_UART:MAX232            | Package_DIP:DIP-16_W7.62mm_Socket_LongPads                                                              | [MAX232N](http://www.ti.com/lit/ds/symlink/max232.pdf)                                                        |
| U2                   | PIC16F1788-xSP    | IUT_symboles:PIC16F1788-xSP      | Package_DIP:DIP-28_W7.62mm_Socket_LongPads                                                              | [PIC16F1788-I/SP](http://ww1.microchip.com/downloads/en/DeviceDoc/40001675C.pdf)                              |

