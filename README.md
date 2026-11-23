# FLUXO Browser

**FLUXO** est un projet de navigateur web multiplateforme en développement, avec une interface sombre et premium.

> **État actuel : prototype expérimental 0.1.0 — Windows uniquement.**
> Ce dépôt ne représente pas encore une version stable, sécurisée pour un usage quotidien ou prête à être distribuée au grand public.

## Vision

Construire un navigateur axé sur la confidentialité, avec des applications Windows et Android, un mode hors ligne, un bloqueur de publicités et de traqueurs, un coffre de mots de passe, un lecteur PDF, des captures d'écran, des extensions compatibles et des fonctions d'assistance IA déclenchées par l'utilisateur.

## État du projet

Le prototype Windows prévu utilise Electron, Chromium, React et TypeScript. Les fonctionnalités avancées (synchronisation E2EE, Android, coffre de mots de passe de production, blocage complet des traqueurs, extensions, assistant IA et mises à jour signées) ne sont pas encore implémentées ni garanties.

## Technologies prévues

| Plateforme | Technologies |
|---|---|
| Windows | Electron, Chromium, React, TypeScript |
| Android | Kotlin, Jetpack Compose, GeckoView (architecture à confirmer) |
| Données locales | SQLite |
| Backend facultatif | Node.js, TypeScript, PostgreSQL |
| Synchronisation | Protocole E2EE à spécifier et auditer |

Android ne sera pas exécuté dans Electron : Electron n'est pas un runtime Android. L'architecture Android doit utiliser une pile native adaptée au moteur de navigateur retenu.

## Principes de confidentialité

- Les fonctions essentielles doivent rester utilisables sans compte.
- La synchronisation sera facultative et désactivée par défaut.
- Les données synchronisées seront chiffrées côté client avant envoi.
- Le serveur ne devra pas posséder les clés de déchiffrement.
- L'assistant IA ne devra transmettre du contenu que sur action explicite de l'utilisateur.
- Aucun mot de passe, cookie ou historique ne sera envoyé automatiquement à un service IA.

## Développement

Le code source du prototype et les instructions de démarrage seront ajoutés au dépôt dans une prochaine mise à jour. Les contributions doivent suivre les consignes de sécurité et de contribution du projet.

## Licence

Licence prévue : **GNU Affero General Public License v3.0 — AGPL-3.0-only**. Le texte officiel complet de la licence doit être ajouté à la racine avant de considérer la publication du code comme complète. Voir [LICENSE-SETUP.md](LICENSE-SETUP.md).

## Sécurité

Ne signale pas une vulnérabilité exploitable dans une issue publique. Consulte [SECURITY.md](SECURITY.md) lorsqu'il sera présent. FLUXO est expérimental : ne l'utilise pas pour protéger des secrets ou des mots de passe importants.
