# Limitations & Roadmap

Voici les problèmes identifiés dans l'architecture actuelle. Si vous contribuez, ce sont d'excellentes `good first issues`.

| # | Problème détecté | Impact | Label suggéré |
|---|---|---|---|
| 1 | **Blocage du nœud Merge** | Si un email est un doublon, la branche s'arrête. Le nœud Merge (en mode `combineAll`) attendra éternellement l'entrée "Accusé de réception", bloquant l'évaluation IA. | `bug`, `refactor` |

| 2 | **Ciblage de l'email candidat** | Le nœud Accusé de réception utilise `$('Gmail Trigger').item.json...`. En cas de polling de multiples emails simultanément, cela peut envoyer les accusés à la mauvaise personne. | `bug`, `help wanted` |
| 3 | **Expressions mal formatées** | Présence de `=={{...}}` au lieu de `={{...}}` classiques dans Text Classifier et Update Record. | `refactor` |
| 4 | **Gestion des PDF sans texte pur** | Si le CV du candidat est une image scannée, l'IA ne lira aucun texte. Besoin d'un nœud OCR. | `enhancement` |
