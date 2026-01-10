# Domain 4: Guidelines for Responsible AI - Quiz 1

**Instructions:**
Scenario-based questions focusing on safety, bias, and compliance.

---

### Question 1
A financial institution is using an LLM to generate summaries of customer service calls. However, they are strictly regulated and must ensure that **no** Personally Identifiable Information (PII) such as names or social security numbers ever appears in the generated summaries.

What is the most direct and managed way to enforce this in Amazon Bedrock?

A) Add a line to the system prompt saying "Do not output any PII."
B) Configure a Guardrail with a "Sensitive Information Filter" to detect and redaction/block PII types.
C) Use AWS Macie to scan the output bucket after the summaries are saved.
D) Fine-tune the model on a dataset that has no PII.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Bedrock Guardrails has built-in PII filtering that intercepts the model response *before* it returns to the application. It's distinct from the model itself.
*   **A (Wrong)**: Prompting is not 100% reliable for compliance (jailbreaks happen).
*   **C (Wrong)**: This is "after the fact" detection, not prevention. The PII would have already been generated.
</details>

---

### Question 2
You are training a model to approve loan applications. You notice that the training data contains 90% applications from one specific demographic and only 10% from others. You are concerned the model will learn this imbalance.

Which AWS service feature should you use to detect this **pre-training bias**?

A) Amazon Inspector
B) Amazon SageMaker Clarify
C) Amazon Augmented AI (A2I)
D) AWS CloudTrail

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: SageMaker Clarify is specifically designed to detect bias in data (pre-training) and models (post-training/inference), and also provides explainability.
*   **C (Wrong)**: A2I is for human review of low-confidence predictions.
</details>

---

### Question 3
An online community wants to build a chatbot but ensures it refuses to engage in "Hate" or "Sexual" content. They also want to ensure the bot does not provide financial investment advice.

Which configuration in Amazon Bedrock Guardrails addresses these needs?

A) Use "Content Filters" for Hate/Sexual and "Denied Topics" for financial advice.
B) Use "Word Filters" for financial terms.
C) Use "Contextual Grounding Check" for the Hate speech.
D) It is impossible to block topics; you must trust the model.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** A

**Explanation:**
*   **A (Correct)**: Content Filters are category-based (Hate, Abuse, etc.). "Denied Topics" is a feature where you describe a topic in natural language (e.g., "Financial Advice") and the guardrail blocks it.
</details>

---

### Question 4
Your detailed RAG application sometimes creates answers that sound plausible but are not actually found in the source documents retrieved from the Knowledge Base.

Which Guardrail feature specifically targets this issue?

A) Sensitive Information Filter
B) Word Filters
C) Contextual Grounding Check
D) Prompt Attack Filter

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: Contextual Grounding Check evaluates if the response is supported by the source data (Grounding) and relevant to the user's query (Relevance), specifically filtering out hallucinations.
</details>

---

### Question 5
You are reviewing the "AWS AI Service Cards" for a specific service. What is the primary purpose of these documents?

A) To provide pricing details and SLA guarantees.
B) To provide code snippets and API references.
C) To provide transparent information about the intended use cases, limitations, and responsible AI design choices of the service.
D) To list the names of the engineers who built the model.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: AI Service Cards are "nutrition labels" for AI, promoting transparency and responsible use.
</details>
