# Domain 3: Applications of Foundation Models - Quiz 1 (Harder)

**Instructions:**
These questions are **scenario-based**, mirroring the actual exam's "distractor" style. Read carefully.

---

### Question 1
A startup is building a customer support chatbot using Amazon Bedrock. The chatbot needs to answer questions based *strictly* on the company's internal PDF manuals, which change weekly. The startup wants to minimize the operational overhead of retraining models.

Which approach is the most efficient and cost-effective?

A) Fine-tune a Titan Text model every week using the new PDF documents as the training dataset.
B) Use a base Titan Text model and implement Retrieval Augmented Generation (RAG) using Amazon Bedrock Knowledge Bases to index the PDFs.
C) Use Prompt Engineering to paste the text of all 500 PDF manuals into the context window for every single query.
D) Train a new custom model from scratch using SageMaker Training jobs.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **A (Wrong)**: Fine-tuning is expensive, slow, and overkill for just adding knowledge. It's better for changing *behavior/style*.
*   **B (Correct)**: RAG is the standard pattern for "chat with your data". It handles dynamic data (weekly changes) by just updating the index, with zero model training.
*   **C (Wrong)**: pasting 500 Manuals will exceed the context window (token limit) and cost a fortune per call.
*   **D (Wrong)**: Training from scratch is astronomical in cost and unnecessary.
</details>

---

### Question 2
You are designing a generative AI feature that summarizes legal contracts. Accuracy is paramount; the model must not invention facts ("hallucinate"). You need a metric to strictly measure how much the model's summary overlaps with a "gold standard" reference summary provided by your lawyers.

Which metric should you choose?

A) ROUGE-N
B) Accuracy
C) Latency
D) RMSE (Root Mean Square Error)

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** A

**Explanation:**
*   **A (Correct)**: ROUGE (Recall-Oriented Understudy for Gisting Evaluation) specifically measures n-gram overlap between the generated text and a reference text. It's the standard for summarization.
*   **B (Wrong)**: "Accuracy" in classification means "Right/Wrong". In text generation, it's ambiguous.
*   **C (Wrong)**: Latency measures speed, not quality.
*   **D (Wrong)**: RMSE is for numerical regression, not text.
</details>

---

### Question 3
A developer is using Amazon Bedrock to build an app. They want to ensure that the model output is deterministic (returns the exact same code snippet for the same input) for a unit testing use case.

Which inference parameter configuration is appropriate?

A) Temperature = 1.0, Top-P = 0.99
B) Temperature = 0, Top-P = 1.0
C) Temperature = 0.5, Top-K = 500
D) Max Generation Length = 4096

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Temperature of 0 eliminates randomness in the next-token selection strategy (Greedy decoding), making the output deterministic.
*   **A/C (Wrong)**: Higher temperature/Top-P introduces randomness.
</details>

---

### Question 4
You are building an agent using Amazon Bedrock that needs to book flights on behalf of users. The agent needs to interact with an external REST API (`POST /book-flight`).

How do you expose this functionality to the Bedrock Agent?

A) Write the API endpoint into the System Prompt of the model.
B) Define an Action Group with an OpenAPI schema and link it to an AWS Lambda function.
C) Use RAG to ingest the API documentation.
D) Fine-tune the model on curl commands.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Bedrock Agents use "Action Groups" defined by OpenAPI schemas (Swagger) to know how to call Lambda functions that execute real-world tasks.
*   **A (Wrong)**: Prompts can't execute code directly.
*   **C (Wrong)**: RAG gives knowledge, it doesn't execute actions.
</details>

---

### Question 5
Your organization requires that all customer data sent to Amazon Bedrock for inference must *never* traverse the public internet, even though the traffic is encrypted.

Which networking solution satisfies this requirement?

A) Use HTTPS (TLS 1.2) for all API calls.
B) Use an Internet Gateway (IGW) attached to the VPC.
C) Configure AWS PrivateLink (VPC Endpoints) for Amazon Bedrock.
D) Use a NAT Gateway in a public subnet.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: PrivateLink enables private connectivity between your VPC and AWS services (like Bedrock) using private IP addresses. Traffic stays on the AWS backbone.
*   **A (Wrong)**: HTTPS is encrypted, but normally goes over the public internet to reach the public API endpoint.
*   **B/D (Wrong)**: Gateways facilitate internet access, which the requirement specifically forbids.
</details>
