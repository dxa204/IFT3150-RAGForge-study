# Suivi de projet

## Semaine 1

??? note "Mettre en place l'environnement"
    - [x] Lorem ipsum dolor sit amet, consectetur adipiscing elit
    - [ ] Vestibulum convallis sit amet nisi a tincidunt
        * [x] In hac habitasse platea dictumst
        * [x] In scelerisque nibh non dolor mollis congue sed et metus
        * [ ] Praesent sed risus massa
    - [ ] Aenean pretium efficitur erat, donec pharetra, ligula non scelerisque

!!! info "Notes"
    - Il est possible que nous révisions les exigences après le prototypage

!!! warning "Difficultés rencontrées"
    - Le plugin Mermaid n'était pas reconnu : confusion entre `mkdocs-mermaid2-plugin` (pip) et `mermaid2` (plugin name)
        - Résolu après nettoyage et configuration correcte dans `mkdocs.yml`

!!! abstract "Prochaines étapes"
    - Démarrer l’analyse du problème
    - Créer la structure de `etudes_preliminaires.md`

---

## Semaine 2
??? note "Procédure éthique"
    - [x] Remplissage et dépôt du formulaire d’éthique **F11-CERSES-31826** sur la plateforme **Nagano**
    - [x] Soumission du projet **2025-7301 : RAGFORGE-ÉTUDE-UTILISATEUR**
    - [x] Vérification de la conformité aux exigences éthiques de l’Université

!!! info "Notes"
    - Cette étape est essentielle pour garantir que la collecte de données des utilisateurs se déroule dans le respect des normes éthiques et de la protection institutionnelle.
    - Le projet a été officiellement **déposé le 6 octobre 2025 à 09h50**.

!!! warning "Difficultés rencontrées"
    - Quelques incertitudes initiales concernant la catégorie du projet (évaluation complète ou simple déclaration).
    - Le processus de validation sur Nagano exige plusieurs vérifications administratives.

!!! abstract "Prochaines étapes"
    - Attendre la réponse du comité d’éthique
    - Planifier la phase de tests utilisateurs après approbation


## Semaine 3
??? note "Mises à jour techniques"
    - [x] Introduction de **CustomChunkerProtocol** et **CustomRetrieverProtocol** pour formaliser les interfaces appelables
    - [x] Mise à jour de **protocol.py** et **ProviderRegistry** afin d’enregistrer les deux types via une union
    - [x] Création d’implémentations d’exemple pour les tests :
        * `paragraph_chunker.py`
        * `levenshtein_retriever.py`

!!! info "Notes"
    - La définition explicite des protocoles permet une meilleure extensibilité et une interface plus propre pour les développeurs.
    - Les exemples créés servent de référence pour tester la compatibilité et la cohérence entre les modules de chunking et de retrieval.

!!! warning "Difficultés rencontrées"
    - Quelques ajustements nécessaires dans la logique d’union pour éviter des collisions de type.
    - Vérification requise du comportement des implémentations personnalisées lors de l’enregistrement multiple.

!!! abstract "Prochaines étapes"
    - Finaliser les tests unitaires pour les protocoles personnalisés
    - Intégrer la documentation technique sur les nouvelles interfaces
    - Préparer un exemple plus complexe combinant chunking et retrieval

## Semaine 4
??? note "Mises à jour techniques"
    - [x] **Custom Providers** : correction de la logique du bouton de paramètres pour les fournisseurs personnalisés (garantit une gestion cohérente du schéma et du comportement de l’interface)
    - [x] **Example Flows** : ajout de deux nouveaux flux d’exemple **RAG** pour illustrer les pipelines à récupération augmentée
    - [x] **Chunking** : introduction d’une méthode de segmentation basée sur les en-têtes **Markdown** pour une meilleure découpe des documents

!!! info "Notes"
    - Les nouveaux flux RAG servent de référence claire pour la mise en œuvre de pipelines hybrides.
    - Le découpage par en-têtes Markdown améliore la lisibilité et la précision du traitement des documents.
    - L’uniformisation de la logique des fournisseurs personnalisés réduit les erreurs liées à la configuration.

!!! warning "Difficultés rencontrées"
    - Quelques incohérences dans la gestion des schémas lors du changement de fournisseur.
    - Ajustements requis pour rendre la segmentation Markdown compatible avec d’anciens formats de documents.

!!! abstract "Prochaines étapes"
    - Tester les nouveaux flux RAG sur différents cas d’utilisation
    - Documenter la nouvelle méthode de chunking et ses avantages
    - Vérifier la stabilité du module de fournisseurs personnalisés après correction


## Semaine 5
??? note "Mises à jour techniques"
    - [x] Mise à jour de l’interface du **Chunk Node** : le menu des méthodes se replie automatiquement et le nœud reflète désormais visuellement le style du **Prompt Node**
    - [x] Modification de la logique du **Stopword Chunker** : renommage de `TextTilingTokenizer` en `Stopword Chunker`
    - [x] Les mots vides (*stopwords*) sont désormais gérés en interne, plutôt qu’importés depuis une ressource externe
    - [x] Suppression du **Neural Chunker**

!!! info "Notes"
    - Ces changements visent à simplifier la maintenance et améliorer la cohérence visuelle entre les différents nœuds.
    - L’intégration des stopwords en interne permet de réduire les dépendances externes et d’accélérer le traitement.

!!! warning "Difficultés rencontrées"
    - Ajustements nécessaires pour s’assurer que la suppression du **Neural Chunker** n’affecte pas la compatibilité des anciens flux.
    - Quelques problèmes de nommage à corriger après le renommage de `TextTilingTokenizer`.

!!! abstract "Prochaines étapes"
    - Mettre à jour la documentation pour refléter la nouvelle dénomination du **Stopword Chunker**
    - Vérifier la compatibilité descendante des flux existants
    - Démarrer les tests de cohérence sur l’interface mise à jour du **Chunk Node**


## Semaine 6
??? note "Mises à jour techniques"
    - [x] Correction de l’interface du **Retrieval Node** pour refléter l’apparence du **Chunk Node** et du **Prompt Node**
    - [x] Résolution d’un petit problème de chemin pour les flux d’exemple avec l’extension `.cfzip`
    - [x] Correction d’une pollution des **métavariables** dans l’inspecteur des nœuds de récupération et de requête
    - [x] Amélioration du **CSS** du **Chunk Node**
    - [x] Correction d’un léger problème de nommage dans deux fichiers de flux d’exemple

!!! info "Notes"
    - L’uniformisation de l’interface entre les différents nœuds améliore la cohérence visuelle et la navigation dans l’outil.
    - Le nettoyage des métavariables simplifie le débogage et réduit la confusion lors de l’inspection des flux.

!!! warning "Difficultés rencontrées"
    - Quelques ajustements CSS ont été nécessaires pour préserver la réactivité du design sur différentes tailles d’écran.
    - La compatibilité entre les fichiers `.cfzip` et la nouvelle logique d’importation a demandé des tests supplémentaires.

!!! abstract "Prochaines étapes"
    - Finaliser les tests d’intégration entre les nœuds de récupération et de requête
    - Vérifier la stabilité du CSS après intégration du thème unifié
    - Mettre à jour la documentation interne sur la structure des flux `.cfzip`


## Semaine 7
??? note "Mises à jour techniques"
    - [x] Implémentation de la fonctionnalité de fusion pour les méthodes de recherche (RRF et Moyenne pondérée)
    - [x] Correction d’un bug de duplication de méthode dans les nœuds de découpage et de recherche — les doublons s’affichent désormais avec des indices (2), (3), etc.
    - [x] Ajout d’un exemple de flux à propos d’un livre
    - [x] Modification du flux d’exemple `chainforge-docs` pour inclure les évaluateurs RAGAS
    - [x] Déplacement de `chunkMethod` des métavariables vers les variables normales afin qu’il apparaisse comme colonne dans l’inspecteur

!!! info "Notes"
    - Les nouvelles fonctionnalités de fusion améliorent la flexibilité des méthodes de récupération.
    - La visibilité accrue des variables facilite l’inspection et le débogage.

!!! warning "Difficultés rencontrées"
    - Quelques ajustements nécessaires pour assurer la compatibilité entre les nœuds de récupération et le nouvel affichage des variables.

!!! abstract "Prochaines étapes"
    - Finaliser les tests sur les méthodes de fusion
    - Documenter les changements dans la section technique du rapport

## Semaine 8
??? note "Travail réalisé"
    - [x] Peaufiner la fonctionnalité **Fusion**
    - [x] Réduire la taille des fichiers des **flux d’exemple**
    - [x] Créer le **modal de Fusion** avec **RJSF**
    - [x] Amélioration de l’interface utilisateur (**UI**) du module Fusion pour un comportement plus fluide et homogène
    - [x] Nettoyage du code et ajustement de la logique de gestion des schémas JSON dans le modal
    - [x] Réception de la réponse du comité d’éthique : **aucune approbation n’est nécessaire** pour notre étude utilisateur

!!! info "Notes"
    - **RJSF = *React JSONSchema Form*** : permet de définir un modal basé sur des schémas pour configurer la fusion.
    - La réduction de la taille des fichiers contribue à un **chargement plus rapide** des exemples et à une **meilleure performance générale**.
    - L’étude utilisateur reste **conforme aux exigences éthiques de l’Université**, sans nécessiter une révision complète.
    - Les ajustements apportés au modal améliorent la **cohérence visuelle** et la **stabilité de la configuration**.

!!! warning "Difficultés rencontrées"
    - Harmonisation des schémas JSON entre RJSF et la logique existante de Fusion.
    - Gestion des dépendances qui gonflaient le bundle lors de la création du modal.
    - Tests nécessaires pour s’assurer que la réduction de taille n’affecte pas les flux complexes.

!!! abstract "Prochaines étapes"
    - Écrire des tests **UX/QA** pour le modal (validation de schéma, états d’erreur)
    - Mesurer et consigner les **gains de taille** (avant/après) des flux d’exemple
    - Mettre à jour la **documentation utilisateur** pour la configuration de Fusion via le modal
    - Démarrer la **préparation logistique de l’étude utilisateur**, maintenant validée sur le plan éthique


## Semaine 9

## Semaine 10

## Semaine 11

## Semaine 12

## Semaine 13
