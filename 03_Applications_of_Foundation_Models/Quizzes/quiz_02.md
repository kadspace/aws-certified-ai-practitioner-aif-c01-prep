# Domain 3: Applications of Foundation Models - Quiz 2 (Advanced)

**Instructions:**
Focus on RAG optimization, Agent internals, and complex inference options.

---

### Question 1
You are implementing RAG with Amazon Bedrock. Your users are complaining that the answers are accurate but retrieved from outdated documents. You have already uploaded the new documents to the S3 bucket connected to your Knowledge Base.

What is the necessary step to make the new documents searchable?

A) Restart the Bedrock Agent.
B) Call the `StartIngestionJob` API to sync the Knowledge Base with the data source.
C) Increase the `Top-K` retrieval parameter.
D) Re-train the embedding model.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Knowledge Bases stay in sync only when you actively trigger a sync/ingestion job. Uploading to S3 is not enough; the embeddings must be generated and indexed.
*   **D (Wrong)**: Embedding models are pre-trained. You index data, you don't retrain the model.
</details>

---

### Question 2
You are designing a chatbot that needs to maintain context over a long conversation (20+ turns). You notice that as the conversation grows, the cost per invocation is rising linearly, and the latency is increasing.

What is the root cause?

A) The `Temperature` is increasing automatically.
B) You are re-sending the entire conversation history (all previous turns) as input prompt context for every new message.
C) The model is learning from the user and getting larger.
D) AWS charges more for longer sessions.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: LLMs are stateless. To have "memory," the developer must paste the previous chat history into the prompt every time. This increases token count (Cost + Latency) linearly.
*   **C (Wrong)**: Base models are frozen. They don't learn or grow live.
</details>

---

### Question 3
You want to maximize the performance of a RAG system. You decide to use "Hybrid Search".

What two search methods does Hybrid Search combine?

A) Keyword Search (BM25) + Semantic Search (Vector Embeddings)
B) SQL Search + NoSQL Search
C) Image Search + Text Search
D) English Search + Spanish Search

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** A

**Explanation:**
*   **A (Correct)**: Hybrid search merges the precision of exact keyword matching (good for product IDs/names) with the understanding of semantic search (good for concepts).
</details>

---

### Question 4
You require a model that can take a user's rough sketch (image) and a text description, and generate a polished website HTML code.

Which model capability is strictly required?

A) Text-to-Image
B) Image-to-Text
C) Multimodal Input (Image + Text -> Text)
D) Embodied AI

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: The input is Image + Text. The output is Text (Code). This is Multimodal Input.
*   **B (Wrong)**: Image-to-text usually implies captioning ("A dog on a beach"), not complex reasoning/coding from a sketch.
</details>

---

### Question 5
Which prompting technique involves asking the model to "Think step-by-step" to improve accuracy on complex reasoning tasks?

A) Zero-Shot Prompting
B) Chain-of-Thought (CoT) Prompting
C) Retrieval Augmented Generation
D) ReAct Prompting

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: CoT encourages the model to generate intermediate reasoning steps, which significantly boosts performance on math/logic.
</details>
