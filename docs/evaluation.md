# Évaluation

## Plan de test

- Format : Sessions de 60 minutes maximum, menées en virtuel (Zoom) ou en présentiel.
- Tâche : Les participants devaient construire un chatbot RAG minimal en modifiant un flux d'exemple préexistant. Cela impliquait la configuration des nœuds de téléversement, de chunking (encouragés à tester plusieurs méthodes) et de récupération.
- Procédure : Introduction au concept → Tâche structurée de construction → Expérimentation avec la fusion/reranking → Entrevue post-tâche.

## Critères d'évaluation

- Succès de l'exécution : Capacité à exécuter le pipeline de bout en bout et à obtenir des réponses logiques.
- Utilisabilité (UX) : Facilité de construction, clarté des paramètres RAG, expérience de téléversement et sentiment de contrôle sur le système

## Analyse des résultats

- Retour d'information système : Les utilisateurs ont exprimé un fort besoin de feedback visuel, notamment une barre de progression dans le nœud de récupération, des indicateurs de succès (coche verte) et l'affichage du temps d'exécution réel (ex: 50ms).
- Aide à la navigation : Il manque des infobulles explicatives ("?") sur les nœuds et des estimations de temps pour les méthodes longues (comme les vector stores) pour guider les choix de l'utilisateur.
- Ergonomie des nœuds : Le nœud "Join" a été jugé confus ; les utilisateurs préfèrent que le nœud "Prompt" accepte plusieurs entrées directement. Des fonctionnalités de contrôle (bouton pause) sont également requises pour les nœuds de récupération et de chunking.