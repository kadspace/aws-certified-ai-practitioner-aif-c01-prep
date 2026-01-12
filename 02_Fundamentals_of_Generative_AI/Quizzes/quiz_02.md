# Domain 2: Fundamentals of Generative AI - Quiz 2 (Advanced)

**Instructions:**
Focus on Token pricing, Bedrock features, and Model limits.

---

### Question 1
You are estimating the cost of a generative AI application using Amazon Bedrock (On-Demand). The application processes 1 million input tokens and generates 1 million output tokens per day.

Which factor significantly affects the cost difference between two models (e.g., Claude 3 Haiku vs. Claude 3 Opus)?

A) The number of concurrent users.
B) The complexity/size of the model intelligence.
C) The usage of a PrivateLink endpoint.
D) The region where the S3 bucket is located.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Bedrock pricing is per-token. "Smarter" models (larger parameter count like Opus) are significantly more expensive per token than "Faster/Smaller" models (like Haiku).
*   **A (Wrong)**: Concurrent users don't change the per-token price (unless you use Provisioned Throughput, but On-Demand measures tokens, not users).
</details>

---

### Question 2
A user reports that the chatbot cuts off mid-sentence. You suspect the `Max Tokens` parameter is too low.
If you increase `Max Tokens`, what creates a trade-off (downside)?

A) The model will hallucinate more.
B) The latency (time to complete the response) and cost will increase.
C) The model will become less deterministic.
D) The model will forget the system prompt.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Generating more tokens takes more time (Linear increase in latency) and costs more money.
*   **A/C (Wrong)**: Max tokens specifically controls length, not creativity or truthfulness.
</details>

---

### Question 3
Which AWS service feature helps you generate high-quality training datasets for fine-tuning a model by managing a workforce of human labelers?

A) Amazon SageMaker Ground Truth
B) Amazon Mechanical Turk
C) Amazon Augmented AI (A2I)
D) Amazon Bedrock Knowledge Bases

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** A

**Explanation:**
*   **A (Correct)**: SageMaker Ground Truth is the service *specifically* for managing labeling jobs (bounding boxes, text classification) to create training datasets.
*   **C (Wrong)**: A2I is for human review *during inference*, not for initial dataset creation.
</details>

---

### Question 4
You have a strict requirement that your GenAI application must support **multimodal** input (Images + Text) to generate a text description.

Which Amazon Bedrock model family supports this?

A) AI21 Labs Jurassic-2
B) Amazon Titan Text Lite
C) Anthropic Claude 3
D) Cohere Command

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: Claude 3 (and Titan Multimodal Embeddings) supports Vision (Image inputs).
*   **A/B/D (Wrong)**: Most older text models (Jurassic, Command, Titan Text Lite) are text-only input.
</details>

---

### Question 5
What is the function of "Stop Sequences" in inference parameters?

A) It prevents the model from generating profanity.
B) It tells the model to stop generating text when it encounters a specific character pattern (e.g., "User:").
C) It creates a timeout for the API call to save money.
D) It stops the model from accessing the internet.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Stop sequences effectively "cut" the model off. Essential for chatbots to prevent the model from hallucinating the *User's* next turn in the conversation.
</details>
