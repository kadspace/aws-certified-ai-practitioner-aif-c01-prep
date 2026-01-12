# Cheat Sheet & Metrics - Quiz 1

**Instructions:**
Focus on mapping "Concepts" to "AWS Services" and selecting the right "Metric" for the job.

---

### Question 1
You are training a model to detect fraudulent credit card transactions. 99.9% of transactions are legitimate, and only 0.1% are fraud.
You train a model that effectively just guesses "Legitimate" every single time. It achieves 99.9% Accuracy.

Why is **Accuracy** a bad metric here, and what should you use instead?

A) Accuracy is fine; 99.9% is excellent.
B) Accuracy is misleading for imbalanced classes. You should use **F1 Score** (or Area Under PR Curve) to balance Precision and Recall.
C) You should use **ROUGE-N** to see if the model summarized the transaction correctly.
D) You should use **RMSE** to measure the price difference.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: F1 Score is the standard metric for Class Imbalance problems. It forces the model to prove it can actually find the "needle in the haystack" (Precision/Recall).
*   **A (Wrong)**: The model is useless (it catches 0 fraud), despite high accuracy.
</details>

---

### Question 2
You are building an app that translates English technical manuals into Japanese. You want to automatically score how good the translation is compared to a human translator's version.

Which metric is the industry standard for **Machine Translation**?

A) ROUGE-L
B) BLEU
C) Perplexity
D) Recall

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: BLEU (BiLingual Evaluation Understudy) measures n-gram precision overlap. It is the king of Translation metrics.
*   **A (Wrong)**: ROUGE is typically for *Summarization* (Recall-oriented).
</details>

---

### Question 3
Use your "Service Translation" skills:
You need a service to **store vector embeddings** so your RAG agent can search them. You do not want to manage any servers.

What is the AWS service name?

A) Amazon SageMaker Feature Store
B) Amazon OpenSearch Serverless (Vector Engine)
C) Amazon Kendra
D) Amazon DynamoDB

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: OpenSearch Serverless is the primary "Vector DB" for Bedrock RAG.
*   **C (Wrong)**: Kendra is an "Enterprise Search" engine (document crawler), not a raw vector store for RAG embeddings.
</details>

---

### Question 4
Use your "Service Translation" skills:
You have a dataset of 10,000 raw PDFs. You need a **human workforce** to highlight specific clauses in them to create a "Gold Standard" training set for your custom entity recognition model.

What is the AWS service name?

A) Amazon Mechanical Turk
B) Amazon SageMaker Ground Truth
C) Amazon Macie
D) Amazon Bedrock Agents

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Ground Truth is the specialized service for managing labeling workflows (Private, Public, or Vendor workforces) for ML data.
</details>

---

### Question 5
You are evaluating a text summarization model. You want to know how much of the "key information" from the reference summary appeared in the generated summary.

Which metric focuses on **Recall** (completeness) of the summary?

A) BLEU
B) ROUGE
C) RMSE
D) Accuracy

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: ROUGE (Recall-Oriented Understudy...) is named for Recall. It penalizes you if you miss important words.
</details>
