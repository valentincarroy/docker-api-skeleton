# Convention de nommage des commits git

Basé sur la convention définie par [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

## Structure du message

Le message de commit doit être structuré de cette manière :

```
<type>(optionnel <scope>): <description>
<LIGNE VIDE>
optionnel <commentaire>
<LIGNE VIDE>
optionnel <BREAKING CHANGE>
```

## Types de commit

- feat: ajoute une nouvelle fonctionnalité
- fix: corrige un bug
- chore: changement n'impactant pas l'utilisateur qui n'est pas une fonctionnalité ou un bug fix
- docs: modification de la documentation
- style: amélioration visuelle du code (indentation, saut de ligne...)
- perf: amélioration des performances
- refactor: remaniement du code
- test: écriture, modification, suppression ou remaniement de tests

## Scopes

Principaux scopes disponible

- api
- front

## Breaking changes

Les breaking changes sont des changements qui nécessitent une action supplémentaire. Ils doivent être indiqués par `!:` avant la description du commit.
Les actions à réalisés sont décrits en dessous du commentaire avec `BREAKING CHANGE:`