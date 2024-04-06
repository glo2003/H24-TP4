[← Retour](../README.md)

# Outils de métrique

Bien que des [outils d'analyses](./analysis.md) et des tests aient été mis en place, des bogues peuvent tout de même s'introduire. De plus, en pratique, les applications sont exécutées sur des serveurs distants pour lesquels l'accès aux logs et aux débogueurs n'est pas toujours possible. Afin de remédier à ce problème, vous devez mettre en place l'outil Sentry, qui permet de rapporter et de notifier les erreurs en production.

**Critères**

1. Doit rapporter **toutes** les erreurs de votre code, sauf celles générées par Jersey (ex: 404 de route non-existante). L'utilisation d'un *exception mapper* pourrait grandement vous aider.
2. Utilisez la variable d'environnement `SENTRY_DSN` pour la valeur du DSN, puisqu'il s'agit d'une **donnée sensible**.
3. Ne **pas** utiliser le plugin `sentry-maven-plugin`, cela risque de bloquer la correction automatique (besoin d'une clée d'API). Utilisez plutôt la dépendance de code `sentry-java`.

Incluez des captures d'écran de rapports de bogues sommaires et détaillées dans votre fichier d'exercice. On ne vous demande pas de régler les problèmes identifiés, sauf s'ils sont des critères d'évaluations demandés dans les énoncés.
