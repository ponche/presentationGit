 ## Pourquoi Utiliser Plusieurs Branches dans Git ?

Utiliser plusieurs branches dans Git offre de nombreux avantages par rapport au travail sur une seule branche :

- **Travail Simultané sur Différentes Fonctionnalités** : Permet aux développeurs de travailler sur diverses fonctionnalités sans interférer avec le travail des autres.
- **Isolation des Modifications** : Les modifications peuvent être isolées dans des branches spécifiques, facilitant ainsi la gestion et le test des changements.
- **Expérimentation Sûre** : Permet d'expérimenter de nouvelles idées ou technologies sans affecter le code principal.
- **Gestion des Conflits** : Réduit les conflits de fusion en isolant les modifications dans des branches distinctes.
- **Stabilité du Code** : Permet de maintenir une branche stable (comme `main`) pour la production, tandis que les développements en cours se font sur d'autres branches.



## Structure des Branches

- **main** : Branche de production, contenant le code stable et déployé. <!-- .element: class="fragment" -->
- **develop** : Branche de développement protégée, utilisée pour intégrer les nouvelles fonctionnalités avant leur déploiement. <!-- .element: class="fragment" -->
- **feature/<MyFeature>** : Branche dédiée au développement d'une nouvelle fonctionnalité. <!-- .element: class="fragment" -->
- **hotfix/<correctifCritiqueEnProduction>** : Branche pour corriger rapidement les bugs critiques en production. <!-- .element: class="fragment" -->
- **bugfix/<Correctif>** : Branche pour les corrections mineures. <!-- .element: class="fragment" -->
- **ci/<pipelineDevelop>** : Branche pour les travaux liés aux pipelines CI/CD. <!-- .element: class="fragment" -->


## Procédures et Conventions

- **Bien nommer ses branches: tableau recapitulatif** : Suivre une convention de nommage claire pour les branches (ex. : `feature/<nom-fonctionnalité>`).

| Catégorie |  Description|
|--|--|
| hotfix | Pour résoudre rapidement les problèmes critiques en production généralement avec une solution temporaire | <!-- .element: class="fragment" -->
| bugfig | pour corriger un bug | <!-- .element: class="fragment" -->
| feature | Pour ajouter une fonctionnalité liée au projet | <!-- .element: class="fragment" -->
| wip | pour un travail en cours, indicateur pour dire bloquer | <!-- .element: class="fragment" -->
| draft | branches de brouillon , utilisées pour test des choses. | <!-- .element: class="fragment" -->
| ci | pour ajouter des Pipeline CI/CD | <!-- .element: class="fragment" -->
| docs | quand on rédige de la documentation, exemple: Docusaurus | <!-- .element: class="fragment" -->




## Mise à Jour des Branches

- **Après une Pull Request (PR)** :
  - Mettez à jour votre branche locale par rapport à `develop` en utilisant `git pull origin develop`.
  - Résolvez les éventuels conflits avant de fusionner.


## Enregistrement et Envoi des Modifications

1. **Ajouter les Modifications** :
   - Utilisez `git add <fichier>` pour ajouter les fichiers modifiés au staging.
2. **Créer un Commit** :
   - Utilisez `git commit -m "Message de commit"` pour enregistrer les modifications avec un message clair.
3. **Envoyer les Modifications** :
   - Utilisez `git push origin <nom-branche>` pour envoyer les modifications vers le dépôt distant.


## La Pull Request (PR)

- **Création via GitHub** :
  - Allez sur l'interface GitHub et cliquez sur "New Pull Request".
  - Sélectionnez la branche source et la branche cible.
- **Description et Revue de Code** :
  - Rédigez une description détaillée des modifications apportées.
  - Demandez une revue de code à vos collègues pour valider les changements.



## Conclusion

- **Résumé des Points Clés** :
  - Suivre des conventions claires pour la création et la gestion des branches.
  - Maintenir une communication efficace via des messages de commit et des descriptions de PR.
- **Importance du Respect des Conventions** :
  - Respecter ces conventions est crucial pour un travail collaboratif efficace, réduisant les conflits et améliorant 

 # Importance des Procédures et Conventions Git

## Introduction

Pour un travail d'équipe efficace, l'adoption de procédures et de conventions Git est essentielle :

- **Éviter les Malentendus** : Les conventions Git facilitent la communication et la compréhension entre les membres de l'équipe, réduisant ainsi les risques de confusion.
- **Historique Clair** : Des messages de commit bien rédigés et des branches bien nommées permettent de maintenir un historique de projet compréhensible.
- **Qualité et Maintenance du Code** : Les procédures (comme les PR et les revues de code que nous aborderont plus tard) assurent que le code intégré est de haute qualité, facilitant ainsi la maintenance.
- **Réduction des Conflits** : En isolant les modifications dans des branches distinctes, les conflits de fusion sont minimisés, ce qui améliore l'efficacité du développement.


## Conventions de Commit

### Rédiger les Commits en Anglais

- **Langue Uniforme** : Tous les messages de commit doivent être rédigés en anglais pour éviter le franglais et assurer une compréhension uniforme au sein de l'équipe.
- **Conventions de Commit** : Suivre les [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) pour structurer les messages de commit de manière cohérente et informative.




### Exemple de Conventional Commit

- **Format** : `<type>(<scope>):<subject>`
  - **type** : Indique le type de changement (ex. : `feat`, `fix`, `docs`).
   - **scope** : Spécifie la partie du code affectée (optionnel).
  - **subject** : Décrit succinctement la modification.
  
  - **exemple** : test(login): add unit tests for login functionality



## Structure des Branches

| **Branche**               | **Description**                                                                                                 |
| ------------------------- | --------------------------------------------------------------------------------------------------------------- |
| **main**                  | Branche de production contenant le code stable et déployé.                                                      |
| **develop**               | Branche de développement protégée, utilisée pour intégrer les nouvelles fonctionnalités avant leur déploiement. |
| **feature/\<MyFeature\>** | Branche dédiée au développement d'une nouvelle fonctionnalité.                                                  |

