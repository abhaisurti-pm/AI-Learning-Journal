# AI Fundamentals — Quick Reference (PM Notes)

## Overview

Artificial Intelligence enables software systems to perform tasks that normally require human intelligence, including understanding language, analyzing images, processing speech, extracting information, generating content, and supporting automated workflows.

From an AI Project Management perspective, understanding AI fundamentals helps translate business problems into appropriate AI capabilities while considering data, models, risks, evaluation, responsible AI, and business outcomes.

## Artificial Intelligence

Artificial Intelligence is the broader field of creating systems that can perform tasks that typically require human intelligence.

Examples include:

- Understanding language
- Recognizing images
- Processing speech
- Extracting information
- Generating content
- Supporting decisions
- Automating tasks

### AI PM Perspective

An AI PM should start with the business problem rather than the technology.

Key question:

> What problem are we solving, and does AI provide a meaningful advantage over traditional software?

### What is Generative AI?
AI that creates new content — text, images, audio, video, or code — based on patterns it learned during training, plus the prompt and context it's given.

### How does a GenAI application work at a high level?
User sends a prompt → application passes it to the AI model along with any context → model generates output → application returns it to the user.

### LLM vs SLM?
| Factor | LLM | SLM |
|---|---|---|
| Model scale | Larger | Smaller |
| Capability | Broad | More focused |
| Resources needed | Higher | Lower |
| Latency | Can be higher | Can be lower |
| Deployment | Usually cloud/API | Can work on-device/edge |
| Cost | Higher | Lower |

Bigger isn't automatically better — the right choice depends on capability, cost, latency, privacy, and deployment needs.

### What makes an AI agent different from a chatbot?
A chatbot just answers questions. An agent reasons about a goal, picks the right tool, takes an action, checks the result, and keeps going until the task is done.

### What are the three key components of an agent?
1. **Model** – the reasoning engine
2. **Instructions** – the goal/guidance it's given
3. **Tools** – knowledge tools (search, databases, docs) and action tools (send email, update records, trigger workflows)

### What are the major AI workloads?
Generative AI, Natural Language Processing, Speech, Computer Vision, and Information Extraction. Pick the workload based on the business problem, not the other way around.

### What is information extraction?
Pulling useful, structured information out of unstructured sources (documents, scanned forms, images, audio, video) so it can feed into a business process — e.g., automated form processing or expense claims.

### What are the six Responsible AI principles?
1. **Fairness** – could different groups get different outcomes?
2. **Reliability & Safety** – what happens when the AI is wrong?
3. **Privacy & Security** – what data is used, who can access it?
4. **Inclusiveness** – can all users effectively use the system?
5. **Transparency** – do users know when/how AI is being used?
6. **Accountability** – who owns the system and its outcomes?

---
*Source: Microsoft Learn — Introduction to AI Concepts*
