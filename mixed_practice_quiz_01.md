# Comprehensive Mock Exam - Quiz 1

**Instructions:**
This quiz mixes questions from all 5 domains to simulate the real exam environment.

---

### Question 1 (Domain 2)
A marketing team wants to generatively create ad copy. They want to provide the model with 5 examples of their brand's tone of voice in the prompt to ensure the output matches their style.

What is this technique called?

A) Fine-tuning
B) Zero-shot prompting
C) Few-shot prompting
D) RAG

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: Giving a few examples (1-5) in the prompt context is the definition of "Few-shot prompting".
*   **A (Wrong)**: Fine-tuning changes the model weights, it's not prompting.
</details>

---

### Question 2 (Domain 5)
An organization wants to prevent any user from ever making a public Amazon S3 bucket, as this could expose training data.

Which AWS service allows you to set a **guardrail** rule that continuously monitors and flags if an S3 bucket is compliant with encryption and public access settings?

A) AWS CloudTrail
B) Amazon GuardDuty
C) AWS Config
D) Amazon Macie

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: AWS Config is the specific service for "Compliance as Code". It checks *configurations* (encryption on? public access off?) against rules.
*   **A (Wrong)**: CloudTrail logs *who* made it public, but doesn't maintain the "state" of compliance.
</details>

---

### Question 3 (Domain 3)
You are building an application that uses Amazon Bedrock. You need to chain together multiple prompts: first to summarize an email, then to extract action items, and finally to format them as JSON.

Which Bedrock feature orchestrates this workflow most simply?

A) Knowledge Bases for Amazon Bedrock
B) Agents for Amazon Bedrock
C) Prompt Flows (Amazon Bedrock)
D) SageMaker Pipelines

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: Prompt Flows (recently added to Bedrock) is a visual builder to chain prompts and logic together.
*   **B (Incorrect)**: Agents are for calling external tools. While they *can* chain steps, Prompt Flows is the specific low-code orchestrator for prompt sequencing.
</details>

---

### Question 4 (Domain 4)
You are using SageMaker Clarify to evaluate a model. You see a metric called "Class Imbalance" in your pre-training report.

What does this indicate?

A) The model is hallucinating 90% of the time.
B) The Training Data has significantly more examples of one category than another (e.g., 90% "Approved", 10% "Rejected").
C) The inference latency is higher for one class than another.
D) The model is overfitted.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Class Imbalance is a *data* bias metric. It means your training set isn't representative, which leads to biased predictions.
</details>

---

### Question 5 (Domain 1)
Which of the following is an example of **Unsupervised Learning**?

A) Training a model to predict house prices based on historical sales data (Price, SqFt, Zip Code).
B) Training a spam filter using a dataset of emails marked "Spam" or "Not Spam".
C) Feeding a customer database into an algorithm to group customers into 5 distinct "segments" based on purchasing behavior, without knowing the segments beforehand.
D) Teaching a robot to walk by rewarding it when it stays upright.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: Clustering (Customer Segmentation) is the classic Unsupervised use case. You don't know the labels (segments) ahead of time; the AI finds them.
*   **A (Supervised - Regression)**.
*   **B (Supervised - Classification)**.
*   **D (Reinforcement)**.
</details>
