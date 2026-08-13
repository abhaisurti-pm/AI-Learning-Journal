# Embeddings

## 1. What is an Embedding?

An embedding is a numerical vector representation of data that captures useful relationships between items.

An embedding represents an item using multiple numerical values in a multi-dimensional embedding space.

A useful AI Project Manager mental model is:

> An embedding converts data into a numerical representation that allows an AI system to compare and understand relationships between items based on learned patterns.

Embeddings can be created for different types of data, including:

* Text
* Words
* Images
* Products
* Documents
* Other types of data

The important point is that the individual dimensions of an embedding usually do not have simple human-readable meanings. The useful information is generally represented by the relationships between the vectors.

---

## 2. Embedding Space

An embedding space is the multi-dimensional space in which embedding vectors are represented.

Items with similar characteristics, meaning, or learned relationships can be positioned closer together in the embedding space.

Conceptually:

**Data → Embedding Model → Vector → Embedding Space → Relationships**

For example, two pieces of text with similar meaning may produce embeddings that are close to each other in the embedding space.

The exact number of dimensions depends on the embedding model and learning approach.

AI PMs do not need to understand the mathematical details of high-dimensional spaces at this stage.

The important understanding is:

> Similarity in embedding space can be used to support AI capabilities such as semantic search, recommendations and content discovery.

---

## 3. Embedding Dimensions

An embedding represents each item using a fixed number of numerical dimensions.

For example:

```text
[0.12, -0.73, 0.44, 0.91, ...]
```

Each value is a floating-point number.

The number of dimensions is determined by the embedding model or learning setup.

Individual dimensions should not automatically be interpreted as simple human concepts such as:

* "Technicality"
* "Friendliness"
* "Modernity"
* "Legal relevance"

The dimensions are generally learned representations.

Therefore:

> The overall vector and the relationships between vectors are usually more meaningful than trying to interpret individual dimensions.

---

## 4. Embeddings vs One-Hot Encoding

One-hot encoding represents each item using a vector where one position identifies the item and the remaining positions are zero.

For example:

```text
Lawyer   → [0, 0, 1, 0, 0]
Attorney → [0, 1, 0, 0, 0]
Banana   → [1, 0, 0, 0, 0]
```

One-hot encoding primarily represents the identity of an item.

It does not naturally represent semantic relationships.

For example, one-hot encoding does not inherently communicate that:

**Lawyer ≈ Attorney**

while:

**Lawyer ≠ Banana**

Embeddings provide learned numerical representations that can capture useful relationships between items.

Therefore:

> One-hot encoding identifies an item, while embeddings can represent useful relationships involving the item.

Embeddings can also provide a more compact representation than a one-hot vector when dealing with large numbers of items.

---

## 5. Task-Specific Embeddings

Embeddings are generally influenced by the task and data used to create them.

Different applications may require different definitions of similarity.

Examples include:

* Legal document similarity
* Product similarity
* Image similarity
* Customer-support intent similarity
* Recommendation relevance
* Semantic text similarity

Therefore:

> An embedding model that works well for one task is not automatically the best choice for another task.

AI PMs should consider:

* Type of data
* Business problem
* Definition of similarity
* Required quality
* Model capabilities
* Evaluation requirements

The embedding representation should support the actual product objective.

---

## 6. Static Embeddings

A static embedding generally assigns a fixed representation to an item.

An older but useful example is Word2Vec.

Word2Vec learns word representations from the contexts in which words appear and produces a single global embedding for each word.

For example:

```text
"bank" → Fixed embedding
```

The same representation is used whether the word appears in:

> "I deposited money in the bank."

or:

> "We sat beside the river bank."

When each word or data point has a single embedding vector, it is called a **static embedding**.

Static embeddings are useful for understanding the development of embedding techniques but have limitations when the same word has multiple meanings.

---

## 7. Contextual Embeddings

Contextual embeddings were developed to address limitations of static representations.

A contextual representation incorporates information from the surrounding context.

For example:

**"River bank"**

can produce a representation influenced by the geographical meaning of "bank."

**"Bank deposit"**

can produce a representation influenced by the financial meaning of "bank."

Another example:

> "I ate a crisp red Apple."

versus:

> "Apple released a new iPhone."

The surrounding words provide context that helps distinguish the meaning of the word.

Therefore:

> Static embeddings generally provide a fixed representation, while contextual representations incorporate surrounding context when representing a word or token.

---

## 8. How Embeddings Can Be Learned

Embeddings can be created in different ways.

One approach is to train embeddings separately for a particular purpose.

Another approach is to learn an embedding as part of training a larger neural network.

A neural network can contain an embedding layer where:

* The layer represents the embedding
* The number of nodes represents the embedding dimensions
* The learned parameters are optimized during training

Conceptually:

**Input → Embedding Layer → Additional Processing → Output**

The embedding can therefore become customized for the target task.

AI PMs do not need to understand the underlying optimization or neural-network mathematics at this stage.

The important understanding is:

> The model can learn numerical representations that help it perform its intended task.

---

## 9. Semantic Similarity

One of the important uses of embeddings is identifying semantic similarity.

For example:

**Text A:**

> How do I terminate a commercial lease early?

**Text B:**

> Steps for tenant exit prior to contract expiration.

The wording is different, but the underlying intent is similar.

An embedding-based system can represent both pieces of text as vectors and compare their relationship in embedding space.

This allows AI systems to work with meaning and relationships rather than relying only on exact keyword matches.

However:

> Similar embeddings do not automatically mean two items have exactly the same meaning.

Similarity reflects the relationships learned by the embedding model.

Therefore, AI teams must evaluate whether the model's definition of similarity matches the product's definition of relevance.

---

## 10. Embeddings and AI Applications

Embeddings can support a variety of AI capabilities.

Examples include:

* Semantic search
* Similar-content discovery
* Recommendation systems
* Content clustering
* Classification
* Intent matching
* Document discovery
* Natural-language search

A useful mental model is:

**Content → Embedding → Vector Representation → Similarity / Relationship → AI Capability**

The embedding itself is not the complete product.

It is a technology component that enables other product capabilities.

---

## 11. Choosing an Embedding Model

The best embedding model is not automatically the largest or most sophisticated model.

The appropriate choice depends on the product requirements.

AI PMs should consider:

* Data type
* Language requirements
* Domain requirements
* Semantic similarity requirements
* Accuracy
* Latency
* Cost
* Scale
* Security
* Privacy
* Evaluation requirements

The key question is:

> What embedding capability is required to solve the product problem within our technical, business and operational constraints?

---

## 12. When to Use Embeddings

Embeddings are particularly useful when a product needs to understand relationships between pieces of information.

Examples include:

* Finding documents with similar meaning
* Matching user questions with relevant content
* Finding similar products
* Discovering related cases or documents
* Grouping similar content
* Identifying similar customer-support requests
* Supporting natural-language search

However, embeddings should not automatically be selected simply because a product contains text.

The AI PM should first understand:

* The business problem
* User workflow
* Definition of relevance
* Accuracy requirements
* Data requirements
* Scale
* Cost
* Latency
* Risk

---

## 13. Example — Legal Research Product

### Semantic Precedent Finder

Business requirement:

> Lawyers need to discover relevant legal precedents even when their search wording differs from the language used in court judgments.

A traditional keyword-based search may depend heavily on exact words or Boolean queries.

An embedding-based capability could conceptually work as:

**Lawyer Query → Query Embedding → Compare with Document Representations → Identify Relevant Documents → Present Relevant Precedents**

For example:

> "contract violation by juvenile"

could potentially identify legally relevant documents that use different terminology.

The product value could include:

* Reduced research time
* Improved discovery of relevant precedents
* Reduced dependence on complex keyword queries
* Better natural-language search
* Improved researcher productivity

However, semantic similarity alone does not guarantee legal relevance.

The AI PM must ensure appropriate:

* Evaluation
* Accuracy requirements
* Source quality
* Legal relevance validation
* Human oversight where required

---

## 14. AI PM Mental Model

Embeddings are a technology component rather than a complete AI product.

A useful AI PM mental model is:

**Business Problem → User / Workflow → AI Capability → Data → Embedding Model → Vector Representation → Similarity / Relationship → Product Output → Evaluation → Business Outcome**

The AI PM is responsible for ensuring that the embedding capability actually supports the intended product requirement.

The key question is not:

> "Are we using embeddings?"

The better question is:

> "What relationship or similarity does the product need the AI system to understand, and does the embedding approach provide that capability reliably?"

---

## 15. What I Do Not Need to Learn Yet

The following topics are intentionally outside the scope of Day 4:

* RAG
* Vector databases
* LangChain
* ANN indexes
* HNSW
* FAISS
* Retrieval pipelines
* Advanced vector search
* Advanced linear algebra
* Word2Vec implementation
* Skip-gram mathematics
* CBOW mathematics
* Backpropagation
* Embedding optimization
* Training embedding models from scratch

These topics will be covered later when they become relevant to the learning roadmap.

---

## 16. Assessment

Google Machine Learning Crash Course — Embeddings

**Quiz Result: 5/5 — Passed**

The course assessment confirmed understanding of the core embedding concepts.

The learning was also reviewed through an AI Project Manager validation exercise covering:

* Definition of embeddings
* Embeddings vs one-hot encoding
* Semantic similarity
* Static vs contextual embeddings
* Practical application of embeddings in a legal research product

**Day 4 validation: Passed**

---

## 17. Key AI PM Takeaways

1. An embedding is a numerical vector representation of data.
2. Embeddings can capture useful relationships between items.
3. Embedding space represents these relationships across multiple dimensions.
4. Individual embedding dimensions usually do not have simple human-readable meanings.
5. One-hot encoding primarily identifies items, while embeddings can represent relationships.
6. Embeddings are generally influenced by the task and data used to create them.
7. Static embeddings provide a fixed representation for an item.
8. Contextual representations incorporate surrounding context.
9. Similar embeddings indicate similarity according to the embedding model's learned representation.
10. Similarity does not automatically guarantee identical meaning or business relevance.
11. Embeddings can support semantic search, recommendations, classification and content discovery.
12. The embedding model should be selected based on the product's data, requirements and constraints.
13. Embeddings are a technology component, not automatically a complete AI product.
14. AI PMs must evaluate whether the embedding model's notion of similarity matches the product's definition of relevance.
15. Evaluation, accuracy, cost, latency, scale, security and privacy remain important considerations.

---

## 18. AI PM Question to Remember

> **What relationship or similarity does our product need the AI system to understand, and does the embedding approach represent that relationship reliably enough to create business value?**
