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

