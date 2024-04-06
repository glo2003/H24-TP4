[← Retour](../README.md)

# Sécurité logicielle

De nos jours, il est pratiquement impossible de développer un logiciel sans utiliser des librairies externes. Ces morceaux de code pré-construits et (souvent) entièrement testés nous permettent de sauver du temps et d'éviter d'avoir à réinventer la roue. Par contre, pour chaque nouvelle dépendance rattachée à notre produit, une porte s'ouvre vers des vulnérabilités.

## Analyse de sécurité

Afin de garantir que votre code repose sur des librairies logicielles sécuritaires, lier votre repository à un outil d'analyse de la sécurité du code. Cet outil doit :

- Analyser les dépendances ainsi que leurs failles de sécurité
  - Dans le cas d'une faille trouvée, lier vers l'analyse de la vulnérabilité CVE ou proposer une version qui corrige la situation
- Analyser les [dépendances transitives](https://semgrep.dev/blog/2023/transitive-supply-chain-vulnerabilities) de vos dépendances directes
- Analyser votre propre code pour trouver des utilisations non sécuritaires
- S'exécuter à chaque commit, au moins sur votre branche principale (idéalement sur toutes les branches)

Montrez des captures d'écran des analyses sommaires et détaillées dans votre fichier d'exercice. On ne vous demande pas de régler les problèmes identifiés.

## Vers des pratiques plus sécures

Trouvez 3 pratiques à intégrer dans un processus de développement logiciel qui permettent de réduire les risques de vulnérabilités. Pour vous aider, voici quelques termes pouvant vous être utiles dans vos recherches:

- DevSecOps
- SSDLC
- Software Supply Chain
- CI/CD/CS
