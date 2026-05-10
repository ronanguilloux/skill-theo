# Architecture Cognitive et Ingénierie des Connaissances : Transformation des Méthodes d'Exégèse Biblique du XXe Siècle en Compétences Algorithmiques pour Modèles de Langage

L'intersection entre la théologie biblique, la linguistique structurale et l'intelligence artificielle ouvre un champ de recherche inédit. Au XXe siècle, l'exégèse biblique s'est dotée de méthodes systématiques pour analyser le texte sacré sous ses angles historiques, littéraires, rhétoriques et sociologiques. Parce qu'elles sont par nature procédurales et heuristiques, ces méthodes fournissent un cadre théorique prêt à être traduit en architectures cognitives (ou "skills") pour les grands modèles de langage (LLM). Modéliser ces démarches permet de dépasser la simple génération probabiliste de texte pour produire un véritable raisonnement herméneutique structuré.

Ce document recense et classifie les méthodes d'exégèse biblique afin d'en extraire la logique sous-jacente. L'objectif consiste à transposer ces raisonnements humains en instructions algorithmiques, en pipelines NLP et en architectures RAG (Retrieval-Augmented Generation). Cela dotera un agent LLM de la capacité d'exécuter une démarche exégétique autonome et nuancée.

Cette architecture logicielle s'inscrit dans le paradigme actuel de **complémentarité méthodique**. Conformément au document de la Commission Biblique Pontificale *L'interprétation de la Bible dans l'Église* (1993) et à l'« exégèse canonique » de Benoît XVI, la discipline a dépassé l'opposition binaire entre approches diachroniques (l'histoire du texte) et synchroniques (le texte dans sa forme finale). L'enjeu contemporain consiste à intégrer les dimensions historiques, littéraires et théologiques sans séparer artificiellement l'exégèse savante de la lecture croyante.

## **Typologie et Évaluation Stratégique des Ressources Exégétiques**

Avant de programmer un agent LLM, il faut cartographier les ressources disponibles. Nous les organisons ici par domaines d'application, types de supports, et degré de complétude méthodologique. Cette taxonomie détermine l'architecture logicielle : elle dicte quelles sources alimenteront les bases de données vectorielles (le corpus RAG) et lesquelles dicteront la logique procédurale (les System Prompts). 

L'exégèse scientifique repose sur deux axes épistémologiques majeurs. Les approches diachroniques étudient la genèse sédimentaire du texte et sa transmission dans le temps. Les approches synchroniques, héritières du structuralisme, analysent le texte dans sa forme achevée, comme un système autonome régi par des règles littéraires internes.

### **Classification des Ressources par Domaines et Orientations Méthodologiques**

Le tableau suivant synthétise cet écosystème documentaire, identifiant les théoriciens majeurs et les corpus mobilisables pour instruire l'agent.

| **Domaine Exégétique Principal**                                                                                               | **Orientation Heuristique**                        | **Figures de Proue et Théoriciens**                                                               | **Types de Ressources et Formats Disponibles**                                                                                                | **Identifiants des Sources Analysées** |
| :----------------------------------------------------------------------------------------------------------------------------- | :------------------------------------------------- | :------------------------------------------------------------------------------------------------ | :-------------------------------------------------------------------------------------------------------------------------------------------- | :------------------------------------- |
| **Paradigme Historico-Critique** (Intègre les critiques textuelle, littéraire, des formes, de la tradition et de la rédaction) | Fondamentalement Diachronique                      | G. Bornkamm, W. Marxsen, M. Dibelius, R. Bultmann, C. Grappe, N. J. Vyhmeister                    | Manuels académiques d'introduction, guides méthodologiques séquentiels (étape par étape), monographies théologiques, syllabus universitaires. | 1-6-3-14-5                             |
| **Analyse Structurale et Sémiotique**                                                                                          | Strictement Synchronique                           | A.J. Greimas, L. Panier, R. Barthes, Équipes du CADIR (Lyon)                                      | Articles de recherche linguistique, revues de sémiotique appliquées, modélisations par schémas actantiels et carrés sémiotiques.              | 17-18-7                                |
| **Analyse Narrative (Narrative Criticism)**                                                                                    | Synchronique (centrée sur la réception)            | D. Marguerat, Y. Bourquin, J.-L. Ska, J.-N. Aletti, M.A. Powell, S. Chatman                       | Monographies littéraires, études d'impact rhétorique, syllabus de narratologie biblique, guides d'initiation.                                 | 23-24-26-1                             |
| **Rhétorique Sémitique et Biblique**                                                                                           | Synchronique (centrée sur la disposition spatiale) | R. Meynet, P. Bovati, A. Vanhoye, P. Beauchamp                                                    | Traités exhaustifs de rhétorique, manuels d'exercices pratiques, grilles taxonomiques des niveaux textuels.                                   | 29-30-31-31-34                         |
| **Approche Canonique (Canonical Criticism)**                                                                                   | Synchronique et Théologique                        | B. Childs, S. Hahn, O.-T. Venard, J. Barton, H. Cazelles                                          | Essais critiques sur l'histoire de la discipline, manifestes herméneutiques, introductions à la forme finale de l'Ancien Testament.           | 35-35-36                               |
| **Histoire de la Réception (Wirkungsgeschichte)**                                                                              | Diachronique et Herméneutique                      | A.-M. Pelletier, R. Burnet, O.-T. Venard (Projet *La Bible en ses traditions*)                    | Commentaires patristiques, études d'histoire de l'art, recueils liturgiques, bases de données encyclopédiques de réception.                   |                                        |
| **Analyse Socio-Scientifique**                                                                                                 | Diachronique, Culturelle et Anthropologique        | J.H. Elliott, B. Malina, R. Stark                                                                 | Études sociologiques, articles modélisant les structures de parenté, l'économie antique et les systèmes de valeurs méditerranéens.            | 37-38                                  |

### **Évaluation de la Complétude et de la Viabilité Algorithmique**

L'existence d'une méthode académique ne garantit pas sa traductibilité algorithmique. Pour devenir une « skill », la méthode doit présenter une structure procédurale stricte, décomposable en étapes séquentielles, en arbres de décision ou en heuristiques paramétrables. L'évaluation suivante mesure la capacité de ces méthodes à être converties en instructions (Prompt Chaining) ou en code de parsage.

| **Méthodologie**                                    | **Degré de Complétude Algorithmique** | **Description de l'Adaptabilité pour le Traitement par LLM**                                                                                                                                                                                                                                                 |
| :-------------------------------------------------- | :------------------------------------ | :----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **Rhétorique Sémitique** (Meynet)                   | **Très Haute**                        | Cette méthode définit des unités textuelles strictes et emboîtées (terme, membre, segment, morceau, partie, passage) obéissant à des lois de symétrie. Elle est idéale pour le parsing JSON récursif, la création d'arbres syntaxiques abstraits (AST) et le calcul de similarité cosinus entre vecteurs.    |
| **Analyse Sémiotique** (Greimas/Panier)             | **Haute**                             | Reposant sur des oppositions logiques binaires (le carré sémiotique) et des relations actantielles mathématisables (Sujet/Objet, Destinateur/Destinataire). Elle se traduit naturellement en graphes de connaissances (Knowledge Graphs) et en requêtes d'extraction d'entités nommées et de relations.      |
| **Critique de la Rédaction** (Redaktionsgeschichte) | **Haute**                             | Nécessite des opérations de comparaison différentielle systématique (par exemple, soustraire le texte source de Marc au texte dérivé de Matthieu pour isoler les altérations éditoriales). S'implémente parfaitement par des algorithmes d'alignement de séquences et d'attention croisée (Cross-Attention). |
| **Histoire de la Réception** (*Wirkungsgeschichte*) | **Moyenne**                           | Repose sur la collecte d'un corpus hétérogène (Pères de l'Église, liturgie, histoire de l'art). Idéale pour être modélisée via une architecture RAG massive et transversale, permettant de tracer l'évolution des interprétations au fil des siècles.                                                        |
| **Analyse Narrative**                               | **Moyenne**                           | Implique des concepts psychologiques nuancés comme l'"auteur implicite", le "lecteur implicite" ou l'"ironie dramatique". Exige des instructions de prompting très avancées, s'appuyant sur l'analyse de sentiment fine et la détection d'états mentaux (Theory of Mind).                                    |
| **Critique des Formes** (Formgeschichte)            | **Moyenne à Basse**                   | Repose fortement sur la déduction spéculative du contexte sociologique originel (le *Sitz im Leben*). Nécessite la construction d'une base de données RAG massive sur l'histoire du Proche-Orient Ancien pour limiter les hallucinations du LLM lors des inférences historiques.                             |
| **Approche Canonique** (Childs)                     | **Basse**                             | Approche macro-structurelle, dogmatique et théologique, exigeant de percevoir la Bible comme un tout spirituellement unifié. Difficile à formuler en étapes mathématiques discrètes, elle relève davantage de l'alignement global (Fine-Tuning) théologique du modèle que d'un script procédural.            |

## **Déconstruction de la Méthode Historico-Critique pour le Traitement Automatique des Langues (TAL)**

Standard académique incontournable de la première moitié du XXe siècle, la méthode historico-critique vise à restituer l'épaisseur historique du texte. Elle déploie une série de « critiques » qui désassemblent le récit pour retracer sa genèse matérielle et idéologique. Pour un LLM, cette méthode se modélise comme un pipeline de rétro-ingénierie textuelle, chaque étape fonctionnant comme un filtre d'analyse distinct.

### **La Phase Fondatrice : Critique Textuelle et Philologie Computationnelle**

La première étape, la critique textuelle, garantit la fiabilité matérielle du document source. L'exégèse s'applique aux langues originales (hébreu, araméen, grec) en s'appuyant sur l'apparat critique des manuscrits antiques, et non sur des traductions vernaculaires.

L'agent LLM devra intégrer une fonction de critique textuelle capable d'ingérer simultanément plusieurs variantes manuscrites d'un même verset. Le système appliquera des règles historiques codées pour évaluer les probabilités de corruption scribale. Par exemple, il privilégiera statistiquement les *lectiones difficiliores* (les leçons difficiles ou grammaticalement rugueuses, présumées plus proches de l'original) par rapport aux *lectiones faciliores* (les leçons lissées par les copistes). L'agent effectuera ensuite un traitement NLP spécifique aux langues anciennes, incluant la tokenisation morphologique et la lemmatisation, pour résoudre les ambiguïtés sémantiques avant de proposer une interprétation.

### **La Catégorisation Documentaire : Critique Littéraire et Détection des Genres**

Une fois le texte établi, la critique littéraire délimite la péricope (l'unité textuelle autonome) et identifie son genre littéraire. Ce genre opère comme un contrat de lecture dictant les règles d'interprétation : on ne lit pas un code législatif prescriptif avec la grille d'analyse d'un psaume de lamentation.

Algorithmiquement, cette étape relève de la classification de texte (Text Classification). Via des instructions *few-shot learning* chargées d'exemples annotés, l'agent analysera les n-grammes, la temporalité des verbes et les formules stéréotypées pour étiqueter la péricope. Une forte densité de verbes à l'impératif couplée à un vocabulaire de pureté orientera automatiquement le LLM vers une exégèse normative.

### **L'Archéologie Sociologique : La Critique des Formes (*Formgeschichte*) et le *Sitz im Leben***

La critique des formes (*Formgeschichte*) postule que les textes bibliques majeurs résultent de l'assemblage de petites unités de tradition indépendantes, transmises d'abord oralement. L'objectif est d'identifier le *Sitz im Leben*, c'est-à-dire le contexte institutionnel ou la situation sociale récurrente (liturgie, tribunal, catéchèse) qui a vu émerger cette forme spécifique.

Pour simuler la *Formgeschichte*, le LLM désassemblera virtuellement le chapitre en péricopes autonomes hypothétiques. Il isolera le noyau narratif (souvent un *logion* encapsulé dans un récit cadre) et interrogera sa base vectorielle pour générer des probabilités sur la fonction sociale du fragment, croisant sa structure rhétorique avec des modèles sociologiques de l'Antiquité.

### **L'Intentionnalité Éditoriale : La Critique de la Rédaction (*Redaktionsgeschichte*)**

La critique de la rédaction (*Redaktionsgeschichte*) déplace l'attention vers l'éditeur final. Ce dernier n'est plus vu comme un simple compilateur, mais comme un auteur créatif doté d'une ligne idéologique forte. La méthode consiste à comparer systématiquement un récit tardif avec sa source présumée pour y détecter les coutures éditoriales. 

L'architecture des LLMs se prête particulièrement bien à cette tâche, qui s'apparente conceptuellement au contrôle de version (Git) et à l'analyse différentielle :
1. **Ingestion et Alignement :** L'agent charge les textes parallèles (ex: la synopse évangélique) et génère un alignement structurel des péricopes.
2. **Traitement Différentiel et Attention Croisée :** Le modèle isole mathématiquement les divergences. Il calcule les deltas textuels (ajouts, omissions, modifications) pour identifier le vocabulaire préférentiel du rédacteur.
3. **Inférence Théologique :** Sur la base de ces altérations, le LLM synthétise l'agenda idéologique de l'auteur final (par exemple, identifier la propension de Luc à souligner l'universalisme du salut là où Matthieu insiste sur l'accomplissement des prophéties d'Israël).

## **La Révolution Synchronique : Analyse Structurale et Sémiotique de l'Énonciation**

Dans la seconde moitié du XXe siècle, le tournant synchronique décide d'étudier le texte comme un objet littéraire unifié et autonome, indépendamment de sa genèse historique. Des institutions comme le CADIR à Lyon (Louis Panier, Jean Delorme) ont adapté l'analyse structurale et la sémiotique de Greimas aux textes sacrés.

### **Les Postulats Axiomatiques de la Sémiotique Algorithmique**

Cette approche repose sur deux principes théoriques extrêmement rigides, qui constituent d'excellentes contraintes algorithmiques :
1. **Le principe de clôture :** Le texte est un système clos se suffisant à lui-même. Le LLM doit ignorer le contexte socio-historique et l'auteur réel pour s'en tenir à l'architecture de l'énoncé.
2. **Le postulat de différence :** Le sens ne naît pas de l'essence d'un mot, mais des oppositions internes au système. 

### **Modélisation du Schéma Narratif et Actantiel par Graphes de Connaissances**

Le modèle actantiel de Greimas réduit l'infinie variété des personnages à seulement six rôles fonctionnels (ou actants), organisés par paires : Sujet/Objet, Destinateur/Destinataire, Adjuvant/Opposant.

En ingénierie des connaissances, cela correspond à une tâche avancée d'extraction d'information. L'agent ne lira pas une histoire peuplée de "personnages", mais exécutera une résolution des coréférences pour lier les entités. Il contraindra ensuite sa réponse dans un schéma JSON strict assignant ces six actants. En parallèle, l'agent calculera le "carré sémiotique", cartographiant les oppositions sémantiques binaires (vie/mort, non-vie/non-mort) pour mesurer logiquement la trajectoire du Sujet au fil du récit.

Pour intégrer la "sémiotique de l'énonciation" (qui prend en compte l'acte dynamique de lire), l'agent inclura une couche d'analyse pragmatique modélisant l'interaction entre l'énoncé statique et l'expérience du lecteur intratextuel.

## **L'Analyse Narrative : Modélisation des États Mentaux et de la Vitesse du Récit**

L'analyse narrative (*Narrative Criticism*) envisage le texte non pas comme une fenêtre documentaire sur l'histoire antique, mais comme un miroir esthétique qui invite le lecteur à créer du sens. Des spécialistes comme Daniel Marguerat, Yvan Bourquin ou Jean-Noël Aletti (côté catholique) ont démontré que la stratégie communicationnelle du récit produit intrinsèquement sa propre théologie. 

La méthode sépare l'histoire racontée (le contenu factuel) et le discours (la mise en récit, la vitesse, le point de vue).

### **L'Ingénierie des Acteurs Textuels et de l'Ironie**

L'exégèse narrative ignore l'auteur charnel. Elle modélise des acteurs intratextuels : l'"auteur implicite" (la conscience organisatrice derrière le texte) et le "lecteur implicite" (le récepteur idéal construit par l'œuvre).

La traduction algorithmique de cette dynamique exige l'implémentation de mécanismes d'attention narrative :
1. **Cartographie temporelle et métriques de rythme :** Le LLM extraira les marqueurs chronologiques pour distinguer le temps de l'histoire du temps du récit. En croisant la durée diégétique avec le nombre de tokens générés, l'algorithme détectera mathématiquement les accélérations (sommaires) et les décélérations (scènes ralenties) qui signalent une insistance théologique.
2. **Simulation d'États Mentaux (Theory of Mind pour LLM) :** Pour repérer l'ironie dramatique, le LLM fragmentera sa base de connaissances locales. Le prompt lui demandera d'isoler ce que sait le "Lecteur Implicite" à un verset donné, puis de le comparer aux connaissances du personnage intradiégétique. Cet écart sémantique révélera les tensions et asymétries dramatiques générées par le déficit d'information.

## **Rhétorique Sémitique et Arborescences Algorithmiques : Le Modèle de Roland Meynet**

L'analyse rhétorique appliquée à la Bible, ou "rhétorique sémitique", est sans doute la méthode la plus compatible organiquement avec le traitement automatique des langues. Systématisée par des savants comme Roland Meynet, Pietro Bovati ou Paul Beauchamp, cette approche rompt avec la logique linéaire gréco-latine. La pensée hébraïque s'articule spatialement, par d'immenses jeux de symétries, de parallélismes et de structures concentriques.

### **La Taxonomie Structurelle et Fractale de Meynet**

La taxonomie de Meynet divise le texte en unités strictement emboîtées : terme, membre, segment, morceau, partie, et passage. L'interprète identifie les correspondances (parallélismes synonymiques, antithétiques) et relève les architectures spécifiques, notamment le chiasme (symétrie concentrique de type A-B-C-B'-A'). Dans la poétique sémitique, le centre géométrique d'un chiasme (le point 'C') contient systématiquement le message fondamental.

Cet emboîtement correspond techniquement au parsage syntaxique et à la génération d'arbres (Abstract Syntax Trees - AST) :
* **Parsage Hiérarchique et Embeddings :** L'agent segmente le texte et utilise le calcul de similarité cosinus entre les embeddings lexicaux pour détecter les récurrences et oppositions.
* **Génération de Structure de Données :** L'agent restitue l'architecture spatiale via du code hiérarchique balisé (JSON ou XML strict), étiquetant scrupuleusement les nœuds (`<partie>`, `<morceau>`, `<segment>`).
* **Inférence Sémantique Automatisée :** Un algorithme parcourt les nœuds pour identifier les chiasmes. S'il isole une structure concentrique, il attribue un poids d'inférence (attention weight) maximal au nœud central lors de l'exégèse finale générée par le LLM, garantissant que l'agent capture l'intention principale de l'auteur.

## **L'Intégration Macro-Structurelle : Les Approches Canonique et Socio-Scientifique**

Si l'analyse rhétorique dissèque le texte au microscope, l'exégèse contemporaine nécessite également des outils macroscopiques pour ne pas produire une interprétation atomisée et hors-sol.

### **La Perspective Canonique de Brevard Childs et l'Intertextualité RAG**

La critique canonique (*Canonical Approach*) de Brevard Childs postule que le sens théologique normatif se trouve exclusivement dans la forme finale du canon biblique, tel qu'il a été édité et reçu par les communautés historiques, et non dans des sources archaïques reconstruites. Ce paradigme, aujourd'hui central dans l'exégèse catholique (cf. Scott Hahn ou le projet *La Bible en ses traditions* d'O.-T. Venard), exige d'interpréter chaque péricope à la lumière de l'ensemble de l'Écriture.

Cette posture herméneutique s'implémente via le déploiement d'une architecture RAG intra-biblique à l'échelle globale. L'agent lance silencieusement une requête de similarité vectorielle multidimensionnelle sur l'immense base de données du corpus canonique pour rapatrier les allusions intertextuelles et les résonances typologiques. Le System Prompt force alors l'agent à fusionner son analyse micro-locale avec cette méta-structure théologique.

### **La Matrice Culturelle : L'Analyse Socio-Scientifique**

L'analyse socio-scientifique (John H. Elliott, Bruce Malina) corrige le biais anachronique occidental en réinscrivant les textes dans la matrice sociale et économique des sociétés agraires méditerranéennes antiques (système binaire de l'honneur et de la honte, patronage, lois implacables de pureté rituelles).

La modélisation intègre un "Module d'Évaluation Anthropologique". L'IA est conditionnée avec ces concepts sociologiques pour repérer les dynamiques implicites. Au lieu de lire une guérison miraculeuse par le prisme de la médecine moderne, l'agent décodera algorithmiquement cet acte comme une subversion sociale visant à réintégrer un marginal (considéré impur) au cœur du système d'honneur communautaire.

### **L'Écho Temporel : L'Histoire de la Réception (*Wirkungsgeschichte*)**

Devenue incontournable dans l'espace francophone avec Anne-Marie Pelletier ou Régis Burnet, l'histoire de la réception (*Wirkungsgeschichte*) affirme que le sens du texte inclut la sédimentation historique de ses lectures (commentaires patristiques, liturgies, usages en histoire de l'art). 

La traduction algorithmique de cette méthode requiert la création d'une architecture RAG massive croisant des corpus hétérogènes. L'agent algorithmique ne cherche pas seulement le "sens originel" ; il trace le vecteur diachronique de signification. La "Skill Réception" moissonnera ces bases de données externes pour cartographier la manière dont le potentiel sémantique du texte s'est actualisé au fil des siècles.

## **Conclusion**

Transformer ces méthodes exégétiques en "skills" pour LLM ne relève pas de la simple automatisation utilitaire. L'ambition consiste à équiper l'IA de protocoles heuristiques et de garde-fous méthodologiques capables de traiter l'extrême complexité et la polysémie du texte biblique. En traduisant mathématiquement la critique de la rédaction, la poétique symétrique de l'Orient antique, la sociologie méditerranéenne ou l'histoire de la réception, nous dotons l'agent d'une véritable profondeur herméneutique multidimensionnelle.

L'architecture finale de cet agent exégétique réalise techniquement l'idéal de l'épistémologie contemporaine : l'intégration. Plutôt que d'appliquer ces outils de manière isolée, l'agent orchestre leur complémentarité. En articulant l'histoire et la littérature, la philologie et la théologie, cette alliance entre l'exégèse classique et l'informatique permet au modèle de restituer la richesse des textes fondateurs, fidèle à la fois à la rigueur scientifique et à l'intelligence croyante.

#### **Sources des citations**

1.  Biblical Exegesis - WJK Books, consulté le mai 9, 2026, <https://www.wjkbooks.com/wp-content/uploads/productsamples/0664266983.pdf>
2.  HANDBOOK OF BIBLICAL CRITICISM - WJK Books, consulté le mai 9, 2026, <https://www.wjkbooks.com/wp-content/uploads/productsamples/0664235344.pdf>
3.  Exégèse biblique - Wikipédia, consulté le mai 9, 2026, <https://fr.wikipedia.org/wiki/Ex%C3%A9g%C3%A8se_biblique>
4.  L'exégèse critique aujourd'hui - Cairn, consulté le mai 9, 2026, <https://shs.cairn.info/article/RSR_112_0185/pdf?lang=fr>
5.  Réalisation de votre exégèse en cinq étapes, consulté le mai 9, 2026, <https://www.unige.ch/theologie/distance/courslibre/atesadan2006/lecon5/exegese5.htm>
6.  L'analyse de la rédaction et l'exégèse canonique - LeVigilant.com, consulté le mai 9, 2026, <https://levigilant.com/Dictionnaire_Tim_Bulkeley/histoire/canonique.htm>
7.  www.reliprofs.be, consulté le mai 9, 2026, <https://www.reliprofs.be/RELIdocument/profs/grillesanalysebiblique__5462-1.doc>
8.  étudier un texte biblique en 8 étapes - Timothée Minard, consulté le mai 9, 2026, <https://timotheeminard.com/wp-content/uploads/2016/12/Etudier-un-texte-biblique-en-8-%C3%A9tapes.pdf>
9.  Exégèse historico-critique de la Bible - Wikipédia, consulté le mai 9, 2026, <https://fr.wikipedia.org/wiki/Ex%C3%A9g%C3%A8se_historico-critique_de_la_Bible>
10. Redaction criticism - Wikipedia, consulté le mai 9, 2026, <https://en.wikipedia.org/wiki/Redaction_criticism>
11. Un plaidoyer théologique pour la méthode historico-critique - OpenEdition Journals, consulté le mai 9, 2026, <https://journals.openedition.org/rsr/1941>
12. Grappe, Christian, Manuel d'exégèse du Nouveau Testament - OpenEdition Journals, consulté le mai 9, 2026, <https://journals.openedition.org/rsr/18635>
13. Redaction Criticism of the Gospels - The Bart Ehrman Blog, consulté le mai 9, 2026, <https://ehrmanblog.org/redaction-criticism-of-the-gospels/>
14. Dr. Robert C. Newman, Synoptic Gospels, Lecture 15 Redaction Criticism - Biblical eLearning, consulté le mai 9, 2026, <https://biblicalelearning.org/wp-content/uploads/2024/08/Newman_Synoptics_EN_Lecture15.pdf>
15. Structuralism and Biblical Studies - Religion Online, consulté le mai 9, 2026, <https://www.religion-online.org/article/structuralism-and-biblical-studies/>
16. Introduction to Structuralism - University of Idaho, consulté le mai 9, 2026, <https://www.uidaho.edu/class/eng506/structuralism.htm>
17. CADIR - Centre pour l'Analyse du Discours Religieux, consulté le mai 9, 2026, <https://www.ucly.fr/la-recherche/poles-de-recherche/pole-de-recherche-theologie-philosophie-et-sciences-religieuses/cadir/>
18. Sémiotique et Bible - Cairn, consulté le mai 9, 2026, <https://www.cairn.info/revue-recherches-de-science-religieuse-2006-2-page-211.htm>
19. Structuralism and Semiotics - University of Oxford, consulté le mai 9, 2026, <https://www.ox.ac.uk/admissions/undergraduate/courses/course-listing/structuralism-and-semiotics>
20. A.J. Greimas - Wikipedia, consulté le mai 9, 2026, <https://en.wikipedia.org/wiki/Algirdas_Julien_Greimas>
21. Louis Panier - Babelio, consulté le mai 9, 2026, <https://www.babelio.com/auteur/Louis-Panier/115409>
22. Narrative Criticism - Oxford Bibliographies, consulté le mai 9, 2026, <https://www.oxfordbibliographies.com/view/document/obo-9780195393361/obo-9780195393361-0012.xml>
23. What is Narrative Criticism? - GotQuestions.org, consulté le mai 9, 2026, <https://www.gotquestions.org/narrative-criticism.html>
24. Narrative Criticism of the New Testament - Society of Biblical Literature, consulté le mai 9, 2026, <https://www.sbl-site.org/publications/article.aspx?articleId=259>
25. Narrative Criticism - Religion Online, consulté le mai 9, 2026, <https://www.religion-online.org/article/narrative-criticism/>
26. Daniel Marguerat - Wikipedia, consulté le mai 9, 2026, <https://fr.wikipedia.org/wiki/Daniel_Marguerat>
27. Yvan Bourquin - Labor et Fides, consulté le mai 9, 2026, <https://www.laboretfides.com/fr_fr/auteur/yvan-bourquin.html>
28. Jean-Louis Ska - Wikipedia, consulté le mai 9, 2026, <https://fr.wikipedia.org/wiki/Jean-Louis_Ska>
29. Rhétorique sémitique - Wikipédia, consulté le mai 9, 2026, <https://fr.wikipedia.org/wiki/Rh%C3%A9torique_s%C3%A9mitique>
30. Biblical Rhetoric - Oxford Bibliographies, consulté le mai 9, 2026, <https://www.oxfordbibliographies.com/view/document/obo-9780195393361/obo-9780195393361-0014.xml>
31. Roland Meynet - Wikipedia, consulté le mai 9, 2026, <https://fr.wikipedia.org/wiki/Roland_Meynet>
32. Albert Vanhoye - Wikipedia, consulté le mai 9, 2026, <https://fr.wikipedia.org/wiki/Albert_Vanhoye>
33. Paul Beauchamp - Wikipedia, consulté le mai 9, 2026, <https://fr.wikipedia.org/wiki/Paul_Beauchamp>
34. Jean-Noël Aletti - Wikipedia, consulté le mai 9, 2026, <https://fr.wikipedia.org/wiki/Jean-No%C3%ABl_Aletti>
35. Canonical Criticism - Wikipedia, consulté le mai 9, 2026, <https://en.wikipedia.org/wiki/Canonical_criticism>
36. Brevard Childs - Wikipedia, consulté le mai 9, 2026, <https://en.wikipedia.org/wiki/Brevard_Childs>
37. Social-Scientific Criticism of the New Testament - Oxford Bibliographies, consulté le mai 9, 2026, <https://www.oxfordbibliographies.com/view/document/obo-9780195393361/obo-9780195393361-0016.xml>
38. Social-Scientific Criticism - Religion Online, consulté le mai 9, 2026, <https://www.religion-online.org/article/social-scientific-criticism/>
39. John H. Elliott - Wikipedia, consulté le mai 9, 2026, <https://en.wikipedia.org/wiki/John_H._Elliott>
40. Bruce Malina - Wikipedia, consulté le mai 9, 2026, <https://en.wikipedia.org/wiki/Bruce_Malina>
