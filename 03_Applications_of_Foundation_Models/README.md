# Domain 3: Applications of Foundation Models (28%)

## 1. Design Considerations
-   **Model Selection Criteria**:
    -   **Modality**: Text, Image, Multimodal?
    -   **Size/Latency**: Bigger models = smarter but slower & more expensive. Small models = faster & cheaper.
    -   **Cost**: pricing models (On-demand tokens vs. Provisioned Throughput).
    -   **Capabilities**: Does it support specific languages or coding tasks?
-   **Inference Parameters**:
    -   *Max Tokens*: Limits response length.
    -   *Top-P / Top-K*: Controls diversity of word choices.

## 2. Advanced Prompt Engineering
-   **Chain-of-Thought (CoT)**: Asking the model to "think step-by-step" to solve complex logic/math problems.
-   **Prompt Templates**: Reusable structures where user input is injected (e.g., "Summarize the following text: {{TEXT}}").
-   **Negative Prompting**: Telling the model what *not* to generate (e.g., "Do not include any PII").

## 3. Retrieval Augmented Generation (RAG)
-   **Problem**: basic LLMs have a "knowledge cutoff" and can't see your private data.
-   **Solution (RAG)**:
    1.  **Retrieve**: Search a **Knowledge Base** (Vector DB) for relevant internal docs.
    2.  **Augment**: Add those docs to the prompt as context.
    3.  **Generate**: Send augmented prompt to LLM.
-   **Amazon Bedrock Knowledge Bases**: Fully managed RAG service.
-   **Vector Stores**:
    -   *Amazon OpenSearch Serverless*: High-scale search.
    -   *Amazon Aurora (pgvector)*: Relational + Vector.
    -   *Amazon Neptune Analytics*: Graph + Vector.

## 4. Agents & Orchestration
-   **Agents for Amazon Bedrock**:
    -   Break down complex tasks into sub-steps.
    -   Call external **APIs** (via Lambda) to perform actions (e.g., "Book a flight").
    -   Can access Knowledge Bases.

## 5. Model Customization
-   **Fine-tuning**: training a model on *specific* labeled dataset to change its behavior or specialized knowledge.
-   **Continued Pre-training**: Feeding a model massive amounts of unlabeled text (e.g., medical journals) to teach it a new domain *language*.

## 6. Model Evaluation
-   **Metrics**:
    -   *ROUGE*: For summarization (overlap with reference summary).
    -   *BLEU*: For translation quality.
    -   *BERTScore*: Semantic similarity.
-   **Bedrock Model Evaluation**:
    -   *Automated*: Compare model A vs B on standard benchmarks.
    -   *Human*: Real humans rate responses (thumbs up/down).
