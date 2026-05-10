# Skills Théologiques et Exégétiques pour Assistants IA

Les LLMs sont programmés pour être consensuels. Demandez-leur une analyse biblique, et ils vous recracheront souvent une synthèse tiède façon "Wikipédia", mélangeant dix traditions différentes pour ne fâcher personne.

Ce dépôt contient des "Skills" pour contrer ça. Il s'agit de dossiers d'instructions (au format [Agent Skills](https://agentskills.io/)) que vous pouvez charger dans votre assistant IA pour le forcer à utiliser une méthode de lecture spécifique et tranchée.

## Comment ça marche ?

Ce n'est pas juste un gros prompt. Le système repose sur la lecture à la demande : l'agent garde le fichier du skill sous le coude et le lit uniquement quand il en a besoin, ce qui évite de polluer sa mémoire le reste du temps.

Quand vous invoquez un skill, l'IA arrête d'être généraliste. Elle est obligée d'utiliser le vocabulaire, les concepts et la logique du courant théologique que vous avez choisi.

## Les Skills

### Disponibles

*   **[`robert-alter-analyse`](./robert-alter-analyse/)** : Analyse de l'Ancien Testament avec la grille littéraire de Robert Alter. Au lieu de faire de la théologie, l'agent va chercher les mots-guides (*Leitwort*), démonter les scènes-types et pointer l'ironie dramatique.
*   **[`theo-rethorique-semitique`](./theo-rethorique-semitique/)** : Analyse de l'architecture formelle des textes bibliques (et sémitiques) selon la méthode de Roland Meynet. L'agent effectue un découpage rigoureux (membres, segments, morceaux) et en révèle les structures symétriques (chiasmes, compositions concentriques, binarité) pour en déduire le sens théologique (fonction anti-idolâtrique, etc.). **Comment l'invoquer :** Ce skill est conçu pour une invocation explicite. Appelez-le en mentionnant des termes comme *Roland Meynet*, *analyse rhétorique biblique*, *rhétorique sémitique*, ou *figures de composition*.

### En projet

Nous avons besoin d'autres grilles de lecture pour séparer les approches. Basé sur la cartographie stratégique de l'exégèse :

*   **`theo-exegese-historico-critique`** : La méthode fondatrice (diachronique). Le skill désassemblera le texte pour remonter à ses sources. Il appliquera la critique textuelle (variantes manuscrites), la critique littéraire (genres), la *Formgeschichte* (contexte sociologique d'origine ou *Sitz im Leben*) et la *Redaktionsgeschichte* (agenda théologique du rédacteur final).
*   **`theo-semiotique-greimas`** : L'analyse purement synchronique et structurale (CADIR, Louis Panier). Le skill enfermera le modèle dans la clôture du texte. Il ignorera l'histoire pour mapper les relations logiques via le schéma actantiel (Sujet/Objet, Destinateur/Destinataire) et le carré sémiotique des oppositions fondamentales.
*   **`theo-analyse-narrative`** : L'étude de la stratégie de communication du récit (Marguerat, Bourquin). Le skill modélisera les états mentaux des acteurs intratextuels (auteur implicite, lecteur implicite) et calculera la vitesse du récit pour faire émerger l'ironie dramatique et les tensions narratives.
*   **`theo-critique-canonique`** : L'approche théologique globale (Childs). Le skill évaluera la péricope non pas de manière isolée, mais en l'insérant de force dans la forme finale et globale du canon biblique, exigeant une résonance intertextuelle avec l'ensemble des Écritures.
*   **`theo-analyse-socio-scientifique`** : Le décodage anthropologique (Elliott, Malina). Le skill brisera nos biais culturels modernes pour relire les événements à travers les grilles des sociétés méditerranéennes antiques : le système binaire honneur/honte, le patronage et les codes de pureté rituelle.
*   **`theo-histoire-reception`** (Wirkungsgeschichte) : Le sens comme sédimentation historique. Le skill ne cherchera pas l'intention originelle mais tracera comment l'interprétation a évolué au fil du temps (Pères de l'Église, liturgie, histoire de l'art).

## Installation

Vous avez besoin d'un assistant local compatible (Claude Desktop, OpenCode, Cursor, gemini-cli...).

**Si vous utilisez Claude Desktop :**
1. Clonez ce dépôt.
2. Zippez le dossier du skill qui vous intéresse (ex: `robert-alter-analyse.zip`).
3. Dans Claude : Co-Work > Customize > Competences > Ajouter (+).
4. Tapez `/robert-alter-analyse` dans le chat en donnant un texte (ex: Genèse 38).

**En ligne de commande :**
Copiez le dossier du skill directement là où votre outil les stocke (généralement `~/.claude/skills` ou `~/.gemini/skill`).

## Contribuer

Si vous voulez ajouter une nouvelle approche herméneutique, la règle d'or est de l'isoler. On cherche des méthodes claires et spécifiques, pas de nouvelles synthèses globales.

Faites un dossier avec un `SKILL.md`, sourcez votre méthodologie et vérifiez que vous avez le droit d'utiliser le contenu.
