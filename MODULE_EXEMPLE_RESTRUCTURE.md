# EXEMPLE DE MODULE RESTRUCTURÉ

Ce fichier montre le format standard que CHAQUE module du curriculum devrait suivre.

---

# MODULE 1.3 : Hash Tables & Advanced Data Structures

## Durée : 70 heures | XP : 1000 | Semaines 5-6

---

## Sous-module 1.3.1 : Hash Tables Fondamentales (35h)

### 1.3.1.a : Introduction aux Hash Tables

#### Ressources Universitaires (Théorie Fondamentale)
| Source | Contenu | Lien |
|--------|---------|------|
| **MIT 6.006** | Lecture 8: Hashing with Chaining | [MIT OCW](https://ocw.mit.edu/courses/6-006-introduction-to-algorithms-spring-2020/) |
| **Stanford CS161** | Hash Tables and Analysis | [Stanford](https://stanford.edu/class/cs161/) |
| **CLRS** | Chapter 11: Hash Tables | Livre de référence |
| **Princeton Algorithms** | Hash Tables | [Coursera](https://www.coursera.org/learn/algorithms-part1) |

#### Vidéos YouTube (Storytelling & Culture G)
| Chaîne | Vidéo | Durée |
|--------|-------|-------|
| **Computerphile** | "Hash Tables" | 12 min |
| **Abdul Bari** | "Hashing Techniques" | 18 min |
| **CS Dojo** | "Hash Tables Explained" | 15 min |
| **MIT OCW** | "Lecture 8: Hashing" | 1h20 |
| **Back To Back SWE** | "Hash Table Implementation" | 22 min |

#### Mathématiques Requises
| Concept | Description | Prérequis |
|---------|-------------|-----------|
| **Modular Arithmetic** | Fonction hash = key mod m | Arithmétique de base |
| **Probabilité** | Analyse des collisions | Probabilités fondamentales |
| **Birthday Paradox** | Pourquoi les collisions arrivent | Combinatoire |
| **Analyse Amortie** | Coût du rehashing | Big-O notation |
| **Fonctions Universelles** | h(k) = ((ak + b) mod p) mod m | Théorie des nombres |

#### Mini-exercices Préparatoires
| # | Exercice | Objectif | Difficulté |
|---|----------|----------|------------|
| 1 | Implémenter une fonction de hash pour strings | Comprendre le hashing | Facile |
| 2 | Gérer une collision par chaining | Technique de base | Facile |
| 3 | Implémenter linear probing | Open addressing | Moyen |
| 4 | Calculer le load factor optimal | Analyse théorique | Moyen |
| 5 | Implémenter quadratic probing | Alternative à linear | Moyen |
| 6 | Comparer les performances chaining vs probing | Analyse empirique | Moyen |

#### Tests LeetCode Associés
| # | Problème | Difficulté | Thème spécifique | Temps estimé |
|---|----------|------------|------------------|--------------|
| 1 | LC 1 Two Sum | Easy | HashMap lookup de base | 30 min |
| 2 | LC 217 Contains Duplicate | Easy | HashSet simple | 15 min |
| 3 | LC 242 Valid Anagram | Easy | Character counting | 20 min |
| 4 | LC 49 Group Anagrams | Medium | Hash function design | 45 min |
| 5 | LC 706 Design HashMap | Easy | Implémentation complète | 1h |
| 6 | LC 128 Longest Consecutive | Medium | HashSet pour O(n) | 45 min |

#### Quiz de Validation
| # | Question | Réponse attendue |
|---|----------|------------------|
| 1 | Quelle est la complexité moyenne d'une recherche dans une hash table ? | O(1) amorti |
| 2 | Qu'est-ce que le load factor et quelle valeur est optimale ? | n/m, typiquement 0.7-0.75 |
| 3 | Comment fonctionne le chaining pour résoudre les collisions ? | Liste chaînée à chaque bucket |
| 4 | Qu'est-ce que le rehashing et quand se produit-il ? | Doubler la table quand load factor > seuil |
| 5 | Différence entre open addressing et chaining ? | Stockage interne vs externe des collisions |

---

### 1.3.1.b : Collision Resolution Avancée

#### Ressources Universitaires (Théorie Fondamentale)
| Source | Contenu | Lien |
|--------|---------|------|
| **MIT 6.006** | Lecture 9: Open Addressing | MIT OCW |
| **CLRS** | Section 11.4: Open Addressing | Livre |
| **Algorithms 4th Ed** | Section 3.4: Hash Tables | Sedgewick |

#### Vidéos YouTube (Storytelling & Culture G)
| Chaîne | Vidéo | Durée |
|--------|-------|-------|
| **mycodeschool** | "Open Addressing" | 15 min |
| **Abdul Bari** | "Double Hashing" | 12 min |
| **WilliamFiset** | "Hash Table Linear Probing" | 20 min |

#### Mathématiques Requises
| Concept | Description |
|---------|-------------|
| **Probing Sequences** | h(k,i) = (h(k) + f(i)) mod m |
| **Primary Clustering** | Problème du linear probing |
| **Secondary Clustering** | Problème du quadratic probing |
| **Double Hashing** | h(k,i) = (h1(k) + i*h2(k)) mod m |

#### Mini-exercices Préparatoires
| # | Exercice | Objectif |
|---|----------|----------|
| 1 | Visualiser le clustering avec linear probing | Comprendre le problème |
| 2 | Implémenter double hashing | Résoudre le clustering |
| 3 | Comparer les trois méthodes sur 1000 insertions | Analyse empirique |
| 4 | Implémenter Robin Hood hashing | Technique avancée |

#### Tests LeetCode Associés
| # | Problème | Difficulté | Thème |
|---|----------|------------|-------|
| 1 | LC 380 Insert Delete GetRandom O(1) | Medium | Design avancé |
| 2 | LC 381 Insert Delete GetRandom Duplicates | Hard | Extension avec duplicates |
| 3 | LC 705 Design HashSet | Easy | Set operations |

#### Quiz de Validation
| # | Question |
|---|----------|
| 1 | Qu'est-ce que le primary clustering et comment l'éviter ? |
| 2 | Pourquoi double hashing est-il supérieur à linear/quadratic probing ? |
| 3 | Comment supprimer un élément en open addressing ? (hint: tombstones) |

---

## Sous-module 1.3.2 : LRU Cache Design (35h)

### 1.3.2.a : Concept de Cache LRU

#### Ressources Universitaires (Théorie Fondamentale)
| Source | Contenu |
|--------|---------|
| **MIT 6.004** | Cache Memory Design |
| **CMU 15-213** | Cache Memories |
| **OS Concepts (Silberschatz)** | Chapter 9: Virtual Memory |

#### Vidéos YouTube (Storytelling & Culture G)
| Chaîne | Vidéo | Durée |
|--------|-------|-------|
| **NeetCode** | "LRU Cache - LeetCode 146" | 18 min |
| **Back To Back SWE** | "Implement An LRU Cache" | 25 min |
| **Tech Dummies** | "LRU Cache Explained" | 15 min |
| **Computerphile** | "Caching Explained" | 12 min |

#### Mathématiques Requises
| Concept | Application |
|---------|-------------|
| **Analyse amortie** | Opérations O(1) |
| **Locality of Reference** | Pourquoi LRU fonctionne |
| **Hit Rate Analysis** | Mesurer l'efficacité |

#### Mini-exercices Préparatoires
| # | Exercice | Objectif |
|---|----------|----------|
| 1 | Implémenter une doubly linked list | Prérequis |
| 2 | Combiner HashMap + LinkedList | Architecture LRU |
| 3 | Tester avec différentes séquences d'accès | Comprendre le comportement |
| 4 | Calculer le hit rate sur un workload | Analyse de performance |

#### Tests LeetCode Associés (UNIQUE - PAS DE RÉPÉTITION)
| # | Problème | Difficulté | Thème | Temps |
|---|----------|------------|-------|-------|
| 1 | **LC 146 LRU Cache** | Medium | Design principal | 1h30 |
| 2 | LC 460 LFU Cache | Hard | Extension avec frequency | 2h |
| 3 | LC 432 All O(1) Data Structure | Hard | Généralisation | 2h |

**NOTE** : Ces exercices n'apparaissent QU'ICI dans le curriculum.

#### Quiz de Validation
| # | Question |
|---|----------|
| 1 | Pourquoi utiliser une doubly linked list et pas une singly linked list ? |
| 2 | Quelle est la complexité de get() et put() dans un LRU cache bien implémenté ? |
| 3 | Comment implémenter un LRU cache thread-safe ? |
| 4 | Différence entre LRU, LFU, et FIFO cache ? |
| 5 | Dans quels cas LRU est-il moins performant que d'autres stratégies ? |

---

## Projet du Module : Custom Hash Table Library (20h)

### Objectifs
1. Implémenter une hash table complète en C++/Rust
2. Supporter chaining ET open addressing
3. Benchmarker contre std::unordered_map

### Architecture
```
custom_hashtable/
├── include/
│   ├── hashtable.h        // Interface principale
│   ├── chaining.h         // Implémentation chaining
│   ├── probing.h          // Implémentation open addressing
│   └── hash_functions.h   // Fonctions de hash
├── src/
│   ├── hashtable.cpp
│   ├── chaining.cpp
│   ├── probing.cpp
│   └── hash_functions.cpp
├── tests/
│   ├── unit_tests.cpp
│   └── benchmarks.cpp
└── README.md
```

### Livrables
| # | Livrable | Heures | Description |
|---|----------|--------|-------------|
| 1 | Hash functions | 3h | Multiple hash functions |
| 2 | Chaining impl | 4h | With dynamic resizing |
| 3 | Open addressing impl | 4h | Linear, quadratic, double |
| 4 | Unit tests | 3h | 100% coverage |
| 5 | Benchmarks | 3h | vs std::unordered_map |
| 6 | Documentation | 2h | README + API docs |
| 7 | LRU Cache | 1h | Using your hash table |

### Critères d'évaluation
- [ ] Toutes les opérations en O(1) amorti
- [ ] Tests passent à 100%
- [ ] Performance comparable à std::unordered_map
- [ ] Code propre et documenté
- [ ] Pas de memory leaks (valgrind clean)

---

## Récapitulatif du Module

| Métrique | Valeur |
|----------|--------|
| Heures totales | 70h |
| Exercices LeetCode | 12 (UNIQUES) |
| Mini-exercices | 16 |
| Questions quiz | 15 |
| Projet | 1 (20h) |
| XP gagné | 1000 |

### Prérequis
- Module 1.1 : Complexité algorithmique
- Module 1.2 : Linked Lists

### Déblocage
Ce module débloque :
- Module 1.4 : Trees & Graphs
- Module 5.1 : System Design (requires hash tables)

---

*Ce format doit être appliqué à TOUS les modules du curriculum POKÉOS.*
