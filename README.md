# Skills Théologiques et Exégétiques pour Assistants IA

Les LLMs sont programmés pour être consensuels. Demandez-leur une analyse biblique, et ils vous recracheront souvent une synthèse tiède façon "Wikipédia", mélangeant dix traditions différentes pour ne fâcher personne.

Ce dépôt contient des "Skills" pour contrer ça. Il s'agit de dossiers d'instructions (au format [Agent Skills](https://agentskills.io/)) que vous pouvez charger dans votre assistant IA pour le forcer à utiliser une méthode de lecture spécifique et tranchée.

## Comment ça marche ?

Ce n'est pas juste un gros prompt. Le système repose sur la lecture à la demande : l'agent garde le fichier du skill sous le coude et le lit uniquement quand il en a besoin, ce qui évite de polluer sa mémoire le reste du temps.

Quand vous invoquez un skill, l'IA arrête d'être généraliste. Elle est obligée d'utiliser le vocabulaire, les concepts et la logique du courant théologique que vous avez choisi.

## Les Skills

### Disponibles

*   **[`robert-alter-analyse`](./robert-alter-analyse/)** : Analyse de l'Ancien Testament avec la grille littéraire de Robert Alter. Au lieu de faire de la théologie, l'agent va chercher les mots-guides (*Leitwort*), démonter les scènes-types et pointer l'ironie dramatique.

### En projet

Nous avons besoin d'autres grilles de lecture pour séparer les approches :
*   **Exégèse historico-critique** (sources, critique des formes)
*   **Herméneutique patristique** (Pères de l'Église, lecture allégorique)
*   **Herméneutique comparée** (l'évolution de l'interprétation)
*   **Théologie systématique** (thomisme, réformée...)
*   **[Herméneutique talmudique](https://en.wikipedia.org/wiki/Talmudical_hermeneutics)**

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
