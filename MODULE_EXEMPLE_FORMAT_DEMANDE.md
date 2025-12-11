# EXEMPLE DE MODULE RESTRUCTURÉ - FORMAT COMPLET

Ce fichier démontre le format standard que CHAQUE module du curriculum POKÉOS devrait suivre, selon les exigences spécifiées.

---

# MODULE 1.3 : Hash Tables & Advanced Data Structures

## Durée : 70h | XP : 1000 | Semaines 5-6

---

## Sous-module 1.3.1 : Hash Tables Fondamentales (35h)

### 1.3.1.a : Introduction aux Hash Tables

#### Ressources Universitaires (Théorie Fondamentale)

| Source | Contenu | Lien/Référence |
|--------|---------|----------------|
| **MIT 6.006** | Lecture 8: Hashing with Chaining | [MIT OCW](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-spring-2020/) |
| **MIT 6.006** | Lecture 9: Open Addressing, Cryptographic Hashing | MIT OCW |
| **Stanford CS161** | Lecture 10: Hash Tables | [Stanford Online](https://web.stanford.edu/class/cs161/) |
| **Princeton Algorithms** | Week 4: Hash Tables | [Coursera](https://www.coursera.org/learn/algorithms-part1) |
| **CLRS** | Chapter 11: Hash Tables (pp. 253-285) | ISBN: 978-0262033848 |
| **Algorithms 4th Ed** | Section 3.4: Hash Tables | Sedgewick & Wayne |

#### Vidéos YouTube (Storytelling & Culture G)

| Chaîne | Vidéo | Durée | Ce que vous apprendrez |
|--------|-------|-------|------------------------|
| **Computerphile** | "Hash Tables" | 12 min | Intuition visuelle du concept |
| **Computerphile** | "Hashing Algorithms and Security" | 8 min | Contexte sécurité |
| **Abdul Bari** | "Hashing | Hash Table | Hash Function" | 18 min | Explication détaillée avec exemples |
| **MIT OpenCourseWare** | "6.006 Lecture 8: Hashing with Chaining" | 1h20 | Cours complet MIT |
| **Back To Back SWE** | "Hash Tables and Hash Functions" | 22 min | Implémentation pratique |
| **CS Dojo** | "Hash Tables and Hashmaps in Python" | 15 min | Application Python |
| **mycodeschool** | "Data Structures: Hash Tables" | 13 min | Visualisation claire |

#### Mathématiques Requises

| Concept | Description | Application dans le module |
|---------|-------------|---------------------------|
| **Arithmétique modulaire** | Opération `key mod m` | Fonction de hash de base |
| **Probabilités fondamentales** | P(collision), espérance | Analyse des collisions |
| **Birthday Paradox** | P(collision) ≈ 1 - e^(-n²/2m) | Pourquoi les collisions arrivent plus vite qu'attendu |
| **Analyse amortie** | Coût moyen sur séquence d'opérations | Justification du O(1) malgré le rehashing |
| **Fonctions universelles** | h(k) = ((ak + b) mod p) mod m | Hash functions de qualité |
| **Séries géométriques** | Σ(1/2^i) = 2 | Analyse du load factor |

**Prérequis mathématiques** : Arithmétique de base, notions de probabilités

#### Mini-exercices Préparatoires

| # | Exercice | Objectif | Difficulté | Temps estimé |
|---|----------|----------|------------|--------------|
| 1 | Implémenter une fonction de hash pour strings (méthode polynomial rolling hash) | Comprendre comment transformer une clé en index | Facile | 30 min |
| 2 | Calculer le load factor d'une table de 100 éléments avec 150 slots | Comprendre la notion de charge | Facile | 15 min |
| 3 | Simuler 20 insertions et compter les collisions (à la main) | Voir le birthday paradox en action | Facile | 20 min |
| 4 | Implémenter une hash table avec chaining en Python | Technique de résolution de collision | Moyen | 1h |
| 5 | Implémenter linear probing et compter les steps moyens | Open addressing | Moyen | 45 min |
| 6 | Comparer chaining vs linear probing sur 1000 éléments | Analyse empirique | Moyen | 1h |
| 7 | Implémenter le rehashing automatique quand load factor > 0.75 | Dynamic resizing | Moyen | 1h |
| 8 | Calculer théoriquement le load factor optimal et vérifier empiriquement | Lier théorie et pratique | Difficile | 1h30 |

#### Tests LeetCode Associés

| # | Problème | Difficulté | Thème spécifique | Temps estimé | Concepts clés |
|---|----------|------------|------------------|--------------|---------------|
| 1 | **LC 1 Two Sum** | Easy | HashMap lookup de base | 30 min | Hash map comme structure de recherche |
| 2 | **LC 217 Contains Duplicate** | Easy | HashSet simple | 15 min | Set pour détecter doublons |
| 3 | **LC 242 Valid Anagram** | Easy | Character counting avec hash | 20 min | Counting sort via hash |
| 4 | **LC 49 Group Anagrams** | Medium | Hash function design | 45 min | Choisir une bonne clé de hash |
| 5 | **LC 706 Design HashMap** | Easy | Implémentation complète | 1h | Construire from scratch |
| 6 | **LC 128 Longest Consecutive Sequence** | Medium | HashSet pour O(n) | 45 min | Éviter le tri avec hash |
| 7 | **LC 560 Subarray Sum Equals K** | Medium | Prefix sum + HashMap | 1h | Hash pour cumulative sum |
| 8 | **LC 525 Contiguous Array** | Medium | Transform + HashMap | 45 min | Réduction de problème |

#### Quiz de Validation

| # | Question | Réponse attendue |
|---|----------|------------------|
| 1 | Quelle est la complexité moyenne d'une recherche dans une hash table bien dimensionnée ? | O(1) amorti |
| 2 | Qu'est-ce que le load factor et quelle valeur est généralement optimale ? | α = n/m, typiquement 0.7-0.75 |
| 3 | Comment fonctionne le chaining pour résoudre les collisions ? | Liste chaînée à chaque bucket, insertion en tête O(1) |
| 4 | Qu'est-ce que le rehashing et quand se produit-il ? | Doubler la taille de la table quand load factor > seuil, re-hasher tous les éléments |
| 5 | Pourquoi utilise-t-on des nombres premiers pour la taille de la table ? | Meilleure distribution, réduit les patterns de collision |
| 6 | Qu'est-ce que le Birthday Paradox et pourquoi est-il pertinent ? | Avec m slots, ~√(2m) insertions suffisent pour 50% de chance de collision |
| 7 | Différence entre hash cryptographique et hash pour tables ? | Crypto: unidirectionnel, résistant aux collisions. Table: rapide, bonne distribution |
| 8 | Quand utiliser une hash table vs un arbre équilibré (BST) ? | Hash: lookup O(1) si pas besoin d'ordre. BST: O(log n) mais ordonné |

---

### 1.3.1.b : Collision Resolution Avancée

#### Ressources Universitaires (Théorie Fondamentale)

| Source | Contenu | Lien/Référence |
|--------|---------|----------------|
| **MIT 6.006** | Lecture 9: Open Addressing | MIT OCW |
| **CLRS** | Section 11.4: Open Addressing | pp. 269-280 |
| **Algorithms 4th Ed** | Section 3.4: Linear Probing | Sedgewick |
| **Stanford CS166** | Advanced Hashing | Stanford |

#### Vidéos YouTube (Storytelling & Culture G)

| Chaîne | Vidéo | Durée | Ce que vous apprendrez |
|--------|-------|-------|------------------------|
| **mycodeschool** | "Open Addressing in Hash Tables" | 15 min | Visualisation probing |
| **Abdul Bari** | "Double Hashing" | 12 min | Technique avancée |
| **WilliamFiset** | "Hash Table Linear Probing" | 20 min | Implémentation détaillée |
| **Computerphile** | "Cuckoo Hashing" | 11 min | Technique moderne |

#### Mathématiques Requises

| Concept | Description | Application |
|---------|-------------|-------------|
| **Probing Sequences** | h(k,i) = (h(k) + f(i)) mod m | Formule générale |
| **Primary Clustering** | Tendance à former des chaînes continues | Problème du linear probing |
| **Secondary Clustering** | Clustering de même hash initial | Problème du quadratic probing |
| **Double Hashing** | h(k,i) = (h1(k) + i*h2(k)) mod m | Solution au clustering |

#### Mini-exercices Préparatoires

| # | Exercice | Objectif | Difficulté |
|---|----------|----------|------------|
| 1 | Visualiser le clustering avec linear probing sur papier | Comprendre le problème | Facile |
| 2 | Implémenter quadratic probing | Alternative au linear | Moyen |
| 3 | Implémenter double hashing | Solution au clustering | Moyen |
| 4 | Comparer les trois méthodes sur 1000 insertions | Analyse empirique | Moyen |
| 5 | Implémenter la suppression avec tombstones | Gérer les suppressions | Difficile |
| 6 | Implémenter Robin Hood hashing | Technique moderne | Difficile |

#### Tests LeetCode Associés

| # | Problème | Difficulté | Thème |
|---|----------|------------|-------|
| 1 | **LC 705 Design HashSet** | Easy | Set avec probing |
| 2 | **LC 380 Insert Delete GetRandom O(1)** | Medium | Design avancé |
| 3 | **LC 381 Insert Delete GetRandom Duplicates** | Hard | Extension avec duplicates |

#### Quiz de Validation

| # | Question | Réponse attendue |
|---|----------|------------------|
| 1 | Qu'est-ce que le primary clustering et comment l'éviter ? | Chaînes continues dans linear probing. Éviter avec quadratic ou double hashing |
| 2 | Pourquoi double hashing est-il supérieur à linear/quadratic probing ? | Pas de clustering car la séquence dépend de la clé |
| 3 | Comment supprimer un élément en open addressing ? | Utiliser des tombstones (marqueurs de suppression) |
| 4 | Qu'est-ce que le Robin Hood hashing ? | Voler la place d'un élément plus "riche" (moins de probes) |

---

## Sous-module 1.3.2 : LRU Cache Design (35h)

### 1.3.2.a : Concept de Cache LRU

#### Ressources Universitaires (Théorie Fondamentale)

| Source | Contenu | Lien/Référence |
|--------|---------|----------------|
| **MIT 6.004** | Cache Memory Design | MIT OCW |
| **CMU 15-213** | Lecture 11: Cache Memories | [CMU](http://www.cs.cmu.edu/~213/) |
| **OS Concepts (Silberschatz)** | Chapter 9: Virtual Memory - Page Replacement | ISBN: 978-1119800361 |
| **Computer Architecture (Patterson)** | Chapter 5: Memory Hierarchy | ISBN: 978-0128119051 |

#### Vidéos YouTube (Storytelling & Culture G)

| Chaîne | Vidéo | Durée | Ce que vous apprendrez |
|--------|-------|-------|------------------------|
| **NeetCode** | "LRU Cache - Leetcode 146" | 18 min | Solution optimale expliquée |
| **Back To Back SWE** | "Implement An LRU Cache" | 25 min | Implémentation détaillée |
| **Tech Dummies** | "LRU Cache Explained" | 15 min | Intuition du concept |
| **Computerphile** | "Caching Explained" | 12 min | Contexte général du caching |
| **MIT OCW** | "6.004 L16: Cache Design" | 50 min | Cours complet sur le cache |

#### Mathématiques Requises

| Concept | Description | Application |
|---------|-------------|-------------|
| **Analyse amortie** | Coût moyen par opération | Justifier O(1) pour get/put |
| **Locality of Reference** | Principe de localité spatiale/temporelle | Pourquoi LRU fonctionne |
| **Hit Rate Analysis** | Ratio cache hits / total accesses | Mesurer l'efficacité |
| **Working Set Model** | Ensemble des pages utilisées récemment | Théorie sous-jacente |

#### Mini-exercices Préparatoires

| # | Exercice | Objectif | Difficulté |
|---|----------|----------|------------|
| 1 | Implémenter une doubly linked list avec sentinel nodes | Prérequis technique | Moyen |
| 2 | Combiner HashMap + LinkedList (sans O(1) delete) | Premier essai | Moyen |
| 3 | Modifier pour avoir O(1) delete avec node references | Architecture LRU | Moyen |
| 4 | Tester avec différentes séquences d'accès | Comprendre le comportement | Facile |
| 5 | Calculer le hit rate sur un workload simulé | Analyse de performance | Moyen |
| 6 | Comparer LRU vs FIFO vs LFU sur même workload | Comprendre les trade-offs | Difficile |

#### Tests LeetCode Associés

| # | Problème | Difficulté | Thème | Temps estimé |
|---|----------|------------|-------|--------------|
| 1 | **LC 146 LRU Cache** | Medium | Design principal | 1h30 |
| 2 | **LC 460 LFU Cache** | Hard | Extension avec frequency | 2h |
| 3 | **LC 432 All O(1) Data Structure** | Hard | Généralisation | 2h |
| 4 | **LC 588 Design In-Memory File System** | Hard | Application étendue | 2h |

**NOTE IMPORTANTE** : LC 146 apparaît aussi dans d'autres modules (System Design, Phase 5) mais dans des contextes différents :
- Ici : Apprentissage de la structure de données
- Phase 5 : Application dans un cache distribué
- System Design : Design à grande échelle

C'est de la **réapplication pédagogique**, pas de la duplication.

#### Quiz de Validation

| # | Question | Réponse attendue |
|---|----------|------------------|
| 1 | Pourquoi utiliser une doubly linked list et pas une singly linked list ? | Suppression en O(1) requiert accès au nœud précédent |
| 2 | Quelle est la complexité de get() et put() dans un LRU cache bien implémenté ? | O(1) pour les deux |
| 3 | Comment implémenter un LRU cache thread-safe ? | Mutex sur toute la structure OU ConcurrentHashMap + ConcurrentLinkedQueue |
| 4 | Différence entre LRU, LFU, et FIFO cache ? | LRU: moins récent. LFU: moins fréquent. FIFO: premier entré |
| 5 | Dans quels cas LRU est-il moins performant que d'autres stratégies ? | Scans séquentiels (database table scan) polluent le cache |
| 6 | Qu'est-ce qu'un sentinel node et pourquoi l'utiliser ? | Nœud factice qui simplifie le code (pas de cas spéciaux head/tail) |

---

## Projet du Module : Custom Hash Table Library (20h)

### Objectifs
1. Implémenter une hash table complète en C++ ou Rust
2. Supporter chaining ET open addressing
3. Benchmarker contre std::unordered_map / HashMap standard

### Architecture Détaillée

```
custom_hashtable/
├── include/
│   ├── hashtable.h           # Interface principale (template)
│   ├── chaining.h            # Implémentation chaining
│   ├── probing.h             # Implémentation open addressing
│   └── hash_functions.h      # Collection de fonctions de hash
├── src/
│   ├── hashtable.cpp         # Implémentation commune
│   ├── chaining.cpp          # Chaining avec dynamic resizing
│   ├── probing.cpp           # Linear, quadratic, double hashing
│   └── hash_functions.cpp    # MurmurHash, FNV, polynomial
├── tests/
│   ├── unit_tests.cpp        # Tests unitaires exhaustifs
│   ├── benchmarks.cpp        # Comparaison avec std::unordered_map
│   └── stress_tests.cpp      # Tests de charge
├── docs/
│   ├── DESIGN.md             # Décisions d'architecture (ADRs)
│   └── BENCHMARKS.md         # Résultats des benchmarks
└── README.md                 # Documentation utilisateur
```

### Livrables Détaillés

| # | Livrable | Heures | Description | Critères d'acceptation |
|---|----------|--------|-------------|------------------------|
| 1 | Hash functions | 3h | Implémenter 3+ fonctions de hash | MurmurHash3, FNV-1a, polynomial |
| 2 | Chaining impl | 4h | Avec dynamic resizing | Load factor < 0.75 déclenche resize |
| 3 | Open addressing | 4h | Linear, quadratic, double | Les 3 méthodes disponibles |
| 4 | Unit tests | 3h | 100% coverage | Tous les edge cases couverts |
| 5 | Benchmarks | 3h | vs std::unordered_map | Performance dans ±20% du standard |
| 6 | Documentation | 2h | README + API docs | Usage clair, exemples inclus |
| 7 | LRU Cache | 1h | Utilisant votre hash table | get() et put() en O(1) |

### Critères d'Évaluation Finaux

- [ ] Toutes les opérations en O(1) amorti
- [ ] Tests passent à 100%
- [ ] Performance comparable (±20%) à std::unordered_map
- [ ] Code propre et documenté
- [ ] Pas de memory leaks (valgrind clean)
- [ ] ADRs documentant les choix techniques

---

## Récapitulatif du Module

| Métrique | Valeur |
|----------|--------|
| **Heures totales** | 70h |
| **Exercices LeetCode** | 15 (tous UNIQUES dans CE module) |
| **Mini-exercices** | 20 |
| **Questions quiz** | 20 |
| **Projet** | 1 (20h) |
| **XP gagné** | 1000 |

### Prérequis
- Module 1.1 : Complexité algorithmique (Big-O)
- Module 1.2 : Linked Lists (doubly linked lists)

### Ce Module Débloque
- Module 1.4 : Trees & Graphs
- Module 5.1 : System Design (caching distribué)
- Module 6.2 : Database Engine (index hash)

---

*Ce format EXACT doit être appliqué à TOUS les modules du curriculum POKÉOS.*
*Chaque sous-module suit la structure : Ressources → Vidéos → Math → Mini-exercices → LeetCode → Quiz*
