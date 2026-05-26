# Matrice des risques

## Objectif

La matrice des risques liés aux formats décrit les formats présents dans le DFDR et leur attribue un niveau de risque calculé en répondant à une série de questions pondérées. Cette matrice s'inspire largement de la matrice des risques liés aux formats de fichiers de la NARA.

## Niveaux de risque

Les niveaux de risque sont classés en trois catégories :

| Catégorie | Description |
| :---- | :---- |
| Faible 0 % - 25 % | Les fichiers sont bien pris en charge, largement utilisés et disposent de spécifications ouvertes et stables. |
| Modéré 26 % \- 50 % | Les fichiers posent certains défis, mais les risques sont gérables. |
| Élevé 51 % \- 100 % | Les fichiers posent des défis importants en matière d'accès et de réutilisation à long terme. Les facteurs incluent le manque de documentation, le caractère propriétaire ou des dépendances obsolètes. | 

### Pondération

Le système de pondération utilisé pour l'analyse des risques est le suivant :

* Oui = 1  
* Non = 0  
* N/A = non pris en compte dans le calcul

Les domaines suivants se voient attribuer un coefficient de pondération en fonction du risque associé à une réponse négative.

| Catégorie            | Coefficient multiplicateur | Total des points possibles\*                              |
| :------------------- | :------------------------- | :-------------------------------------------------------- |
| Divulgation          | Critique \= 3              | 12                                                        |
| Adoption             | Élevée \= 2                | 6                                                         |
| Transparence         | Standard \= 1              | 4 \*Ajouter 3 au total maximal pour les formats binaires. |
| Auto-documentation   | Standard \= 1              | 2                                                         |
| Dépendances externes | Standard \= 1              | 5                                                         |
| Incidence des brevets | Standard \= 1              | 2                                                         |
| Mécanismes de protection technique                 | Élevé \= 2                 | 4                                                         |

\*Le total des points possibles peut varier si un élément de risque n'est pas applicable

### Calcul

Note finale de préservation (%) = (somme des points pondérés / total des points pondérés maximaux possibles) × 100

Note finale de risque = 100 % – Note finale de préservation

Une pénalité de 3 points est ajoutée à la note maximale globale si le format est binaire.

## Ressources

* [Sustainability Factors](https://www.loc.gov/preservation/digital/formats/sustain/sustain.shtml) (LoC)	  
* [Danish National Archives \- Concept Model](https://github.com/the-danish-national-archives/concept-model/tree/main/P2%20Format%20Assessment)   
* [https://github.com/usnationalarchives/digital-preservation/tree/full/Digital\_Preservation\_Risk\_Matrix](https://github.com/usnationalarchives/digital-preservation/tree/master/Digital_Preservation_Risk_Matrix)	  
* [https://harvardwiki.atlassian.net/wiki/spaces/digitalpreservation/pages/48136762/Assessment+Tool](https://harvardwiki.atlassian.net/wiki/spaces/digitalpreservation/pages/48136762/Assessment+Tools)

## Éléments de la matrice et questions

### Divulgation

La notion de « divulgation » désigne le degré auquel une spécification complète du format existe et est accessible. Les spécifications ayant fait l'objet d'une évaluation par des experts externes sont préférables.

| Question | Description |
| :---- | :---- |
| Le format est-il ouvert ? | Indiquez dans quelle mesure le format de fichier est ouvert. Par exemple, le format dispose-t-il d’une licence ouverte ou est-il propriétaire avec une licence restreinte détenue par une entreprise ou une personne ? Les licences restreintes peuvent poser des défis en matière de préservation, notamment en raison de l’obsolescence et de problèmes de compatibilité ascendante.|
| Le format dispose-t-il d’une spécification publiée ? | Indiquez si le format possède une spécification publiée accessible sans frais. |
| Le cas échéant, la spécification est-elle publiée et approuvée par un organisme de normalisation ? | es spécifications approuvées et publiées par un organisme de normalisation reconnu à l’échelle internationale ont fait l’objet d’un processus contrôlé d’élaboration et de publication et disposent généralement d’un mécanisme relativement stable de maintenance.|
| La spécification a-t-elle été mise à jour au cours des cinq dernières années ? | À mesure que les formats vieillissent, le risque s’accroît, ceux-ci pouvant être supplantés par des formats plus récents et bénéficier d’un soutien logiciel et outillé de plus en plus limité. |
| **Multiplicateur x 3** |  |

### Adoption

Adoption refers to the level in which a format is in use by the community, primary creators and disseminators. The more widely used the format the less likely it will disappear. Tools to mitigate obsolescence such as emulation and migration are more likely to be in place. If the format has been assessed as preferred or acceptable for long-term preservation at other repositories or institutions engaged with long-term preservation work, this also provides evidence of adoption. 

| Question | Description |
| :---- | :---- |
| Le format est-il utilisé à des fins de préservation par la communauté ? | Les formats largement utilisés par les dépôts et reconnus comme formats de préservation privilégiés sont généralement plus stables à long terme.|
| Is the format prevalent within the community/research field? | The more widely used a file format is used in the research field or for research data in general the more likely the file will remain in existence in the long-term. |
| Is the file format actively maintained by the community? | File formats that are maintained by a community rather than one or two individuals are more likely to remain available in the long-term. |
| **Multiplier x 2**|  |

### Transparency

Transparency refers to a format that can be analyzed using basic tools including text-only editors. Transparency is enhanced if metadata is embedded for non-text content in a UNICODE using UTF-8 encoding. Source code is more transparent than compiled code. 

Encryption is incompatible with transparency.

Compression inhibits transparency. If a repository must take in material that is compressed, compression algorithms that are common and widely used are preferred. Lossless would be preferred to lossy compression

| Question | Description |
| :---- | :---- |
| Is the format character-based? | Character-based file formats are human readable, platform-independent and based in a character encoding (ASCII, UTF-8, etc.) |
| Can the file be identified by elements other than the extension?  | File formats that have an internal signature increase the ability of the file to be identified. |
| Is the format uncompressed? | Compressed file formats are used to optimize space and transmission but some compression methods result in permanently removing data from the file. The most common compression methods are known as lossy and lossless. |
| **If yes,** does the format use a compression other than lossy?  | Lossy compression permanently removes data from files. This causes degradation of the data in comparison from its original.|
| **Multiplier x 1** | 

### Self-Documentation

Self-Documentation refers to formats with metadata stored with the digital object that is used to render the digital object. These formats are easier to sustain over time. The ability of the format to hold administrative and technical metadata is an advantage for preservation.

| Question | Description |
| :---- | :---- |
| Does the format natively include metadata that documents the file and the technical environment used to create (and/or modify) it? | Formats that natively include technical metadata about their creation will likely be easier to sustain and provide access to over time. |
| Does the format support adding embedded metadata through manual or automated processes? | Formats that natively support adding embedded descriptive and administrative metadata are more likely to contain information about the context of their creation and the chain of custody, both of which are important for providing meaningful access to records over time. |
| **Multiplier x 1 - override on binary formats add 3** |  |

### External Dependencies

External Dependencies refers to the degree to which the format depends on a particular hardware, software and operating system to be rendered.

The ability to sustain static content is easier than sustaining dynamic content.

| Question | Description |
| :---- | :---- |
| Can the format be used in various hardware environments to be rendered? | If a specific hardware environment needed to render and migrate the file format, if yes, the likelihood of continued access is diminished. |
| Are there many renderers available for the format? | If renderers are not available for the format then there is less likelihood of providing continued access. |
| Is at least one renderer open source? | If renderers are only proprietary then the risk of being able to render the object is put at risk. Older renderers may discontinue support for older versions of the formats as they are updated. |
| Can the format be rendered or executed in multiple computing operating systems? | Formats that cannot be rendered in more than one computing operating system are typically representative of data that is difficult to transfer between computing systems. |
| Is the software that was used to create the format currently supported? | Can the software be deployed using current hardware environments? If not, then a risk to the digital object is present. |
| **Multiplier x 1** |  |

### Impact of Patents {#impact-of-patents}

Impact of Patents refers to the limitations from licenses or patents to decode formats for future use. This will impact the development of open source encoders or decoders that can aid in rendering the digital object.

| Question | Description |
| :---- | :---- |
| Is the format free of patent claims? | Formats subject to patent claims have higher preservation risk associated with them as the ability to manage the formats is tied to a specific software. |
| Does the format have open source license terms? | File formats that have open licenses associated with their usages have a low risk related to usage of the format and the creation of tools to process the format for access and long-term preservation. |
| **Multiplier x 1** |  |

### Technical Protection Mechanisms {#technical-protection-mechanisms}

Technical Protection Mechanisms (TPMs) refers to the ability to replicate digital content on new media, through migration or normalization activities.

| Question | Description |
| :---- | :---- |
| Is the format free of encryption? | Encryption restricts access and creates risks to managing and migrating files in the long-term. |
| Is the format free of technical protection measures? | Similar to encryption, technical protection measures may prevent organizations from rendering the file for validation and processing, and they also inhibit long-term access to the content. |
| **Multiplier x 2** |  |

