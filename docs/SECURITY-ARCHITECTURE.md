# Architecture de sécurité — objectifs

## Frontière de confiance
Le contenu des sites web est non fiable. Il ne doit jamais accéder directement aux API Node/Electron, au système de fichiers ou aux secrets de l'application.

## Electron
- contextIsolation activé.
- nodeIntegration désactivé pour les pages distantes.
- sandbox activé lorsque possible.
- API preload minimale.
- IPC avec validation stricte de l'émetteur, du schéma et des autorisations.
- Navigation, popups, téléchargements et permissions contrôlés.
- CSP restrictive et dépendances maintenues à jour.

## Synchronisation E2EE
Le chiffrement et le déchiffrement doivent être réalisés sur les appareils. Le serveur ne reçoit que des données chiffrées. Le protocole, la rotation, la révocation des appareils et la récupération des clés nécessitent une conception formelle et un audit indépendant. Ne pas inventer de cryptographie.

## IA
Aucun envoi automatique de mots de passe, cookies, formulaires ou historique. Toute transmission de contenu doit être initiée par l'utilisateur et clairement présentée.
