# Études préliminaires

## Analyse du problème

- Limitation actuelle : Bien que ChainForge soit efficace pour comparer plusieurs LLMs, il manque de support natif pour le RAG (Retrieval-Augmented Generation).

- Impact : Cette lacune empêche la conception et l'évaluation de systèmes fondés sur des connaissances externes, rendant difficile l'injection de contexte dynamique et l'analyse de son impact sur les réponses des modèles.

## Exigences

- Fonctionnelles : Le système doit permettre le téléversement de documents, la segmentation automatique (chunking), l'indexation, la récupération de contexte (retrieval) et l'injection de ce contexte dans les prompts.

- Non-fonctionnelles : L'outil doit préserver le flux visuel unique de comparaison multi-LLM de ChainForge et offrir une traçabilité des résultats intermédiaires pour le débogage.

## Recherche de solutions

- Solution retenue : Extension de l'outil existant ChainForge pour créer "RAGForge".

- Justification : Plutôt que de créer un nouvel outil à partir de zéro, étendre ChainForge permet de bénéficier de son interface de prototypage visuel existante tout en y ajoutant les étapes manquantes du pipeline RAG.

