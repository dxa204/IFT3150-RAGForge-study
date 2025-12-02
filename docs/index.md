# Extension de ChainForge avec des capacités de génération augmentée par récupération (RAG)

> **Thèmes**: RAG, UX
> **Superviseur**: Ian Arawjo

## Équipe
> **Etudiant**: Derin Akay

## Description du projet

### Contexte
ChainForge est un outil de prototypage visuel permettant d’interroger et de comparer plusieurs LLMs en temps réel. Pour de nombreuses applications avancées — assistants de connaissance, outils de recherche, chatbots spécialisés — il est nécessaire d’enrichir les modèles avec des informations externes, actualisées ou spécialisées via le RAG.

### Problématique ou motivations
Malgré ses atouts, ChainForge offre peu de support natif pour le RAG. Cette lacune limite la conception et l’évaluation de systèmes fondés sur des connaissances, où l’on doit combiner comparaison multi-LLM et récupération dynamique d’informations. Il manque une intégration fluide du pipeline RAG (téléversement, segmentation, indexation, récupération, injection de contexte) et des moyens d’analyser son impact sur les sorties des LLMs.

### Proposition et objectifs
Nous proposons d’étendre **RAGForge** (prototype basé sur ChainForge) afin d’offrir un support **complet** du RAG tout en préservant son flux unique de comparaison multi-LLM. Les utilisateurs pourront téléverser et traiter des documents, les segmenter automatiquement, récupérer des contextes pertinents et enrichir les réponses des modèles. L’interface visuelle permettra de chaîner des étapes RAG avec plusieurs requêtes LLM, d’observer les résultats intermédiaires et de comparer les sorties dans un même contexte.

**Objectifs concrets :**
- Intégrer le pipeline RAG de bout en bout (uploading → chunking → retrieval → (reranking) → output).
- Conserver et améliorer le flux de **comparaison multi-LLM** avec contexte partagé.
- Exposer les **résultats intermédiaires** pour la traçabilité et le debug.
- Mener une **étude utilisateur** pour recueillir des retours sur l’ergonomie, la fiabilité et la performance, et orienter les améliorations futures.

## Échéancier

!!! info
    Le suivi complet est disponible dans la page [Suivi de projet](suivi.md).

| Jalon (*Milestone*)            | Date prévue   | Livrable                            | Statut      |
|--------------------------------|---------------|-------------------------------------|-------------|
| Ouverture de projet            | 1 septembre   | Proposition de projet               | ✅ Terminé  |
| Commence l'authorisation sur Nagano        | 16 septembre  | Formulaire                  | ✅ Terminé  |
| Terminer RAGForge et faire la lancement                    | 13 Novembre  | Interface fonctionnel         | ⏳ À venir  |
| Faire l'etude utilisateur                    | Novembre-Decembre  | Le rapport final             | ✅ Terminé  |
| Presentation Orale                   | 11 Decembre  | Presentation de la projet fini         | ⏳ À venir  |
| Soumettre le rapport final | 19 Decembre | Le rapport final | ⏳ À venir|