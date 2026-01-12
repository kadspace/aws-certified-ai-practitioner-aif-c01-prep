# Mixed Practice Exam - Quiz 2 (Advanced)

**Instructions:**
This is the "Boss Fight". Complex scenarios mixing multiple domains.

---

### Question 1 (Domain 3)
You are building an agent for an insurance company. The agent needs to verify a policy number (Read-only) and then Submit a Claim (Write action).
You want to design the schema optimally.

Which approach follows best practices?

A) Create two separate Agents: one for reading, one for writing.
B) Create one Agent with two separate Action Groups: one "Consult" (Read-only API), one "Transactional" (Write API).
C) Use RAG for the Claim Submission.
D) Put all logic in the System Prompt.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Agents can handle multiple Action Groups. It is best practice to group functions logically (e.g., Read vs Write) but keep them in the same Agent so it can handle the full conversation context.
</details>

---

### Question 2 (Domain 1)
You are training a model on Amazon SageMaker. You want to save money by using "Spot Instances".
What is the risk, and how does SageMaker mitigate it?

A) Risk: Low accuracy. Mitigation: Auto-tuning.
B) Risk: Instance interruption. Mitigation: SageMaker Checkpointing.
C) Risk: Slow network. Mitigation: PrivateLink.
D) Risk: Data loss. Mitigation: RAID 0.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Spot instances can be reclaimed by AWS with 2 minutes notice. "Checkpointing" saves the model state to S3 periodically so training can resume from the last checkpoint instead of restarting from zero.
</details>

---

### Question 3 (Domain 4)
You are using a Large Language Model to summarize financial news. You notice the model occasionally makes up fake company names.
You want to implement a **Contextual Grounding Check** using Amazon Bedrock Guardrails.

What score threshold should you adjust to filter this out?

A) Toxicity Score
B) Grounding Score (0.0 to 1.0)
C) PII Confidence Score
D) Temperature

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: The Grounding check returns a confidence score (e.g., 0.85). Low scores mean "This sentence is NOT supported by the source text." You filter out responses below your threshold.
</details>

---

### Question 4 (Domain 5)
A data scientist needs to upload a model to the **SageMaker Model Registry**. They are currently blocked by a permission error.
Following the principle of Least Privilege, which specific IAM Action do they need?

A) `sagemaker:CreateDomain`
B) `sagemaker:CreateModelPackage`
C) `iam:PassRole`
D) `s3:ListBucket`

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: In SageMaker API terms, a versioned model in the registry is essentially a "Model Package". The permission is `CreateModelPackage`.
*   **A**: Creates a Studio IDE environment.
*   **C**: Needed to pass IAM roles to services, but not the specific action for the registry upload itself.
</details>

---

### Question 5 (Domain 2)
You want to fine-tune a Llama 3 model on Amazon Bedrock.
Where does the training actually happen?

A) On your local laptop.
B) In a public EC2 instance managed by you.
C) In a private, isolated copy of the model managed by AWS (Serverless).
D) On the Anthropic public servers.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: Bedrock Fine-Tuning creates a private copy of the model. It runs on AWS managed infrastructure, completely isolated from the public base model and other customers. Meaning: Your data is safe.
</details>
