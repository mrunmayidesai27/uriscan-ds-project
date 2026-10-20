# UriScan – Urine Test Strip Reader

Colorimetry-based AI use case · Data Structures mini project (Units 1–5 mapped to real features)

## 1 · Scan strip (Colorimetry)

Unit 1: ADT, space/time complexityUnit 4: Map ADT, Hash table

Upload a strip photo and click a pad to sample its colour, or choose colours manually. Each colour is matched to the nearest reference colour (Euclidean distance in RGB, O(k) per pad) found via a hash table with chaining.

## 2 · Priority Queue & Processing

Unit 2: Queue, Priority QueueUnit 5: Heap

Strips wait in a max-heap keyed by severity score, so the most critical sample is processed first.

## 3 · Scan History – Linked List & Undo Stack

Unit 2: Singly Linked List, Stack

**History (linked list)**

**Undo stack (LIFO)**

## 4 · Health Score – Postfix Evaluation

Unit 2: Stack applications, Infix→Postfix, Evaluation

Letters: G=Glucose, P=Protein, K=Ketone, B=Blood, H=pH deviation, N=Nitrite (severity levels 0–3). Edit the formula; it's converted with a stack (shunting-yard) and evaluated with another stack.

## 5 · Patient Index – Binary Search Tree

Unit 3: BST, Traversals, SearchUnit 5: Binary search

**Tree shape** (root at top, indented)

```

```

## 6 · Condition Graph – BFS / DFS

Unit 3: Graph, adjacency list, BFS, DFS

Abnormal pads are start nodes. Traversal finds the possible conditions linked to them (graph: pad → pathway → condition).

## 7 · Sort & Search Records

Unit 5: Bubble, Counting, Heap sort

## 8 · Hash Table (Reference colours & Flags)

Unit 4: Set, Map, DictionaryUnit 5: Chaining, Linear probing

Reference dictionary uses separate chaining (7 buckets, h = Σchar mod 7). The flagged-IDs Set below uses linear probing (size 11).

## Syllabus mapping & complexity

| Unit | Concept | Used in | Complexity |
| --- | --- | --- | --- |
| 1 | ADT, space/time | Every structure as class | — |
| 2 | Linked list | Scan history | Insert O(1) tail ptr, delete tail O(n) |
| 2 | Stack | Undo, postfix | Push/Pop O(1) |
| 2 | Priority queue | Critical-first processing | O(log n) |
| 3 | BST | Patient ID index | Avg O(log n), worst O(n) |
| 3 | Graph BFS/DFS | Condition inference | O(V+E) |
| 4 | Map / Set | Reference table, flags | Avg O(1) |
| 5 | Sorting / Hashing | Records, collision handling | See tab 7 / 8 |