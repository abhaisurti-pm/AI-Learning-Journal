# Large Language Models (LLMs)

## 1. What is an LLM?

A Large Language Model (LLM) is an AI model designed primarily to process and generate human language.

LLMs are trained on very large datasets and learn statistical patterns and relationships in language. These learned patterns allow them to perform tasks such as:

* Question answering
* Summarization
* Translation
* Text generation
* Information extraction
* Conversational interactions
* Code generation
* Language-related classification tasks

A useful AI Project Manager mental model is:

> An LLM is an extremely sophisticated language prediction system that generates useful outputs based on the input, context, and patterns learned during training.

An LLM is a technology component, not automatically a complete AI product.

---

## 2. LLMs and Generative AI

Generative AI is the broader category of AI systems capable of generating new content.

Generative AI can produce:

* Text
* Images
* Audio
* Video
* Code
* Other forms of generated content

LLMs are one important class of models used for language-related generative AI applications.

Therefore:

> Generative AI is broader than LLMs.

Not every Generative AI system is an LLM, and modern language models may also support multimodal capabilities.

---

## 3. LLMs and Neural Networks

LLMs are based on neural-network architectures.

At a conceptual level:

**Input → Neural Network Processing → Output**

Modern LLMs commonly use transformer-based architectures.

The AI Project Manager does not need to understand the mathematical details of neural networks at this stage.

The important understanding is that the model learns patterns from training data and uses those learned patterns to process inputs and generate outputs.

---

## 4. Model Parameters

LLMs contain a very large number of learned parameters.

Parameters are values learned during model training that influence how the model processes information and generates predictions.

Model size is often discussed in:

* Millions (M)
* Billions (B)
* Trillions (T)

A larger parameter count can provide greater model capacity, but:

> A larger model is not automatically the best model for every business problem.

AI PMs must consider model capability together with:

* Cost
* Latency
* Accuracy
* Scale
* Reliability
* Security
* Operational requirements

---

## 5. Foundation Models

A foundation model is a broadly trained model that can serve as a base for many downstream tasks or applications.

Foundation models can be adapted or specialized through approaches such as prompting, additional training, or other forms of customization.

An LLM can be a foundation model, but the terms are not interchangeable.

Mental model:

**Foundation Model → Broadly trained base capability → Multiple downstream applications**

An AI PM should distinguish between:

* The underlying model
* The AI application built using the model
* The business workflow in which the application operates

---

## 6. Prompts

A prompt is the input provided to an AI model to guide its response.

A prompt can contain:

* Instructions
* Questions
* Context
* Data
* Constraints
* Desired output format

Example:

> Summarize these meeting notes into three bullet points. Focus only on decisions and action items.

For AI projects, prompt requirements can affect:

* Output quality
* Consistency
* User experience
* Token consumption
* Cost
* Evaluation criteria

---

## 7. Tokens

A token is a basic unit of text processed by a language model.

Depending on the language and content, a token may represent:

* Part of a word
* A complete word
* Punctuation
* Other pieces of text

Tokens matter to AI Project Managers because token consumption can influence:

### Cost

Many AI APIs price usage based partly on input and output tokens.

### Context

Models have limits on how much information can be processed within a particular interaction.

### Latency

Generating larger amounts of output can increase response time.

Therefore, token usage can become an important product and engineering consideration at scale.

---

## 8. How LLMs Generate Responses

At a high level:

**User Input → Tokenization → Model Processing → Probability Distribution → Token Selection → Repeat → Generated Response**

LLMs generate output incrementally, generally predicting one token at a time.

The model assigns probabilities to possible next tokens. The generation process then selects tokens according to the model's output and configured generation behavior.

This means LLM output is not equivalent to retrieving a guaranteed fact from a database.

---

## 9. Fluency Does Not Equal Accuracy

An LLM can produce highly fluent, convincing and grammatically correct text that is still factually incorrect.

Therefore:

> A convincing AI response should not automatically be treated as a correct response.

AI projects need appropriate:

* Evaluation
* Validation
* Guardrails
* Human oversight
* Monitoring

The required controls should depend on the risk of the use case.

---

## 10. Choosing the Right Model

The largest or most powerful model is not automatically the best model.

Model selection should consider:

* Required quality
* Accuracy
* Latency
* Cost
* Scale
* Context requirements
* Security
* Privacy
* Reliability
* Business risk
* Operational complexity

An AI PM should ask:

> What is the minimum model capability required to meet the business and user requirements?

The goal is not to select the most powerful model.

The goal is to select an appropriate model that satisfies the product requirements within the project's constraints.

---

## 11. When to Use an LLM

LLMs are particularly useful for problems involving natural language and unstructured information.

Examples include:

* Customer-support summarization
* Document summarization
* Question answering
* Content generation
* Conversational assistants
* Draft generation
* Translation
* Natural-language interfaces

However, an LLM should not automatically be selected simply because a problem contains text.

The AI PM must first understand:

* The business problem
* User workflow
* Accuracy requirement
* Risk
* Data requirements
* Security requirements
* Expected scale
* Cost constraints
* Latency requirements

---

## 12. AI PM Mental Model

The LLM is only one component of an AI solution.

A useful AI PM mental model is:

**Business Problem → User / Workflow → AI Capability → Input + Context → Model → Generated Output → Human Review / Action → Evaluation → Business Outcome**

The AI PM is responsible for ensuring that the technology actually solves the intended business problem.

---

## 13. Example — Internal HR Policy Assistant

Business requirement:

> Employees need an AI assistant that answers questions using approved internal HR policies.

A high-level solution could involve:

**User Query → Safety / Intent Check → Find Relevant Approved Policy Information → Provide Relevant Context to the AI → Generate Answer → Verify / Evaluate Answer → Return Answer → Log Feedback and Quality Signals**

Important requirements would include:

* Approved data sources
* Data freshness
* Access permissions
* Privacy and security
* Accuracy expectations
* Escalation when the AI cannot answer reliably
* Monitoring and evaluation

The AI PM should define these requirements before simply selecting an LLM.

---

## 14. Key AI PM Takeaways

1. An LLM is a technology component, not automatically a complete product.
2. Generative AI is broader than LLMs.
3. LLMs learn patterns from large datasets and use them to generate language.
4. Prompts provide instructions and context to guide model behavior.
5. Tokens affect context, cost and potentially latency.
6. LLMs generate responses incrementally through next-token prediction.
7. Fluency does not guarantee factual correctness.
8. The largest model is not automatically the best model.
9. Model selection must consider business and technical constraints.
10. AI solutions require more than the model itself.
11. Risk, privacy, security, human oversight and evaluation must be considered according to the use case.
12. The AI PM's responsibility is to connect AI capability to measurable business outcomes.

---

## 15. AI PM Question to Remember

> **What business problem are we solving, what AI capability is actually required, and what constraints determine whether this model is appropriate?**
