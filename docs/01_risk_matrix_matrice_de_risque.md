# Format Risk Matrix
Last updated: 2026-05-25

## Purpose

The format risk matrix outlines the formats in FRDR and assigned a risk level which is derived by answering a series of weighted questions. The risk matrix borrows heavily from NARA’s File Format Risk Matrix. The sections outlined below provide guidance on how to fill in the sheet. 

## Risk Levels

Risk levels are divided into three categories:

| Category | Description |
| :---- | :---- |
| Low 0% \- 25 % | Files are well supported, widely-adopted, and have open stable specifications. |
| Moderate 26% \- 50% | Files pose some challenges but the risks are manageable. |
| High 51% \- 100% | Files pose significant challenges to long-term access and reuse. Factors include lack of documentation, proprietary, or obsolete dependencies. |

### Weighting

The weight system for the risk analysis is as follows

* Yes \= 1  
* No \= 0  
* N/A \= not included in the calculation

The following areas are assigned a multiplier weight depending on the risk associated with a negative answer.

| Category | Multiplier rate | Total Possible Points\* |
| :---- | :---- | :---- |
| Disclosure | Critical \= 3 | 12 |
| Adoption | High \= 2 | 6 |
| Transparency | Standard \= 1 | 4 \*add 3 to the overall maximum totally for binary formats. |
| Self-documentation | Standard \= 1 | 2 |
| External Dependencies | Standard \= 1 | 5 |
| Patents | Standard \= 1 | 2 |
| TPMs | High \= 2 | 4 |

\*Total possible points can change if a risk element is not applicable

### Calculation

Final preservation score % \= (sum of weighted points/total maximum possible weighted points) x 100

Final risk score \= 100% \- Final preservation score

A penalty of 3 points is added to the overall maximum score if the format is binary.

## Resources

* [Sustainability Factors](https://www.loc.gov/preservation/digital/formats/sustain/sustain.shtml) (LoC)	  
* [Danish National Archives \- Concept Model](https://github.com/the-danish-national-archives/concept-model/tree/main/P2%20Format%20Assessment)   
* [https://github.com/usnationalarchives/digital-preservation/tree/full/Digital\_Preservation\_Risk\_Matrix](https://github.com/usnationalarchives/digital-preservation/tree/master/Digital_Preservation_Risk_Matrix)	  
* [https://harvardwiki.atlassian.net/wiki/spaces/digitalpreservation/pages/48136762/Assessment+Tool](https://harvardwiki.atlassian.net/wiki/spaces/digitalpreservation/pages/48136762/Assessment+Tools)

## Matrix Elements and Questions

### Disclosure

Disclosure refers to the degree to which a complete specification of the format exists and is accessible. Specifications that go through external expert evaluation are preferable.

| Question | Description |
| :---- | :---- |
| Is the format open? | Indicate how open the file format is. For example, the file format has an open license or is proprietary and has a restricted license that is owned by a company or individual. Restricted licensing can be linked to preservation challenges including obsolescence and backward compatibility issues. |
| Does the format have a published specification? | Indicate whether the format has an openly published specification. By open it means that the specification is not behind a paywall. |
| **If yes,** is the specification published and approved by a standards organization? | Specifications that have been approved and published by an internationally recognized standards organization have undergone a controlled process for creation and publication. There is a stable mechanism for maintaining the specification. |
| Was the specification updated in the last 5 years? | As formats age, the potential risk increases because they may be superseded by newer formats and software and tool support may decrease. |
| **Multiplier x 3** |  |

### Adoption

Adoption refers to the level in which a format is in use by the community, primary creators and disseminators. The more widely used the format the less likely it will disappear. Tools to mitigate obsolescence such as emulation and migration are more likely to be in place. If the format has been assessed as preferred or acceptable for long-term preservation at other repositories or institutions engaged with long-term preservation work, this also provides evidence of adoption. 

| Question | Description |
| :---- | :---- |
| Is the format used for preservation in the community? | Formats that are used widely by repositories and the larger digital preservation as a preferred preservation formats, are likely to be more stable in the long-term |
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
| Can the file be identified by elements other than the extension?  | File formats that have an internal signature increases the ability of the file being identified. |
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

### Impact of Patents

Impact of Patents refers to the limitations from licenses or patents to decode formats for future use. This will impact the development of open source encoders or decoders that can aid in rendering the digital object.

| Question | Description |
| :---- | :---- |
| Is the format free of patent claims? | Formats subject to patent claims have higher preservation risk associated with them as the ability to manage the formats is tied to a specific software. |
| Does the format have open source license terms? | File formats that have open licenses associated with their usages have a low risk related to usage of the format and the creation of tools to process the format for access and long-term preservation. |
| **Multiplier x 1** |  |

### Technical Protection Mechanisms

Technical Protection Mechanisms (TPMs) refers to the ability to replicate digital content on new media, through migration or normalization activities.

| Question | Description |
| :---- | :---- |
| Is the format free of encryption? | Encryption restricts access and creates risks to managing and migrating files in the long-term. |
| Is the format free of technical protection measures? | Similar to encryption, technical protection measures may prevent organizations from rendering the file for validation and processing, and they also inhibit long-term access to the content. |
| **Multiplier x 2** |  |

---
# Matrice des risques
Dernière mise à jour : 2026-05-25

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

L'adoption désigne le degré d'utilisation d'un format par la communauté, les principaux créateurs et les diffuseurs. Plus un format est largement utilisé, moins il risque de disparaître. Des outils visant à limiter son obsolescence, tels que l'émulation et la migration, sont alors plus susceptibles d'être mis en place. Si le format a été jugé préférable ou acceptable pour la préservation à long terme par d'autres dépôts ou institutions engagés dans des travaux de préservation à long terme, cela constitue également une preuve de son adoption. 

| Question | Description |
| :---- | :---- |
| Le format est-il utilisé à des fins de préservation par la communauté ? | Les formats largement utilisés par les dépôts et reconnus comme formats de préservation privilégiés sont généralement plus stables à long terme.|
| Le format est-il répandu au sein de la communauté ou du domaine de recherche ? | Plus un format est largement utilisé dans un domaine de recherche ou pour les données de recherche en général, plus il est susceptible d’être maintenu à long terme. |
| Le format est-il activement maintenu par une communauté ?| Les formats maintenus par une communauté, plutôt que par une ou deux personnes, sont plus susceptibles de rester disponibles à long terme. |
| **Multiplicateur x 2**|  |

### Transparence

La transparence désigne un format pouvant être analysé à l'aide d'outils de base, notamment des éditeurs de texte brut. La transparence est renforcée si les métadonnées sont intégrées pour le contenu non textuel dans un fichier Unicode utilisant l'encodage UTF-8. Le code source est plus transparent que le code compilé. 

Le chiffrement est incompatible avec la transparence.

La compression nuit à la transparence. Si un référentiel doit accepter des données compressées, il est préférable d'utiliser des algorithmes de compression courants et largement utilisés. Une compression sans perte est préférable à une compression avec perte.

| Question | Description |
| :---- | :---- |
| Le format est-il en mode caractère ? | Les formats basés sur des caractères sont lisibles par l’humain, indépendants des plateformes et fondés sur un encodage de caractères (ASCII, UTF-8, etc.). |
| Le fichier peut-il être identifié par des éléments autres que son extension ? | Les formats disposant d’une signature interne facilitent l’identification des fichiers. Ces signatures devraient figurer dans un registre de formats. |
| Le format est-il non compressé ? | Les formats compressés sont utilisés pour optimiser l’espace et la transmission, mais certaines méthodes de compression entraînent une suppression permanente de données. Les deux méthodes de compression les plus courantes sont la compression avec perte (Losey) et la compression. |
| Le cas échéant, le format utilise-t-il une compression avec perte ? |La compression avec perte supprime définitivement des données des fichiers, entraînant une dégradation par rapport à l’original.|
| **Multiplicateur x 1** | 

### Auto-documentation

L'auto-documentation désigne les formats dans lesquels les métadonnées sont stockées avec l'objet numérique et servent à afficher ce dernier. Ces formats sont plus faciles à conserver à long terme. La capacité du format à contenir des métadonnées administratives et techniques constitue un avantage pour la préservation.

| Question | Description |
| :---- | :---- |
| Le format inclut-il nativement des métadonnées documentant le fichier et l’environnement technique utilisé pour sa création (et/ou sa modification) ? | Les formats intégrant nativement des métadonnées techniques relatives à leur création sont généralement plus faciles à maintenir et à rendre accessibles dans le temps.|
| Le format permet-il l’intégration de métadonnées intégrées, manuellement ou automatiquement ? | Les formats qui prennent en charge l’intégration de métadonnées descriptives et administratives intégrées sont plus susceptibles de contenir des informations sur le contexte de création et la chaîne de conservation, deux éléments essentiels pour assurer un accès significatif à long terme.|
| **Multiplicateur x 1 - pour les formats binaires, ajouter 3** |  | 

### Dépendances externes

Les « dépendances externes » désignent le degré de dépendance du format vis-à-vis d'un matériel, d'un logiciel et d'un système d'exploitation spécifiques pour son affichage.

Il est plus facile de prendre en charge un contenu statique qu'un contenu dynamique.

| Question | Description |
| :---- | :---- |
| Ce format peut-il être utilisé dans différents environnements matériels pour être affiché ? | Si un environnement matériel particulier est requis pour le rendu et la migration du format, la probabilité d’un accès continu diminue.|
| Existe-t-il plusieurs logiciels permettant le rendu du format ? | Si aucun logiciel permettant de rendre le format n’est disponible, il devient plus difficile d’assurer un accès continu. |
| Au moins un logiciel permettant le rendu du format est-il à code source ouvert ?| Lorsque les logiciels de rendu sont exclusivement propriétaires, le risque d’impossibilité de rendre les fichiers à l’avenir augmente. À mesure que les logiciels sont mis à jour, la prise en charge des versions plus anciennes des formats peut être abandonnée. |
| Le format peut-il être rendu ou exécuté sur plusieurs systèmes d’exploitation ?| Les formats qui ne peuvent être rendus sur plus d’un système d’exploitation sont généralement plus difficiles à transférer entre environnements informatiques.|
| Existe-t-il actuellement un logiciel pris en charge dans les environnements informatiques actuels permettant de créer ce format ? | Le logiciel peut-il être déployé sur les environnements matériels actuels ? Si ce n'est pas le cas, cela représente un risque pour l'objet numérique. |
| **Multiplicateur x 1** |  |

### Incidence des brevets

L'impact des brevets fait référence aux restrictions imposées par les licences ou les brevets concernant le décodage des formats en vue d'une utilisation future. Cela aura des répercussions sur le développement d'encodeurs ou de décodeurs open source susceptibles de faciliter le rendu de l'objet numérique.

| Question | Description |
| :---- | :---- |
| Le format est-il assujetti à des revendications de brevet ? | Les formats assujettis à des revendications de brevet présentent un risque accru en matière de préservation, car leur gestion dépend d’un logiciel spécifique.|
| Le format est-il assorti de modalités de licence libre ou à code source ouvert ? | Les formats de fichiers dont l'utilisation est régie par des licences ouvertes présentent un risque moindre en matière de pérennité de l'accès. |
| **Multiplicateur x 1** |  |

### Mécanismes de protection technique

Les mécanismes techniques de protection  désignent la capacité à reproduire des contenus numériques sur de nouveaux supports, par le biais d'opérations de migration ou de normalisation.

| Question | Description |
| :---- | :---- |
| Le format nécessite-t-il un chiffrement ? | Le chiffrement restreint l’accès et crée des risques pour la gestion et la migration des fichiers à long terme. |
| Le format utilise-t-il des mesures de protection techniques ? | À l’instar d’autres formes de chiffrement, les mesures techniques de protection peuvent empêcher les organisations de rendre les fichiers à des fins de validation et de traitement, et entravent également l’accès à long terme au contenu. |
| **Multiplicateur x 2** |  |



