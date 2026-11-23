# Architecture cible

## Windows
Electron + Chromium + React + TypeScript. Electron gère la fenêtre et les capacités système ; Chromium affiche les pages. Le contenu distant doit rester séparé du renderer privilégié de l'interface. Préférer WebContentsView pour les vues web contrôlées.

Mesures minimales : contextIsolation, nodeIntegration désactivé pour le contenu distant, sandbox, CSP stricte, validation IPC, contrôle de navigation, fenêtres, permissions et téléchargements.

## Android
Architecture Android native à définir autour d'un moteur de navigateur approprié (par exemple GeckoView), avec Kotlin pour l'intégration système. Electron n'est pas un runtime Android. La compatibilité des extensions et des fonctions réseau doit être validée avant toute promesse produit.

## Services communs
Partager les contrats, modèles, paramètres, règles de confidentialité et protocole de synchronisation, sans forcer le partage du moteur de rendu.

## Données
Stockage local chiffré lorsque nécessaire. Backend facultatif ; les fonctions essentielles doivent rester accessibles sans compte.
