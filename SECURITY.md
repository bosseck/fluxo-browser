# Politique de sécurité

FLUXO est un prototype expérimental et n'est pas encore recommandé pour un usage quotidien sensible.

## Signaler une vulnérabilité
N'ouvre pas d'issue publique contenant une preuve d'exploitation ou des détails permettant d'attaquer les utilisateurs. Utilise les **GitHub Security Advisories / Private vulnerability reporting** du dépôt si cette fonctionnalité est activée. À défaut, contacte les mainteneurs par un canal privé vérifié.

Dans ton signalement, indique la version, la plateforme, les étapes de reproduction et l'impact. Évite d'inclure des données personnelles ou des secrets.

## Engagement
Les signalements seront examinés de bonne foi. Aucun délai de correction n'est garanti pour le prototype. Ne divulgue pas publiquement la vulnérabilité avant coordination avec les mainteneurs.

## Principes techniques
- Isolation stricte du contenu web et des processus privilégiés.
- IPC limité et validé.
- Permissions refusées par défaut tant qu'une politique explicite n'existe pas.
- Mises à jour régulières d'Electron et Chromium.
- Aucun secret ni donnée de navigation sensible dans les journaux.
