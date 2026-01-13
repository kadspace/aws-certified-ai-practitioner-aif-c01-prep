# AWS Certified AI Practitioner - Graduation Mock Exam

**Instructions:**
This is the final hurdle. 20 Questions covering all domains. Treat this like the real exam.
*   **Passing Score**: 14/20 (70%)
*   **Target Score**: 17+/20 (85%)

---

### Domain 1: Fundamentals of AI/ML

**Q1.** A researcher wants to train a model to recognize rare bird species. They have 1,000 images, but only 50 are labeled with the bird name. They want to use the 950 unlabeled images to help the model learn the general structure of bird features.
What type of learning is this?
A) Supervised Learning
B) Unsupervised Learning
C) Semi-Supervised Learning
D) Reinforcement Learning

<details><summary>View Answer</summary>

**Correct: C (Semi-Supervised)**. Uses a small amount of labeled data + large amount of unlabeled data.
</details>

**Q2.** Which AWS service allows you to launch a JupyterLab environment to build models, but provides a "No-Code" visual interface for business analysts to build models in the same domain?
A) Amazon SageMaker Studio
B) Amazon Bedrock
C) AWS Cloud9
D) Amazon Inspector

<details><summary>View Answer</summary>

**Correct: A (SageMaker Studio)**. Studio includes both "JupyterLab" (for coders) and "Canvas" (No-code), often in the same unified interface (formerly separate, now converging).
</details>

**Q3.** You need to identify the Correlation between "House Size" and "House Price".
Which matrix helps visualize this?
A) Confusion Matrix
B) Scatter Plot / Correlation Matrix
C) F1 Score
D) ROC Curve

<details><summary>View Answer</summary>

**Correct: B**. Confusion Matrix and F1 are for Classification (Categories), not continuous logic like Price.
</details>

---

### Domain 2: Generative AI Fundamentals

**Q4.** You are using a Diffusion Model. What is the primary input and output?
A) Input: Text. Output: Text.
B) Input: Text/Image. Output: Image.
C) Input: Audio. Output: Text.
D) Input: Table. Output: Number.

<details><summary>View Answer</summary>

**Correct: B**. Diffusion models (like Stable Diffusion/Titan Image) generate Images.
</details>

**Q5.** Which inference parameter essentially "cuts off" the tail of unlikely word choices, forcing the model to pick from only the top X% of probable next words?
A) Temperature
B) Top-P (Nucleus Sampling)
C) Top-K
D) Stop Sequence

<details><summary>View Answer</summary>

**Correct: B (Top-P)**. It creates a dynamic pool of words that adds up to P% probability (e.g., 0.9).
</details>

**Q6.** What is the most effective way to adapt a foundation model to your company's specific "Tone of Voice" without extensive retraining?
A) Pre-training
B) Instruction Fine-Tuning
C) Prompt Engineering (Few-Shot)
D) RAG

<details><summary>View Answer</summary>

**Correct: C (Few-Shot)**. Giving the model 3-5 examples of your "Tone" in the prompt is usually enough for style copying. Fine-tuning (B) is powerful but expensive/slow compared to just prompting.
</details>

**Q7.** You are building a chatbot using Amazon Bedrock. You need to ensure the chatbot *never* answers questions about your competitor, "Acme Corp".
A) System Prompt
B) Guardrails for Amazon Bedrock (Denied Topics)
C) AWS WAF
D) Security Groups

<details><summary>View Answer</summary>

**Correct: B**. Guardrails are the dedicated, managed way to block specific topics reliably.
</details>

---

### Domain 3: Applications of Foundation Models

**Q8.** You have a large amount of documentation in S3. You want to implement RAG. You need a service to turn the text into Vector Embeddings.
Which model type do you need?
A) Text Generation Model (e.g., Llama 3)
B) Text Embedding Model (e.g., Titan Embeddings)
C) Image Generation Model
D) Classification Model

<details><summary>View Answer</summary>

**Correct: B**. You need an *Embedding* model to turn text into vectors. A Generation model (A) creates text, it doesn't create vectors for storage.
</details>

**Q9.** Your RAG application is retrieving the correct document, but the LLM is answering "I don't know" because the document is too long to fit in the context window.
What is the solution?
A) Increase Top-K
B) Chunking
C) Increase Temperature
D) Use a smaller model

<details><summary>View Answer</summary>

**Correct: B**. You must split (chunk) the document into smaller pieces so the relevant piece fits in the prompt.
</details>

**Q10.** What is the unique capability of an **Agent** compared to a standard **Chatbot**?
A) Agents have memory.
B) Agents can execute multi-step workflows and call APIs (Action Groups) to perform tasks.
C) Agents run faster.
D) Agents are cheaper.

<details><summary>View Answer</summary>

**Correct: B**. The definition of an Agent is "Reasoning + Action".
</details>

**Q11.** You want to evaluate strictly the "Fluency" and "Coherence" of your LLM's responses. You don't have a ground truth dataset.
Which metric is suitable?
A) ROUGE
B) Perplexity
C) Accuracy
D) F1 Score

<details><summary>View Answer</summary>

**Correct: B**. Perplexity measures how "natural" or confident the model is with the language. It doesn't check for facts, just fluency.
</details>

---

### Domain 4: Responsible AI

**Q12.** You are examining a model's performance on loan approvals. You notice that for Group A (Age < 25), the False Negative rate is 50%. For Group B (Age > 25), the False Negative rate is 5%.
What type of bias is this?
A) Temporal Bias
B) Disparate Impact / Demographic Parity issues
C) Confirmation Bias
D) Availability Bias

<details><summary>View Answer</summary>

**Correct: B**. The model performs significantly differently across demographic groups.
</details>

**Q13.** Which AWS tool would you use to create a PDF report detailing accuracy, bias, and explainability metrics for your compliance team?
A) Amazon QuickSight
B) Amazon SageMaker Clarify
C) AWS Artifact
D) Amazon Inspector

<details><summary>View Answer</summary>

**Correct: B**. Clarify generates these specific ML reports.
</details>

**Q14.** You are concerned that your model might be memorizing PII from the training data.
Which attack helps you test this?
A) Model Inversion / Membership Inference
B) Prompt Injection
C) DDoS
D) Man-in-the-Middle

<details><summary>View Answer</summary>

**Correct: A**. These attacks try to reverse-engineer ("Invert") the model to see if a specific person's data was in the training set.
</details>

---

### Domain 5: Security & Compliance

**Q15.** Which encryption method ensures that AWS *never* sees your encryption keys in plaintext, and you manage the key material outside of AWS entirely?
A) SSE-S3
B) SSE-KMS
C) CSE (Client-Side Encryption)
D) SSE-KMS with External Key Store (XKS)

<details><summary>View Answer</summary>

**Correct: C**. "Outside of AWS entirely" usually points to Client-Side Encryption (you encrypt it *before* you send it). XKS (D) is also a strong candidate, but C is the most absolute "AWS never sees the key" definition in standard contexts. *Note: On the test, look for "Control"* -> *KMS CMK*. Look for *"AWS has zero access ever"* -> *Client Side*.
</details>

**Q16.** A developer tries to delete a Production Knowledge Base in Amazon Bedrock. They receive an "Access Denied" error. You check their IAM role, and they have `AdministratorAccess`.
What could be blocking them?
A) Security Group
B) Network ACL
C) Service Control Policy (SCP) at the Organization root
D) The service is down

<details><summary>View Answer</summary>

**Correct: C**. SCPs override Admin permissions.
</details>

**Q17.** You need to securely connect your VPC to Amazon Bedrock without using the public internet.
A) Internet Gateway
B) NAT Gateway
C) VPC Endpoint (PrivateLink)
D) VPN

<details><summary>View Answer</summary>

**Correct: C**. Standard answer for private AWS-to-AWS connectivity.
</details>

**Q18.** Who is responsible for "Curating the Training Data" for a custom model built on SageMaker?
A) AWS
B) The Customer
C) Shared
D) No one

<details><summary>View Answer</summary>

**Correct: B**. Under the Shared Responsibility Model, *Data* is always the Customer's responsibility.
</details>

**Q19.** Which document provides information about the alignment of AWS services with ISO 27001 standards?
A) AWS Artifact
B) Amazon SageMaker Model Card
C) IAM Credential Report
D) AWS Cost and Usage Report

<details><summary>View Answer</summary>

**Correct: A**. AWS Artifact is the portal for compliance reports (SOC2, ISO, etc.).
</details>

**Q20.** You want to run a specific ML workload on EC2. You require the lowest possible cost and your application is stateless and fault-tolerant (can handle random shutdowns).
A) On-Demand Instances
B) Reserved Instances
C) Spot Instances
D) Dedicated Hosts

<details><summary>View Answer</summary>

**Correct: C**. "Fault-Tolerant" + "Low Cost" = Spot.
</details>
