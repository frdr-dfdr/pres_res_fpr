# Stratégie relative aux formats de fichiers des Services de préservation numérique

La compréhension des formats de fichiers est essentielle à la mise en œuvre de stratégies favorisant l’accès continu aux données de recherche et leur réutilisation. Cette page présente de l’information sur les travaux des Services de préservation numérique relatifs aux formats de fichiers et sera mise à jour et enrichie au fur et à mesure de l’élaboration de la stratégie.

Pour de plus amples renseignements concernant les Services de préservation numérique de l’Alliance de recherche numérique du Canada, veuillez consulter [la page](https://github.com/frdr-dfdr/pres_res_dpservices?tab=readme-ov-file#services-de-pr%C3%A9servation-num%C3%A9rique) qui leur est consacrée.

## Stratégie
Bien que des formats recommandés soient souvent précisés pour le dépôt et la préservation numérique, il est reconnu que tous les projets de recherche ne peuvent pas utiliser des formats de fichiers ouverts. Les Services de préservation numérique ont élaboré différents niveaux de préservation afin de déterminer les capacités de préservation applicables aux divers formats de fichiers utilisés par les chercheuses et chercheurs.

### Niveaux de préservation
| Action | Niveau de base | Niveau de surveillance | Niveau complet |
| :----------- | :-----------: | :-----------: | :-----------: |
| Vérifications régulières de l’intégrité (fixité) | ✔️ | ✔️ | ✔️ |
| Analyse antivirus | ✔️ | ✔️ | ✔️ |
| Stockage géoredondant | ✔️ | ✔️ | ✔️ |
| Actualisation ou remplacement du stockage | ✔️ | ✔️ | ✔️ |
| Identification des formats de fichiers| | ✔️ | ✔️ |
| Génération de métadonnées de préservation |  | ✔️ | ✔️ |
| Surveillance des formats quant à leur aptitude à la préservation  |  | ✔️ | ✔️ |
| Surveillance de l’évolution des formats dans le temps |  | | ✔️ |
| Normalisation |  | | ✔️ |
| Stockage à long terme dans un format de préservation|  |  | ✔️ |

- Adapté de [l’Université Simon Fraser, Archives et gestion des documents, Registre des politiques relatives aux formats](https://github.com/sfu-archives/format-policy-registry).

#### Niveau de base
Le niveau de base de la préservation comprend la copie du flux binaire (les 1 et les 0). Aucune migration ni normalisation des fichiers n’est effectuée à ce niveau. Le niveau de base comprend :
- Des vérifications de l’intégrité
- Le stockage de deux copies complètes des fichiers numériques dans des emplacements géographiques distincts
- Des analyses antivirus

Le niveau de base de la préservation ne permet pas de garantir que les fichiers pourront être utilisés à l’avenir.

#### Niveau de surveillance
Le niveau de surveillance comprend des fichiers propriétaires largement utilisés dans leur secteur, pour lesquels le risque d’obsolescence est jugé faible. Ce niveau comprend tous les éléments du niveau de base, ainsi que les activités de préservation supplémentaires suivantes :
- Suivi des formats
- Production de métadonnées à des fins de préservation 

#### Niveau complet
Le niveau complet comprend des fichiers dont le dépôt est jugé durable à long terme, car ils sont couramment utilisés, reposent sur des formats ouverts et documentés, ou peuvent être normalisés vers un format propice à la préservation. La préservation de niveau complet comprend toutes les actions des niveaux de base et de surveillance, ainsi que les activités supplémentaires suivantes :
- La normalisation des formats de fichiers vers des formats adaptés à la préservation
- L’identification des formats de fichiers
- La validation des formats de fichiers

## Activités de préservation numérique
### Vérification de l’intégrité (fixité)
La fixité permet de déterminer si un fichier numérique a été modifié ou altéré. La fixité constitue un mécanisme permettant d’établir si l’intégrité d’un fichier numérique a été compromise.

### Identification des formats de fichiers
L’identification des formats de fichiers consiste à reconnaître un fichier à partir de son extension ou de sa signature interne et, le cas échéant, à déterminer la version du format concerné. 

### Validation des formats de fichiers
La validation des formats de fichiers consiste à vérifier qu’un fichier est conforme aux spécifications de son format.

### Caractérisation des formats de fichiers
La caractérisation des formats de fichiers consiste à extraire des métadonnées à partir du fichier. Ces métadonnées peuvent comprendre, entre autres, des informations telles que le rapport hauteur/largeur ou le niveau de compression.

### Normalisation
La normalisation est une activité qui consiste à convertir des objets numériques d’un type donné vers un format de fichier unique, non propriétaire et reconnu comme adapté à la préservation. Par exemple, les formats jpg, png et gif peuvent être normalisés vers le format tiff.

### Fichiers originaux
Dans tous les cas, les Services de préservation numérique conservent les fichiers originaux, ceux-ci renfermant des informations absentes des fichiers dérivés.

### Stockage
Différentes options de stockage sont utilisées pour soutenir les activités de préservation numérique, notamment :
- Niveau 1— Deux copies complètes des fichiers de l’ensemble de données, stockées dans deux emplacements géographiques distincts.
- Niveau 2 — Trois copies complètes des fichiers de l’ensemble de données, dont une stockée sur un type de support différent.
- Niveau 3 — Trois copies complètes des fichiers des jeux de données, dont une stockée dans un emplacement différent présentant un niveau de risque de sinistre distinct.

---
## Remerciements
La stratégie relative aux formats de fichiers et la politique sur les formats de fichiers (FPR) s’appuient sur l’excellent travail mené à l’échelle internationale par des bibliothèques, des archives, des galeries, des musées et des dépôts, notamment, mais sans s’y limiter :
- [Archives et gestion des documents, Université Simon Fraser](https://www.sfu.ca/archives.html)
- [DANS (Data Archiving and Records Service)](https://dans.knaw.nl/en/)
- [Bibliothèque et Archives Canada](https://www.canada.ca/fr/bibliotheque-archives/services/gouvernement/information-disposition/gestion/lignes-directrices/formats-ficher-transfert.html)
- [Bibliothèque du Congrès des États-Unis, Sustainability of Digital Formats](https://www.loc.gov/preservation/digital/formats/)
- [National Archives and Records Administration (NARA), Digital Preservation](https://github.com/usnationalarchives/digital-preservation)

Merci pour tout votre travail !


