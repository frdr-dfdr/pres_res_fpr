# Digital Preservation Services File Format Strategy
Last updated: 2026-02-04

Understanding file formats is integral to implementing strategies that aid in the continued access and reuse of research data. This page contains information about Digital Preservation Services' file format work. This page will be updated as we develop our strategy. 

For additional information about Digital Preservation Services at the Digital Research Alliance of Canada, please visit the [Digital Preservation Services](https://github.com/frdr-dfdr/pres_res_dpservices) page.

## Strategy
While repositories may provide a list of recommended formats we recognize that not all research projects can use open or recommended file formats. Therefore, all file formats are accepted. Different preservation levels are implemented to determine digital preservation capabilities for the various file formats received. 

### Preservation Levels

| Action | Basic level | Watch Level | Full Level|
| :----------- | :-----------: | :-----------: | :-----------: |
| Regular fixity checks | ✔️ | ✔️ | ✔️ |
| Virus scanning  | ✔️ | ✔️ | ✔️ |
| Geo-redundant storage | ✔️ | ✔️ | ✔️ |
| Storage refresh/replace | ✔️ | ✔️ | ✔️ |
| File format identification |  | ✔️ | ✔️ |
| Generation of preservation metadata |  | ✔️ | ✔️ |
| Watch format for ability to preserve  |  | ✔️ | ✔️ |
| Monitor format over time |  | ✔️ | ✔️ |
| Perform normalization |  | | ✔️ |
| Long-term storage in preservation format  |  | | ✔️ |

- Adapted from [Simon Fraser University, Archives and Records Management, Format Policy Registry](https://github.com/sfu-archives/format-policy-registry)
  
#### Basic Level
Basic level of preservation, the bit-stream (1s and 0s) of the file are preserved. No file migration or normalization occurs at this level. Basic level includes:
- Fixity checks
- Store two complete copies of the digital files in different geographic locations
- Virus checking

The basic level of preservation cannot ensure that the file can be rendered in the future.

#### Watch Level 
Watch level includes files that are proprietary but are prevalent in the industry that the likelihood of obsolescence is unlikely. The watch level includes all elements of basic level with the additional preservation activities:
- File identification, when possible
- Monitoring of the formats
- Generation of metadata for preservation and access

#### Full Level 
Full level includes files that the repository has confidence will be available in the long term because they are commonly used, the formats are open and documented, or the formats can be normalized to a preservation friendly format. Full level preservation includes all actions undertaken at the basic and watch level with the additional preservation activities:
- Normalization of file formats to preservation friendly formats
- File format identification
- File format validation

## Digital Preservation Activities
### Fixity Checking
Fixity determines whether or not a digital file has been altered or changed. Establishing fixity is a method for ensuring the integrity of files.

### File Format Identification
File format identification involves determining the version and the specific type of a file. [Siegfried](https://github.com/richardlehane/siegfried) is used for file format identification work. [DROID](https://www.nationalarchives.gov.uk/information-management/manage-information/preserving-digital-records/droid/) is used for testing file format signatures.

### File Format Validation
File format validation involves checking if a file format conforms to its file format specification. 

### File Format Characterization
File format characterization involves extracting metadata from the file. The metadata may include information such as aspect ratio or compression level.

### Normalization
An activity that results in digital objects of a particular type converted to a single chosen file format that is non-proprietary and designated preservation friendly. Example jpg, png, gif are normalized to tiff.

### Original Files
In all instances, digital preservation services keeps the original files as it holds information that the derivatives will not contain.

## Storage
Different storage options are employed to achieve digital preservation activities. These include:
- Level 1: Two complete copies of the files in the dataset stored in two different geographic locations. 
- Level 2: Three complete copies of files in the dataset with one copy on a different storage media type. 
- Level 3: Three complete copies of the files in the dataset, one copy stored in a different location with a different disaster threat level.

---
## Acknowledgements
The Strategy and the Format Policy Registry (FPR) draws on the excellent work being undertaking internationally by libraries, archives, galleries, museums, and repositories including but not limited to

- [Archives and Records Management, Simon Fraser University](https://www.sfu.ca/archives.html)
- [DANS (Data Archiving and Records Service)](https://dans.knaw.nl/en/)
- [Library and Archives Canada](https://www.canada.ca/en/library-archives/services/government/information-disposition/management/guidelines/file-formats-transfer.html)
- [Library of Congress, Sustainability of Digital Formats](https://www.loc.gov/preservation/digital/formats/)
- [National Archives and Records Administration (NARA), Digital Preservation](https://github.com/usnationalarchives/digital-preservation)

Thank you for all your work!

---
# Stratégie relative aux formats de fichiers des Services de préservation numérique
Dernière mise à jour : 2026-02-04

La compréhension des formats de fichiers est essentielle à la mise en œuvre de stratégies favorisant l’accès continu aux données de recherche et leur réutilisation. Cette page présente de l’information sur les travaux des Services de préservation numérique relatifs aux formats de fichiers et sera mise à jour et enrichie au fur et à mesure de l’élaboration de la stratégie.

Pour de plus amples renseignements concernant les [Services de préservation numérique](https://github.com/frdr-dfdr/pres_res_dpservices?tab=readme-ov-file#services-de-pr%C3%A9servation-num%C3%A9rique) de l’Alliance de recherche numérique du Canada, veuillez consulter la page qui leur est consacrée.

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