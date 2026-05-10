# Documentation du Skill : `theo-rethorique-semitique`

Ce document explique le fonctionnement interne du skill, et plus particulièrement le rôle fondamental du système d'évaluation (dossier `evals/`), basé sur les conventions officielles du framework **Agent Skills** (notamment le `skill-creator`).

## 1. À quoi sert le dossier `evals/` ?

Le dossier `evals/` et son fichier central `evals.json` sont la clé de voûte de l'amélioration continue de cette compétence. Ils permettent d'appliquer les principes de l'ingénierie logicielle (*Test-Driven Development*) à l'ingénierie des prompts (Prompt Engineering) :

- **Créer un Benchmark (Référentiel de test)** : Constituer une bibliothèque de cas d'usage (péricopes courtes, paraboles, épîtres, conférences) pour évaluer la capacité de l'IA à appliquer rigoureusement la méthode de Roland Meynet sur différents niveaux de difficulté.
- **Garantir la Non-Régression** : Lorsqu'on modifie les instructions du `SKILL.md` (ex: pour qu'il comprenne mieux les "compositions elliptiques"), on s'assure via ces tests que cela ne dégrade pas sa capacité à analyser les figures de base (ex: les chiasmes).
- **Automatiser la Validation** : Permettre à l'écosystème d'outils d'évaluer objectivement si la sortie générée correspond aux attentes théoriques.

## 2. Structure du fichier `evals.json`

Le fichier `evals/evals.json` contient l'historique des cas de tests. Chaque évaluation respecte un schéma précis issu de la documentation `schemas.md` du skill-creator :

```json
{
  "skill_name": "theo-rethorique-semitique",
  "evals": [
    {
      "id": 1,
      "name": "nom-court-du-test",
      "prompt": "La requête exacte que ferait l'utilisateur (incluant souvent le texte source à analyser)...",
      "expected_output": "Les critères de réussite qualitatifs. (ex: 'Le modèle doit identifier une composition spéculaire de type A B / B\\' A\\'.')",
      "files": ["chemin/vers/un/fichier_optionnel.md"],
      "assertions": []
    }
  ]
}
```

## 3. Comment ajouter de nouveaux tests ?

Il est recommandé d'enrichir ce fichier à chaque fois qu'un nouveau cas complexe est validé ou lorsqu'une erreur récurrente est identifiée. 

Par exemple, après avoir généré la synthèse des notes de la conférence de R. Meynet, on peut ajouter ce test pour s'assurer que le modèle saura toujours traiter de longues transcriptions académiques :

```json
{
  "id": 6,
  "name": "synthese-conference-meynet",
  "prompt": "Applique le skill pour lire le fichier MEYNET_Roland_Come_ho_scoperto_la_retorica_biblica_2024.md et produire une synthèse académique exhaustive.",
  "expected_output": "Le modèle doit générer un document avec exactement les bonnes sections (MÉTADONNÉES, PLAN, POINTS CLÉS...) et identifier que la méthode retient les symétries globales (parallèles, spéculaires, concentriques, elliptiques) et partielles."
}
```

## 4. Le cycle de développement et d'utilisation (Workflow)

Dans le futur, lorsque vous voudrez améliorer le skill, vous (ou l'agent IA) utiliserez l'outillage standardisé de la manière suivante :

1. **Modification** : Édition des règles dans `SKILL.md`.
2. **Exécution des Evals** : L'outil lance en parallèle tous les prompts de `evals.json` avec la *nouvelle* version du skill ET avec l'*ancienne*.
3. **Notation (Grading)** : Un script compare les résultats générés avec le champ `expected_output` (Pass / Fail).
4. **Revue Visuelle (Viewer)** : L'outil `generate_review.py` produit une interface HTML locale permettant d'afficher côte à côte le prompt, l'ancien résultat, et le nouveau résultat.
5. **Validation Humaine** : L'utilisateur navigue dans l'interface, constate que les améliorations sont effectives sans avoir causé de régressions, et valide la nouvelle itération.

---
*Note: Garder et enrichir ce dossier `evals/` n'est donc pas optionnel pour un skill complexe ; c'est ce qui garantit sa stabilité méthodologique dans le temps.*
