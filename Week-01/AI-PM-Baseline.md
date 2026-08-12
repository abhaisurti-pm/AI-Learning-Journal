# Week 01 — AI PM Baseline

**Dates:** 10 August 2026 – 14 August 2026
**Phase:** Phase 1 — AI + Technical Foundation
**Weekly Focus:** AI Fundamentals + Generative AI + LLM Foundations

---

## Week Objective

Build a strong foundational understanding of AI and Generative AI concepts required for an AI Project Manager.

The goal is not to become an AI engineer, but to understand the technology well enough to:

* Communicate effectively with AI/ML engineers
* Understand AI project requirements
* Identify AI opportunities and limitations
* Understand technical trade-offs
* Define meaningful AI product and project metrics
* Identify AI risks
* Translate technical concepts into project decisions

---

## Learning Framework

**Learn → Understand → Apply → Build → Document → Explain**

---

## Weekly Topics

### AI Fundamentals

* AI vs ML vs GenAI
* Large Language Models
* Tokens
* Context windows
* Prompts
* Embeddings
* AI APIs
* Hallucinations
* Evaluation basics

### Generative AI

* Generative AI capabilities
* Responsible AI
* Copilot workflows

---

## Daily Learning Plan

### Day 1 — 10 August

**Topic:** AI Fundamentals

**Learning Resource:** Microsoft Learn — Introduction to AI concepts

**Status:** Completed

#### Topics Completed

- Introduction to AI
- Generative AI
- Generative AI applications
- LLMs and SLMs
- AI agents
- AI workloads
- Natural Language Processing
- Text analysis
- Speech AI
- Computer vision
- Information extraction
- Responsible AI

#### Key Understanding

Generative AI enables applications to generate new content such as text, images, audio, video, and code based on learned patterns, instructions, prompts, and available context.

A typical GenAI application follows:

**User → Prompt → Application → AI Model + Context → Generated Output → User**

LLMs are larger language models designed for broad language capabilities, while SLMs are smaller models that can require fewer resources and may be suitable for focused or local/edge scenarios.

AI agents extend beyond conversational responses by using a model, instructions, and tools to reason about tasks and perform actions.

Major AI workloads covered:

- Generative AI
- Natural Language Processing
- Speech
- Computer Vision
- Information Extraction

Responsible AI principles covered:

- Fairness
- Reliability and Safety
- Privacy and Security
- Inclusiveness
- Transparency
- Accountability

#### AI PM Perspective

AI projects require more than traditional project delivery. An AI PM needs to understand the relationship between:

**Business Problem → AI Capability → Solution → Data/Context → Requirements → Risks → Evaluation → Business Outcome**

Important AI PM questions include:

- Why is AI required for this problem?
- Which AI capability is appropriate?
- What data or context is required?
- What quality level is acceptable?
- What happens when the AI is incorrect?
- What level of human involvement is required?
- What responsible AI risks exist?
- How will the AI feature be evaluated?
- What business outcome should improve?

#### Microsoft Learn Assessment

**Module:** Introduction to AI concepts

**Status:** Passed

**Achievement:** Earned

The module assessment was successfully completed after reviewing the learning units, completing the exercise, passing the assessment, and reviewing the summary.

#### Day 1 Reflection

The biggest learning from Day 1 is that AI should not be treated simply as another software component. AI systems introduce model limitations, data dependencies, probabilistic outputs, evaluation requirements, and responsible AI considerations that need to be considered throughout the project lifecycle.

---

### Day 2 — 11 August

**Topic:** Generative AI

**Learning Resource:** Microsoft Learn — What is generative AI?

**Status:** Completed

#### Topics Completed

- Generative AI fundamentals
- Generative AI capabilities
- Large Language Models (LLMs)
- Small Language Models (SLMs)
- Generative AI use cases
- Generative AI application workflow
- Responsible AI considerations
- Microsoft Copilot
- Copilot workflow
- Human-AI collaboration

#### Key Understanding

Generative AI enables applications to create new content such as text, images, code, audio, and other formats.

Generative AI applications use models trained on large amounts of data and generate outputs based on user prompts, instructions, and available context.

The choice of AI model should be based on the business and technical requirements rather than simply selecting the largest or most powerful model.

Generative AI can support multiple business scenarios including:

- Content generation
- Summarization
- Question answering
- Translation
- Information transformation
- Productivity assistance
- AI-powered conversations
- Task assistance

Microsoft Copilot demonstrates how generative AI can be integrated into existing productivity workflows to assist users with tasks while keeping humans involved in the process.

#### AI PM Perspective

As an AI Project Manager, Generative AI should be approached as a business capability rather than simply a technology.

Important questions include:

- What user problem are we solving?
- Why is Generative AI appropriate?
- What type of content or assistance should the AI provide?
- What information/context does the AI need?
- What level of quality is acceptable?
- How will incorrect or harmful outputs be handled?
- Where should human review remain?
- What privacy and security considerations exist?
- How will success be measured?

A key learning from Copilot-style workflows is that AI can augment human productivity rather than completely replace the human decision-maker.

#### Responsible AI Considerations

Generative AI introduces risks such as:

- Incorrect or misleading outputs
- Harmful content
- Privacy concerns
- Security concerns
- Bias
- Lack of transparency
- Over-reliance on AI-generated information

These risks should be considered during requirements, design, testing, deployment, and monitoring.

#### Day 2 Reflection

The key learning from Day 2 is that Generative AI is most valuable when it is connected to a clear user or business problem. An AI PM should focus not only on what the model can generate, but also on how the capability fits into the user's workflow, how quality will be evaluated, what risks exist, and where humans should remain involved.

---

### Day 3 — 12 August

**Topic:** Large Language Models (LLMs)

**Learning Resource:** Microsoft Learn — Introduction to large language models

**Resource:** https://learn.microsoft.com/en-us/training/modules/introduction-large-language-models/

**Status:** Completed & Validated

#### Topics Completed

* What Large Language Models (LLMs) are
* LLMs and Generative AI
* Neural-network foundation of LLMs
* Model parameters and model size
* Foundation models
* Prompts
* Tokens
* LLM response generation
* Next-token prediction
* Model capabilities and limitations
* Model selection
* Fluency vs factual correctness
* Appropriate and inappropriate LLM use cases

#### Microsoft Learn Assessment

**Status:** Passed

**Achievement:** Earned

#### Day 3 Key Understanding

An LLM is a language-focused AI model trained on large amounts of data to learn patterns and relationships that allow it to process and generate language.

An LLM is a technology component rather than a complete AI product.

Generative AI is broader than LLMs and includes systems capable of generating different types of content such as text, images, audio, video, and code.

#### Important LLM Concepts

**Prompt**

A prompt provides instructions, questions, context, constraints, or other information that guides the model's output.

**Token**

A token is a basic unit of text processed by a language model. Token consumption can affect context usage, cost, and potentially latency.

**Next-token prediction**

At a high level, an LLM generates a response incrementally by predicting possible next tokens and selecting tokens according to the model's output and generation behavior.

#### Foundation Models

A foundation model is a broadly trained model that can serve as a base for multiple downstream applications or tasks.

An LLM can be a foundation model, but the terms are not interchangeable.

#### Model Selection

The largest or most powerful model is not automatically the best model.

An AI PM should consider:

* Required quality
* Accuracy
* Cost
* Latency
* Scale
* Context requirements
* Security
* Privacy
* Reliability
* Business risk
* Operational complexity

#### Fluency vs Accuracy

An LLM can produce fluent and convincing text that is factually incorrect.

Therefore:

**Fluent output ≠ Guaranteed correct output**

AI projects require appropriate evaluation, validation, guardrails, monitoring, and human oversight based on the risk of the use case.

#### AI PM Perspective

The key learning from Day 3 is that selecting an LLM should start with the business problem rather than the model.

A useful AI PM mental model is:

**Business Problem → User / Workflow → AI Capability → Input + Context → Model → Generated Output → Human Review / Action → Evaluation → Business Outcome**

The AI PM must evaluate whether an LLM is actually appropriate and define requirements around quality, cost, latency, security, privacy, scale, risk, and human involvement.

#### Day 3 Validation

Understanding was validated through scenario-based questions covering:

* Model selection for high-volume classification
* AI API cost investigation
* Fluency vs correctness
* Foundation model vs AI product
* High-level AI assistant architecture

**Validation Result:** PASSED

#### Day 3 Reflection

The biggest learning from Day 3 is that an LLM should be treated as a technology capability within an overall AI solution rather than as the product itself.

The AI PM's responsibility is to connect model capabilities with user needs, business requirements, technical constraints, risks, evaluation, and measurable outcomes.

---

### Day 4 — 13 August

**Topic:** Embeddings

**Planned Learning Resource:** To be confirmed from the current Week 1 roadmap before starting Day 4

**Learning Focus:**

* What embeddings are
* Text represented as vectors
* Semantic meaning
* Similarity between embeddings
* Semantic search
* Basic embedding use cases
* Business applications of embeddings
* AI PM requirements and trade-offs

**Learning Status:** Not Started

> Do not document or finalize `04-Embeddings.md` until the topic has been learned and understanding has been validated.

---

### Day 5 — 14 August

**Topic:** RAG Foundation

**Planned Learning Resource:** To be confirmed from the current Week 1 roadmap before starting Day 5

**Learning Focus:**

* Why AI applications need external/contextual information
* Retrieval and generation concepts
* Grounded AI responses
* High-level RAG workflow
* Business use cases
* Data and knowledge requirements
* AI PM considerations

**Learning Status:** Not Started

> Do not document or finalize `05-RAG.md` until the topic has been learned and understanding has been validated.


---

## AI PM Skill Gap

This section will be updated as I assess my current understanding.

| Skill              | Current Understanding | Target Understanding            | Gap |
| ------------------ | --------------------- | ------------------------------- | --- |
| AI Fundamentals    | To assess             | Strong                          | —   |
| LLMs               | To assess             | Strong                          | —   |
| Prompt Engineering | To assess             | Practical                       | —   |
| Embeddings         | To assess             | Strong conceptual understanding | —   |
| RAG                | To assess             | Strong conceptual understanding | —   |
| AI APIs            | To assess             | Working PM knowledge            | —   |
| AI Evaluation      | To assess             | Strong                          | —   |
| AI Governance      | To assess             | Strong                          | —   |
| AI Agents          | To assess             | Strong conceptual understanding | —   |

---

## AI Terminology

This section will be continuously expanded during the week.

| Term             | My Understanding | PM Implication  |
| ---------------- | ---------------- | --------------- |
| AI               | To be completed  | To be completed |
| Machine Learning | To be completed  | To be completed |
| Generative AI    | To be completed  | To be completed |
| LLM              | To be completed  | To be completed |
| Token            | To be completed  | To be completed |
| Context Window   | To be completed  | To be completed |
| Prompt           | To be completed  | To be completed |
| Embedding        | To be completed  | To be completed |
| API              | To be completed  | To be completed |
| Hallucination    | To be completed  | To be completed |
| Evaluation       | To be completed  | To be completed |

---

## Key Learnings

This section will be updated after each learning session.

### Day 1 — AI Fundamentals

**Date:** 10 August 2026

#### Topics Covered

* Generative AI
* Generative AI applications
* LLMs and SLMs
* AI agents
* AI workloads
* Natural Language Processing
* Text analysis
* Speech AI
* Computer vision
* Information extraction
* Responsible AI

#### Key Understanding

Generative AI enables applications to generate new content such as text, images, audio, video, and code based on learned patterns, instructions, prompts, and available context.

A typical GenAI application follows a high-level flow:

**User → Prompt → Application → Model + Context → Generated Output → User**

LLMs are larger language models designed for broad capabilities, while SLMs are smaller models that can provide lower resource requirements and may be suitable for more focused or local/edge scenarios. Model selection should be based on business and technical requirements rather than model size alone.

AI agents extend beyond conversational responses by using models, instructions, and tools to reason about tasks and perform actions. The level of autonomy should be carefully defined based on risk and business requirements.

AI workloads covered include Generative AI, Natural Language Processing, Speech, Computer Vision, and Information Extraction.

Information extraction can transform unstructured data such as documents, images, and recordings into structured information that can be used by downstream business workflows.

Responsible AI principles covered:

* Fairness
* Reliability and Safety
* Privacy and Security
* Inclusiveness
* Transparency
* Accountability

#### AI PM Perspective

The key learning from Day 1 is that AI Project Management requires more than managing development tasks. An AI PM must understand the relationship between the business problem, AI capability, data/context, model, user experience, risks, evaluation, and business outcome.

For AI features, important PM questions include:

* Why is AI required for this problem?
* Which AI workload is appropriate?
* What data or context does the system require?
* What level of AI quality is acceptable?
* What happens when the AI is incorrect?
* What level of human involvement is required?
* What responsible AI risks must be addressed?
* How will the feature be evaluated?
* What business outcome should improve?

#### Personal Reflection

The biggest shift in my understanding is that AI should not be treated simply as another software component. AI systems introduce probabilistic outputs, model limitations, data dependencies, evaluation requirements, and responsible AI considerations that need to be incorporated into project planning from the beginning.


### Day 2

*To be completed.*

### Day 3

*To be completed.*

### Day 4

*To be completed.*

### Day 5

*To be completed.*

---

## Practical Exercises

### Exercise 1 — AI Fundamentals

*To be completed.*

### Exercise 2 — LLM Understanding

*To be completed.*

### Exercise 3 — Prompt Library

*To be completed.*

### Exercise 4 — Embedding / Semantic Search

*To be completed.*

### Exercise 5 — AI Evaluation

*To be completed.*

---

## Questions & Unknowns

Questions discovered during the week:

* [ ]
* [ ]
* [ ]

---

## Resources

Learning resources used during the week:

*
*
*
*

---

## Weekly Assessment

### Can I explain AI fundamentals?

* [ ] AI
* [ ] ML
* [ ] GenAI
* [ ] LLM
* [ ] Training vs inference

### Can I explain LLM fundamentals?

* [ ] Tokens
* [ ] Context windows
* [ ] Inference
* [ ] Model limitations

### Can I explain modern AI concepts?

* [ ] Prompting
* [ ] Embeddings
* [ ] Semantic search
* [ ] AI APIs
* [ ] Hallucinations

### Can I think like an AI PM?

* [ ] Define AI use cases
* [ ] Identify AI risks
* [ ] Define evaluation metrics
* [ ] Understand technical trade-offs
* [ ] Define human-in-the-loop requirements

---

## Week 1 Practical Deliverable

### AI Project Assistant

Build a conceptual AI PM case study for an AI assistant that helps Project Managers with:

* Project status summaries
* Risk identification
* Meeting summaries
* Action-item extraction
* Project questions
* Next-step recommendations

Detailed documentation will be added after completing the week's learning.

---

## Week 1 Retrospective

### What I learned

*To be completed.*

### What became clearer

*To be completed.*

### What I still don't understand

*To be completed.*

### What I need to revisit

*To be completed.*

### How this applies to AI Project Management

*To be completed.*

---

Completion Status

Week 1: In Progress

Start Date: 10 August 2026

End Date: 14 August 2026

Overall Completion: 60%

Completed: 3 / 5 days

Current Checkpoint: Day 3 — LLM Foundations completed and validated

Next: Day 4 — Embeddings

---

> This document is a living weekly record. It will be updated throughout the week as learning progresses.
