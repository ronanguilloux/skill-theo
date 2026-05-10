# La Réécriture Visuelle (Rhétorique Biblique)

L'étape 3 de l'analyse rhétorique consiste à "réécrire" le texte, c'est-à-dire le disposer visuellement sur la page pour "donner à voir sa composition". Cette étape de mise en page stricte est la signature de la méthode de R. Meynet.

Pour générer cette réécriture en format Markdown, vous devez appliquer strictement les règles suivantes, qui sont l'adaptation de la méthode de Meynet aux contraintes de la syntaxe Markdown.

## Règle 1 : La Ligne et le Membre
- **Un membre par ligne :** Chaque membre du texte doit occuper *une seule et unique ligne*.
- Ne regroupez jamais plusieurs membres sur la même ligne (sauf règle exceptionnelle de "mise en facteur commun" pour de petits mots, mais en général : 1 membre = 1 ligne).
- N'ajoutez aucun mot et n'en supprimez aucun. N'utilisez **jamais** de points de suspension `...`.

## Règle 2 : Les Blocs, Segments et Morceaux
- **Séparation des Segments :** Les segments sont séparés par **une ligne blanche** (un saut de ligne). Les membres d'un même segment sont liés et n'ont pas de ligne blanche entre eux.
- **Séparation des Morceaux :** Les morceaux (regroupement de segments) sont séparés par **une ligne pointillée ou discontinue** (utilisez la balise Markdown `---` précédée et suivie d'une ligne blanche).
- **Encadrement des Parties/Passages :** En Markdown simple, si le texte est long, vous pouvez utiliser des blocs de citation (`> `) pour simuler les "cadres" ou filets de Meynet. Notez que rigoureusement, la *Partie* (et la sous-partie) est délimitée par deux filets.
- **Macro-structure (Séquences) :** À l'intérieur de la séquence (ou de la sous-séquence), les passages ne sont plus réécrits membre par membre. Ils sont **réécrits en prose** et disposés dans des cadres séparés par une ligne blanche. Dans une sous-séquence, les cadres sont contigus.

## Règle 3 : Alignements (Indentation)
L'alignement vertical permet de visualiser les structures spéculaires, concentriques ou parallèles.
- Utilisez des niveaux d'indentation (espaces) ou des listes non ordonnées Markdown pour créer des retraits.
- Les membres qui se correspondent dans l'architecture doivent avoir le même niveau d'indentation.
- Exemple pour un trimembre concentrique (A / x / A') :
  - `A membre`
    - `x membre central en retrait`
  - `A' membre`

## Règle 4 : Marqueurs d'architecture
Placez en préfixe de chaque ligne le repère d'architecture (la lettre) que vous avez trouvé à l'Étape 2, en le mettant entre crochets `[ ]`.
Exemple : `[A]`, `[B]`, `[x]`, `[B']`, `[A']`.

## Règle 5 : Typographie des correspondances (Rapports linguistiques)
Pour rendre les rapports évidents visuellement :
- **Identité :** Mettez en **gras** (avec `**`) les termes qui se correspondent par identité (répétitions du même mot, synonymes, mots de même racine).
- **Opposition :** Mettez en *italique* (avec `*`) les termes qui se correspondent par opposition (antonymes, actions contraires).
*(Note : Meynet utilise les petites capitales, le soulignement ou les couleurs, mais le gras et l'italique sont plus robustes en Markdown).*

- **Épure visuelle (Loi d'abstraction) :** Pour ne pas surcharger la lisibilité, vous ne mettez en forme (gras/italique) *que* les relations pertinentes au niveau que vous illustrez. Si vous réécrivez un Morceau, mettez en gras les rapports entre les Segments, *mais plus* les rapports internes aux membres de chaque segment.
- **Exception Synoptique :** Pour visualiser le parallélisme entre deux textes entiers (ex: deux évangiles), on utilise une présentation en colonnes parallèles.

## Exemple de rendu Markdown attendu

Pour la phrase "Car quiconque s'élève sera abaissé, et qui s'abaisse sera élevé" (Composition spéculaire A B / B' A').
À l'Étape 1, c'est un segment de 4 membres (ce qui est interdit), donc il se divise en 2 segments bimembres :

[A] Car quiconque **s'élève**
[B] sera *abaissé*,

[B'] et qui *s'abaisse*
[A'] sera **élevé**.

*Note : La ligne blanche sépare les deux segments bimembres. Le gras lie 'élève/élevé' (identité de racine), l'italique lie 'abaissé/abaisse'. L'inversion des concepts montre le chiasme.*