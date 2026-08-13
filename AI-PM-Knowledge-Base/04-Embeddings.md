# Day 4 — Embeddings

**Date:** 13 August 2026
**Phase:** Phase 1 — AI + Technical Foundation
**Week:** Week 1
**Topic:** Embeddings
**Status:** Completed & Validated
**Primary Resource:** Google Machine Learning Crash Course — Embeddings
**Assessment:** 5/5 — Passed

---

## 1. Learning Objective

Understand what embeddings are, why AI systems use them, how embedding space represents relationships between items, and the difference between static and contextual embeddings.

The goal is to understand embeddings at an **AI Project Manager level**, rather than learning the underlying mathematics or implementation details.

---

## 2. Primary Resource

**Google Machine Learning Crash Course — Embeddings**

The module covered:

* Embeddings
* Embedding space
* Static embeddings
* Obtaining embeddings
* Embedding layers
* Contextual embeddings
* Interactive exercises
* Knowledge assessment

---

## 3. What I Learned

### 3.1 What is an Embedding?

An embedding is a **numerical vector representation of data** that captures useful relationships between items.

Instead of representing an item only by an identifier, an embedding represents it using a vector of numerical values in a multi-dimensional embedding space.

Conceptually:

```text
Raw data
   ↓
Embedding model
   ↓
Numerical vector
   ↓
Embedding space
```

For example:

```text
[0.12, -0.73, 0.44, 0.91, ...]
```

The important point is not that individual dimensions necessarily have human-readable meanings. Instead, the overall vector representation allows an AI system to represent and compare relationships between items.

---

## 4. Embedding Space

An embedding space is the multi-dimensional space in which embedding vectors are represented.

Items with similar characteristics, meaning, or learned relationships can be positioned closer together in this space.

Conceptually:

```text
Item A → Vector A
Item B → Vector B

Compare Vector A ↔ Vector B
                ↓
        Similarity / relationship
```

The exact meaning of an individual dimension is often difficult to interpret.

Therefore, from an AI PM perspective, the important question is generally not:

> "What does dimension 327 mean?"

but:

> "What useful relationships does this embedding model capture for our specific use case?"

---

## 5. Embedding Dimensions

An embedding represents an item using a fixed number of numerical dimensions determined by the embedding model or learning setup.

For example:

```text
Embedding
→ [0.12, -0.73, 0.44, 0.91, ...]
```

A model may produce embeddings with hundreds or thousands of dimensions.

The numerical values are not universally restricted to a particular range such as `-1 to 1`. Their range depends on how the embedding model produces and/or normalizes the vectors.

---

## 6. Why One-Hot Encoding Has Limitations

One-hot encoding represents each item using a vector where one position identifies the item and the remaining positions are zero.

Example:

```text
Lawyer   → [0, 0, 1, 0, 0]
Attorney → [0, 1, 0, 0, 0]
Banana   → [1, 0, 0, 0, 0]
```

The major limitation is that one-hot encoding primarily represents **identity**, not semantic relationships.

It does not naturally express that:

```text
Lawyer ≈ Attorney
```

while:

```text
Lawyer ≠ Banana
```

Embeddings provide a learned representation that can capture useful relationships between items.

Therefore:

> **One-hot encoding identifies an item; embeddings represent useful relationships involving the item.**

---

## 7. Task-Specific Embeddings

Embeddings are generally influenced by the task and data used to create them.

Different applications may require different notions of similarity.

For example:

* Legal document similarity
* Product similarity
* Image similarity
* Customer-support intent similarity
* Recommendation relevance

The same embedding approach should not automatically be assumed to be optimal for every use case.

From an AI PM perspective:

> **The embedding model needs to be appropriate for the data, task, and definition of relevance required by the product.**

---

## 8. Static Embeddings

A static embedding generally assigns a fixed representation to an item.

A classic example is **Word2Vec**.

Word2Vec learns representations from the contexts in which words appear. A word receives a single global embedding.

For example:

```text
"bank"
   ↓
Fixed vector
```

The same representation is used regardless of whether the word appears in:

> "I deposited money in the bank."

or:

> "We sat beside the river bank."

Static embeddings are useful for understanding the historical development of embedding techniques, but they have limitations when words have multiple meanings.

---

## 9. Contextual Embeddings

Contextual embeddings address the limitation of fixed word representations by incorporating surrounding context.

The same word can therefore receive different representations depending on the sentence or context.

Example:

```text
"River bank"
      ↓
Representation influenced by geography

"Bank deposit"
      ↓
Representation influenced by finance
```

Another example:

```text
"I ate a crisp red Apple."
        ↓
Fruit-related context

"Apple released a new iPhone."
        ↓
Technology/company-related context
```

The important distinction is:

> **Static embeddings generally provide a fixed representation, while contextual representations incorporate surrounding context when representing a word or token.**

---

## 10. How Embeddings Can Be Learned

Embeddings can be obtained in different ways.

One approach is to train embeddings separately.

Another approach is to learn an embedding representation as part of a larger neural network.

A neural network can contain an embedding layer whose dimensions represent the embedding space.

Conceptually:

```text
Input
  ↓
Embedding Layer
  ↓
Vector Representation
  ↓
Additional Layers
  ↓
Output / Prediction
```

During training, the model learns representations that help it perform its target task.

At the AI PM level, it is not necessary to understand the underlying backpropagation or optimization mathematics at this stage.

---

## 11. Similar Embeddings

If two pieces of content have similar embeddings, this generally means the embedding model considers them similar according to the relationships it has learned.

For example:

**Text A:**

> How do I terminate a commercial lease early?

**Text B:**

> Steps for tenant exit prior to contract expiration.

Even though the wording differs, the underlying intent is similar.

An embedding-based system can therefore represent the two texts in a way that allows their semantic relationship to be identified.

Important nuance:

> **Similar embeddings do not automatically mean two items have exactly the same meaning. They indicate similarity according to the embedding model and the relationships it has learned.**

This distinction is important when evaluating an AI product.

---

## 12. AI Project Manager Perspective

Embeddings matter to an AI Project Manager because they enable AI systems to work with data based on learned relationships rather than relying only on exact matches.

Potential product capabilities include:

* Semantic search
* Similar-content discovery
* Recommendation systems
* Content clustering
* Classification
* Intent matching
* Similarity-based discovery
* Natural-language search

The product-level mental model is:

```text
Content
   ↓
Embedding model
   ↓
Numerical vector
   ↓
Embedding space
   ↓
Meaningful relationships / similarity
   ↓
AI product capability
```

---

## 13. Practical Application — Legal Research

### Feature: Semantic Precedent Finder

A legal research product could use embeddings to improve precedent discovery.

### Problem

Traditional legal search can depend heavily on exact keywords or Boolean queries.

A lawyer may search:

> "contract violation by juvenile"

while a relevant judgment may use completely different terminology.

A keyword-only search can potentially miss relevant material.

### Embedding-based approach

Conceptually:

```text
Lawyer's Query
      ↓
Query Embedding
      ↓
Compare with Document Embeddings
      ↓
Identify Semantically Relevant Documents
      ↓
Relevant Legal Precedents
```

### Product Value

This could help:

* Reduce time-to-first-relevant-case
* Improve discovery of relevant precedents
* Reduce dependence on complex Boolean queries
* Support natural-language legal research
* Improve discovery when terminology differs

### AI PM consideration

The definition of "similar" must be validated against the actual business requirement.

For a legal product, semantic similarity alone is not enough. The system must ultimately provide results that are **legally relevant and trustworthy**.

---

## 14. What I Do Not Need to Know Yet

The following topics are intentionally outside the scope of Day 4:

* RAG
* Vector databases
* LangChain
* ANN indexes
* HNSW
* FAISS
* Retrieval pipelines
* Advanced vector search
* Training embedding models from scratch
* Advanced linear algebra
* Word2Vec implementation
* Skip-gram mathematics
* CBOW mathematics
* Backpropagation
* Embedding optimization

These will be studied later when they become relevant to the learning roadmap.

---

## 15. Assessment

### Google ML Crash Course — Embeddings Quiz

**Result: 5/5**

**Status: Passed**

The course also unlocked the Machine Learning Crash Course: Embeddings milestone.

---

## 16. Key Corrections From Validation

During validation, the following technical refinements were established:

### Correction 1 — Embeddings are not simply "lower-dimensional projections"

An embedding is better understood as a **learned numerical representation that captures useful relationships**.

Lower dimensionality can be a characteristic of some embedding approaches, but it is not the complete definition.

### Correction 2 — Embedding values are not universally restricted to -1 to 1

The range of embedding values depends on the model and whether/how the vectors are normalized.

### Correction 3 — Individual dimensions usually do not have simple human-readable meanings

Dimensions should not automatically be interpreted as:

```text
Dimension 1 = friendliness
Dimension 2 = technicality
Dimension 3 = seriousness
```

The useful information is generally in the relationships represented by the overall vector.

### Correction 4 — Similar embeddings do not guarantee identical meaning

Similarity reflects the embedding model's learned representation and notion of similarity.

For an AI product, the team must validate whether this notion of similarity matches the product's business definition of relevance.

### Correction 5 — Contextual embeddings are not synonymous with "Transformers"

Transformer is a model architecture. Models using transformer architectures can produce contextual representations, but the two terms should not be treated as identical.

---

## 17. Interview-Level Understanding

If asked:

> **What are embeddings?**

My AI PM-level answer:

> Embeddings are numerical vector representations of data that capture useful relationships between items. They allow AI systems to compare things based on semantic or learned similarity rather than relying only on exact matches. For example, in a legal research product, a lawyer's natural-language query can be represented as an embedding and compared with representations of legal documents to identify relevant precedents even when the wording differs.

---

## 18. Key Takeaway

The core mental model from Day 4 is:

> **Content → Embedding Model → Numerical Vector → Embedding Space → Meaningful Relationships → AI Product Capability**

Embeddings provide the foundation for many AI capabilities where understanding relationships and similarity is more useful than exact keyword matching.

---

## 19. Definition of Done

* [x] Understand what an embedding is
* [x] Understand vector representation
* [x] Understand embedding space
* [x] Understand embedding dimensions
* [x] Understand limitations of one-hot encoding
* [x] Understand semantic similarity
* [x] Understand task-specific embeddings
* [x] Understand static embeddings
* [x] Understand contextual embeddings
* [x] Understand embedding layers at a conceptual level
* [x] Apply embeddings to a real AI product use case
* [x] Explain embeddings from an AI PM perspective
* [x] Complete Google ML Crash Course Embeddings module
* [x] Pass knowledge assessment with 5/5
* [x] Complete understanding validation

**Day 4 — COMPLETED & VALIDATED**
