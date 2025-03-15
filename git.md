## Introduction

Pour un travail d'équipe efficace, l'adoption de procédures et de conventions Git est essentielle :

- **Éviter les Malentendus** <!-- .element: class="fragment" -->
- **Historique Clair** <!-- .element: class="fragment" -->
- **Qualité et Maintenance du Code** <!-- .element: class="fragment" -->
- **Réduction des Conflits** <!-- .element: class="fragment" -->

Note: 
- Les conventions Git facilitent la communication et la compréhension entre les membres de l'équipe, réduisant ainsi les risques de confusion.
- Des messages de commit bien rédigés et des branches bien nommées permettent de maintenir un historique de projet compréhensible.
- Les procédures (comme les PR et les revues de code que nous aborderont plus tard) assurent que le code intégré est de haute qualité, facilitant ainsi la maintenance.
- En isolant les modifications dans des branches distinctes, les conflits de fusion sont minimisés, ce qui améliore l'efficacité du développement.

---

## Pourquoi Utiliser Plusieurs Branches dans Git ?

- **Travail Simultané** <!-- .element: class="fragment" -->
- **Isolation des Modifications** <!-- .element: class="fragment" -->
- **Expérimentation Sûre** <!-- .element: class="fragment" -->
- **Gestion des Conflits** <!-- .element: class="fragment" -->
- **Stabilité du Code** <!-- .element: class="fragment" -->

Note:
- **Travail Simultané** : Permet aux développeurs de travailler sur diverses fonctionnalités sans interférer avec le travail des autres.
- **Isolation des Modifications** : Les modifications peuvent être isolées dans des branches spécifiques, facilitant ainsi la gestion et le test des changements.
- **Expérimentation Sûre** : Permet d'expérimenter de nouvelles idées ou technologies sans affecter le code principal.
- **Gestion des Conflits** : Réduit les conflits de fusion en isolant les modifications dans des branches distinctes.
- **Stabilité du Code** : Permet de maintenir une branche stable (comme `main`) pour la production, tandis que les développements en cours se font sur d'autres branches.


--

## Structure des Branches

- **main** <!-- .element: class="fragment" -->
- **develop** <!-- .element: class="fragment" -->
- **feature/\<MyFeature\>** <!-- .element: class="fragment" -->
- **hotfix/\<correctifCritiqueEnProduction\>** <!-- .element: class="fragment" -->
- **bugfix/\<Correctif\>** <!-- .element: class="fragment" -->
- **ci/\<pipelineDevelop\>** <!-- .element: class="fragment" -->

Note:
- **main** : Branche de production, contenant le code stable et déployé.
- **develop** : Branche de développement protégée, utilisée pour intégrer les nouvelles fonctionnalités avant leur déploiement.
- **feature/\<MyFeature\>** : Branche dédiée au développement d'une nouvelle fonctionnalité.
- **hotfix/\<correctifCritiqueEnProduction\>** : Branche pour corriger rapidement les bugs critiques en production.
- **bugfix/\<Correctif\>** : Branche pour les corrections mineures.
- **ci/\<pipelineDevelop\>** : Branche pour les travaux liés aux pipelines CI/CD.

--


## Conventions de Commit

### Rédiger les Commits en Anglais

- **Langue Uniforme** 
- **Conventions de Commit** : Suivre les [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) 
Note:
- Tous les messages de commit doivent être rédigés en anglais pour éviter le franglais et assurer une compréhension uniforme au sein de l'équipe.
- convention pour structurer les messages de commit de manière cohérente et informative.

--

### Exemple de Conventional Commit

 - **Format** : `<type>(<scope>):<subject>`
 - **type** : Indique le type de changement (ex. : `feat`, `fix`, `docs`).
 - **scope** : Spécifie la partie du code affectée (optionnel).
 - **subject** : Décrit succinctement la modification.

-- 

  - **exemple** : test(login): add unit tests for login functionality



---

## Enregistrement et Envoi des Modifications

1. **Ajouter les Modifications** <!-- .element: class="fragment" -->
   - `git add <fichier>` <!-- .element: class="fragment" -->
2. **Créer un Commit** <!-- .element: class="fragment" -->
   - `git commit -m "Message de commit"` <!-- .element: class="fragment" -->
3. **Envoyer les Modifications** <!-- .element: class="fragment" -->
   - `git push origin <nom-branche>` <!-- .element: class="fragment" -->

Note:
- **Ajouter les Modifications** : Utilisez `git add <fichier>` pour ajouter les fichiers modifiés au staging.
- **Créer un Commit** : Utilisez `git commit -m "Message de commit"` pour enregistrer les modifications avec un message clair.
- **Envoyer les Modifications** : Utilisez `git push origin <nom-branche>` pour envoyer les modifications vers le dépôt distant.


---

## La Pull Request (PR)

- **Création via GitHub** <!-- .element: class="fragment" -->
  - Sélectionner la branche source et la branche cible <!-- .element: class="fragment" -->
- **Description et Revue de Code** <!-- .element: class="fragment" -->
  - Rédiger une description détaillée <!-- .element: class="fragment" -->
  - Demander une revue de code <!-- .element: class="fragment" -->


Note:
- **Création via GitHub** : Allez sur l'interface GitHub et cliquez sur "New Pull Request". Sélectionnez la branche source et la branche cible.
- **Description et Revue de Code** : Rédigez une description détaillée des modifications apportées. Demandez une revue de code à vos collègues pour valider les changements.

--

## Mise à Jour des Branches


  - `git pull origin develop` <!-- .element: class="fragment" -->
  - **Résoudre les conflits** <!-- .element: class="fragment" -->
  - **Après une Pull Request (PR) : on tire une nouvelle branche depuis la develop**<!-- .element: class="fragment" -->

Note:
- **Après une Pull Request (PR)** : Mettez à jour votre branche locale par rapport à `develop` en utilisant `git pull origin develop`. Résolvez les éventuels conflits avant de fusionner.

---

## Conclusion

- **Résumé des Points Clés** <!-- .element: class="fragment" -->
- **Importance du Respect des Conventions** <!-- .element: class="fragment" -->

Note:
- **Résumé des Points Clés** : Suivre des conventions claires pour la création et la gestion des branches. Maintenir une communication efficace via des messages de commit et des descriptions de PR.
- **Importance du Respect des Conventions** : Respecter ces conventions est crucial pour un travail collaboratif efficace, réduisant les conflits et améliorant la qualité du code.

