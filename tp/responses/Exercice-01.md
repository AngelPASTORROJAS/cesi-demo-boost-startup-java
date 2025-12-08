## 🤔 Questions de Compréhension

1. **Quelle est la différence entre `push` et `pull_request` ?**
Le `push`, c'est lorsqu'on pousse un commit dans une branch.
La `pull_request`, c'est lorsqu'on pousse un ensemble de commit lié une branch vers une autre branch. Elle est utilisé pour voir les différences qui seront apporté dans la branch où la demande de pull request est faite.

2. **À quoi sert `workflow_dispatch` ?**
workflow_dispatch sert à lancer un workflow GitHub Actions « à la main », un peu comme si tu appuyais sur un bouton “Exécuter ce pipeline maintenant”, éventuellement avec des paramètres que tu remplis dans un petit formulaire.

3. **Pourquoi avons-nous besoin de `security-events: write` ?**
`security-events: write` permet au GITHUB_TOKEN d'un workflow GitHub Actions de créer et modifier des événements de sécurité (comme des alertes de vulnérabilités ou des SBOM), cela donne aussi accès à la lecture de tous les événements existants ce qui pose un risque de fuite d'infos sensibles. Ceci nous sert à faire des scan.

4. **Que se passe-t-il si on commente `schedule:` ?**
Si on commente shedule on désactive les processus automatisé à date.
