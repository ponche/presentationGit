## Pourquoi Utiliser Plusieurs Branches dans Git ?

- **Travail Simultané** <!-- .element: class="fragment" -->
- **Isolation des Modifications** <!-- .element: class="fragment" -->
- **Expérimentation Sûre** <!-- .element: class="fragment" -->
- **Gestion des Conflits** <!-- .element: class="fragment" -->
- **Stabilité du Code** <!-- .element: class="fragment" -->

<div class="notes">
- **Travail Simultané** : Permet aux développeurs de travailler sur diverses fonctionnalités sans interférer avec le travail des autres.
- **Isolation des Modifications** : Les modifications peuvent être isolées dans des branches spécifiques, facilitant ainsi la gestion et le test des changements.
- **Expérimentation Sûre** : Permet d'expérimenter de nouvelles idées ou technologies sans affecter le code principal.
- **Gestion des Conflits** : Réduit les conflits de fusion en isolant les modifications dans des branches distinctes.
- **Stabilité du Code** : Permet de maintenir une branche stable (comme `main`) pour la production, tandis que les développements en cours se font sur d'autres branches.
</div>

---

## Structure des Branches

- **main** <!-- .element: class="fragment" -->
- **develop** <!-- .element: class="fragment" -->
- **feature/\<MyFeature\>** <!-- .element: class="fragment" -->
- **hotfix/\<correctifCritiqueEnProduction\>** <!-- .element: class="fragment" -->
- **bugfix/\<Correctif\>** <!-- .element: class="fragment" -->
- **ci/\<pipelineDevelop\>** <!-- .element: class="fragment" -->

<div class="notes">
- **main** : Branche de production, contenant le code stable et déployé.
- **develop** : Branche de développement protégée, utilisée pour intégrer les nouvelles fonctionnalités avant leur déploiement.
- **feature/\<MyFeature\>** : Branche dédiée au développement d'une nouvelle fonctionnalité.
- **hotfix/\<correctifCritiqueEnProduction\>** : Branche pour corriger rapidement les bugs critiques en production.
- **bugfix/\<Correctif\>** : Branche pour les corrections mineures.
- **ci/\<pipelineDevelop\>** : Branche pour les travaux liés aux pipelines CI/CD.
</div>

---

## Procédures et Conventions

- **Nommer les Branches** <!-- .element: class="fragment" -->
  Catégorie | Description | <!-- .element: class="fragment" -->
  |-----------|-------------|
  | hotfix | Résolution rapide des problèmes critiques. |
  | bugfix | Correction de bugs. |
  | feature | Ajout de fonctionnalités. |
  | wip | Travail en cours. |
  | draft | Branches de brouillon. |
  | ci | Ajout de Pipeline CI/CD. |
  | docs | Rédaction de documentation. |

<div class="notes">
- **Nommer les Branches** : Suivre une convention de nommage claire pour les branches (ex. : `feature/<nom-fonctionnalité>`).
- **hotfix** : Pour résoudre rapidement les problèmes critiques en production généralement avec une solution temporaire.
- **bugfix** : Pour corriger un bug.
- **feature** : Pour ajouter une fonctionnalité liée au projet.
- **wip** : Pour un travail en cours, indicateur pour dire bloquer.
- **draft** : Branches de brouillon, utilisées pour tester des choses.
- **ci** : Pour ajouter des Pipeline CI/CD.
- **docs** : Quand on rédige de la documentation, exemple : Docusaurus.
</div>

---

## Mise à Jour des Branches

- **Après une Pull Request (PR)** <!-- .element: class="fragment" -->
  - `git pull origin develop` <!-- .element: class="fragment" -->
  - Résoudre les conflits <!-- .element: class="fragment" -->

<div class="notes">
- **Après une Pull Request (PR)** : Mettez à jour votre branche locale par rapport à `develop` en utilisant `git pull origin develop`. Résolvez les éventuels conflits avant de fusionner.
</div>

---

## Enregistrement et Envoi des Modifications

1. **Ajouter les Modifications** <!-- .element: class="fragment" -->
   - `git add <fichier>` <!-- .element: class="fragment" -->
2. **Créer un Commit** <!-- .element: class="fragment" -->
   - `git commit -m "Message de commit"` <!-- .element: class="fragment" -->
3. **Envoyer les Modifications** <!-- .element: class="fragment" -->
   - `git push origin <nom-branche>` <!-- .element: class="fragment" -->

<div class="notes">
- **Ajouter les Modifications** : Utilisez `git add <fichier>` pour ajouter les fichiers modifiés au staging.
- **Créer un Commit** : Utilisez `git commit -m "Message de commit"` pour enregistrer les modifications avec un message clair.
- **Envoyer les Modifications** : Utilisez `git push origin <nom-branche>` pour envoyer les modifications vers le dépôt distant.
</div>

---

## La Pull Request (PR)

- **Création via GitHub** <!-- .element: class="fragment" -->
  - Sélectionner la branche source et la branche cible <!-- .element: class="fragment" -->
- **Description et Revue de Code** <!-- .element: class="fragment" -->
  - Rédiger une description détaillée <!-- .element: class="fragment" -->
  - Demander une revue de code <!-- .element: class="fragment" -->

<div class="notes">
- **Création via GitHub** : Allez sur l'interface GitHub et cliquez sur "New Pull Request". Sélectionnez la branche source et la branche cible.
- **Description et Revue de Code** : Rédigez une description détaillée des modifications apportées. Demandez une revue de code à vos collègues pour valider les changements.
</div>

---

## Conclusion

- **Résumé des Points Clés** <!-- .element: class="fragment" -->
- **Importance du Respect des Conventions** <!-- .element: class="fragment" -->

<div class="notes">
- **Résumé des Points Clés** : Suivre des conventions claires pour la création et la gestion des branches. Maintenir une communication efficace via des messages de commit et des descriptions de PR.
- **Importance du Respect des Conventions** : Respecter ces conventions est crucial pour un travail collaboratif efficace, réduisant les conflits et améliorant la qualité du code.
</div>
