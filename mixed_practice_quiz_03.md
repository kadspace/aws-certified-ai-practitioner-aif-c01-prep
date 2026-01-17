# Mixed Practice Exam - Quiz 3 (Exam Simulator)

**Instructions:**
This quiz is designed to mimic the phrasing and difficulty of the actual AWS Certified AI Practitioner (AIF-C01) exam. 
*   **Questions**: 10
*   **Passing Score**: 7/10 (70%)
*   **Target Score**: 9/10 (90%)

---

### Question 1 (Domain 1: Fundamentals)
A business analyst with no coding experience wants to build a machine learning model to predict customer churn using a CSV file exported from their CRM. They need a visual, drag-and-drop interface.
Which AWS service should they use?
A) Amazon SageMaker Studio
B) Amazon SageMaker Canvas
C) Amazon SageMaker Ground Truth
D) Amazon Comprehend

<details><summary>View Answer</summary>

**Correct: B (SageMaker Canvas)**. Canvas is the specific "No-Code" visual interface for business analysts. Studio is for developers/data scientists.
</details>

---

### Question 2 (Domain 2: Generative AI)
A developer is building a creative writing assistant using Amazon Bedrock. They want the model to be highly creative and diverse in its word choices, even if it occasionally becomes less predictable.
Which combination of inference parameters should they adjust?
A) Decrease Temperature and Increase Top-P
B) Increase Temperature and Increase Top-P
C) Set Temperature to 0 and Decrease Top-K
D) Increase Stop Sequences

<details><summary>View Answer</summary>

**Correct: B**. Increasing Temperature and Top-P both increase the "randomness" and diversity of the output, making it more "creative."
</details>

---

### Question 3 (Domain 3: Applications)
A legal firm has 10,000 internal case files that change daily. They want their AI chatbot to answer questions based *only* on these files. They want the most cost-effective solution that handles the daily updates without retraining the model.
Which approach is best?
A) Fine-tuning a Foundation Model
B) Continued Pre-training
) Retrieval Augmented Generation (RAG)
D) Prompt Engineering with Zero-Shot learning

<details><summary>View Answer</summary>

**Correct: C (RAG)**. RAG is the best for frequently changing data because you just update the vector database (Knowledge Base), you don't have to retrain or fine-tune the model.
</details>

---

### Question 4 (Domain 4: Responsible AI)
A company is concerned that their new loan approval model might be biased against certain zip codes. They want to generate a report that explains which features (like income, credit score, or location) contributed most to the model's decisions.
Which tool should they use?
A) Amazon Macie
B) Amazon SageMaker Clarify
C) Amazon Inspector
D) AWS Artifact

<details><summary>View Answer</summary>

**Correct: B (SageMaker Clarify)**. Clarify is the tool for detecting bias and providing "Explainability" (Feature Attribution/SHAP values).
</details>

---

### Question 5 (Domain 5: Security & Compliance)
Under the AWS Shared Responsibility Model, when using **Amazon Bedrock**, which of the following is the responsibility of the **Customer**?
A) Managing the physical security of the data centers
B) Patching the underlying operating system of the model servers
C) Protecting the data sent to the model and managing IAM permissions
D) Developing the base Foundation Models (e.g., Claude or Titan)

<details><summary>View Answer</summary>

**Correct: C**. AWS manages the infrastructure and the models themselves in Bedrock (Serverless). The customer is always responsible for their own data and access control (IAM).
</details>

---

### Question 6 (Domain 3: Applications)
When configuring an **Agent for Amazon Bedrock**, what is the primary purpose of an **Action Group**?
A) To store the vector embeddings of the company's documents
B) To define the set of APIs the agent can call to perform tasks (via Lambda)
C) To select which Foundation Model the agent uses
D) To redact PII from the user's prompt

<details><summary>View Answer</summary>

**Correct: B**. Action Groups connect the Agent's "reasoning" to actual "actions" (calling APIs via AWS Lambda).
</details>

---

### Question 7 (Domain 1: Fundamentals)
A retail company wants to group its customers into different "segments" based on their purchasing patterns (e.g., "Budget Shoppers," "Luxury Buyers," "Frequent Small Buyers"). They do not have any pre-existing labels for these groups.
What type of machine learning is this?
A) Supervised Learning
B) Unsupervised Learning (Clustering)
C) Reinforcement Learning
D) Deep Learning

<details><summary>View Answer</summary>

**Correct: B**. Clustering (grouping data without labels) is a classic Unsupervised Learning task.
</details>

---

### Question 8 (Domain 2: Generative AI)
A company notices their chatbot is "hallucinating" facts about products that don't exist. They want to implement a check that verifies if the model's response is actually supported by the source documents provided in the prompt.
Which feature of **Guardrails for Amazon Bedrock** should they use?
A) Content Filters
B) Sensitive Information Filters (PII)
C) Contextual Grounding Checks
D) Denied Topics

<details><summary>View Answer</summary>

**Correct: C**. Contextual Grounding checks specifically verify if the output is "grounded" in the provided source text to prevent hallucinations.
</details>

---

### Question 9 (Domain 5: Security & Compliance)
A global organization wants to ensure that no developer in their AWS Organization can use AI services in any region other than `us-east-1` and `eu-west-1` for compliance reasons.
What is the most efficient way to enforce this across all accounts?
A) Individual IAM Policies on every user
B) Service Control Policies (SCPs) applied at the Organization Root
C) Security Groups
D) VPC Endpoints

<details><summary>View Answer</summary>

**Correct: B**. SCPs are the only way to enforce "Guardrails" across an entire AWS Organization, regardless of individual IAM permissions.
</details>

---

### Question 10 (Domain 3: Applications)
You are evaluating two different models for a summarization task. You want to measure the "Semantic Similarity" (meaning) between the generated summary and a human-written reference, rather than just looking for exact word overlaps.
Which metric is most appropriate?
A) ROUGE
B) BLEU
C) BERTScore
D) F1 Score

<details><summary>View Answer</summary>

**Correct: C**. BERTScore uses embeddings to check for **meaning** (semantics). ROUGE and BLEU only check for literal word/n-gram overlaps.
</details>
