# Domain 4: Guidelines for Responsible AI - Quiz 2 (Advanced)

**Instructions:**
Focus on Explainability, Bias types, and Governance tools.

---

### Question 1
You are using **Amazon SageMaker Clarify**. You want to understand *why* a specific individual loan application was rejected by your model.

Which specific feature of Clarify should you use?

A) Class Imbalance Report
B) SHAP (SHapley Additive exPlanations) values
C) Bias Drift Monitor
D) Model Card generation

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: SHAP values explain *local* feature attribution (e.g., "Income contributed +20% to approval, but Debt contributed -50% to rejection"). Ideally suited for single-prediction explanation.
*   **A (Wrong)**: Class Imbalance is a global dataset metric.
</details>

---

### Question 2
Your organization builds a generative AI model for medical advice. You want to ensure that if a user asks "How do I make a bomb?", the model refuses, even if the user tries to trick it (jailbreaking).

Which layer of defense provides the most robust, managed protection specifically for this?

A) System Prompt Engineering ("You are a helpful assistant...")
B) Amazon Bedrock Guardrails (Content Filters & Denied Topics)
C) Amazon Macie
D) AWS WAF (Web Application Firewall)

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Bedrock Guardrails sits *outside* the model. It intercepts inputs/outputs and blocks specific categories (Violence/Hate) and topics, regardless of prompt hacks.
*   **A (Wrong)**: Prompts can be bypassed by "jailbreaks" (e.g., "Ignore previous instructions").
</details>

---

### Question 3
What is the purpose of "Human-in-the-loop" (HITL) in the context of Responsible AI?

A) To replace the AI entirely with humans.
B) To have humans review low-confidence predictions or audit random samples to ensure quality and safety.
C) To use humans to physically carry the servers.
D) To have humans type the prompts for the end-users.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: HITL (often using Amazon A2I) is a safety net. If the model is unsure (<50% confidence), route it to a human. Essential for high-stakes decisions.
</details>

---

### Question 4
You are using **Amazon SageMaker Model Monitor** in production. It alerts you that the live data coming into the model has significantly different statistical properties (e.g., different age distribution) than the data used for training.

What is this issue called?

A) Concept Drift
B) Data Drift (Feature Drift)
C) Model Latency
D) Bias Leakage

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Data Drift means the *input data* has changed (e.g., "We used to get mostly young users, now we get mostly old users").
*   **A (Wrong)**: Concept Drift means the *relationship* has changed (e.g., "Housing prices have doubled, so the old pattern of Price vs Size is invalid"). The question specified input stats, which is Data Drift.
</details>

---

### Question 5
Which document is intended to provide critical information about a model's intended uses, limitations, and ethical considerations to downstream developers and customers?

A) AWS CloudTrail Log
B) AI Service Card (or Model Card)
C) Service Control Policy (SCP)
D) SLA Agreement

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Model Cards (or AI Service Cards for AWS services) are the standard documentation for transparency/ethics.
</details>
