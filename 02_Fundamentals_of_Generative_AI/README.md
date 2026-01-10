# Domain 2: Fundamentals of Generative AI (24%)

## 1. What is Generative AI?
-   **Definition**: A subset of Deep Learning powered by **Foundation Models (FMs)** that can generate *new* content (text, images, audio, code) based on patterns learned from massive datasets.
-   **Discriminative vs. Generative**:
    -   *Discriminative AI*: Classifies existing data (e.g., "Is this a cat?").
    -   *Generative AI*: Creates new data (e.g., "Draw a cat").

## 2. Core Concepts
-   **Foundation Models (FMs)**: Large models pre-trained on vast amounts of unstructured data. They are "adapted" for downstream tasks rather than built from scratch.
-   **Tokens**: The basic unit of text for an LLM (word, part of a word, or character).
    -   *Rule of Thumb*: 1,000 tokens ≈ 750 words.
    -   **Context Window**: The maximum number of tokens a model can process in a single interaction (input + output).
-   **Embeddings**: Converting text/images into numerical vectors (lists of numbers) that represent semantic meaning.
    -   *Vector Database*: Specialized DBs to store and search these embeddings (used for RAG).
-   **Transformers**: The architecture behind modern GenAI.
    -   *Attention Mechanism*: Allows the model to focus on different parts of the input sentence to understand context.

## 3. Generative Model Types
-   **Large Language Models (LLMs)**: Text-to-Text (e.g., GPT, Claude, Titan Text).
-   **Diffusion Models**: Text-to-Image. They work by adding noise to an image until it disrupts it, then learning to reverse the process to "denoise" pure noise into a clear image (e.g., Stable Diffusion, Titan Image Generator).
-   **Multi-modal Models**: Can accept/generate multiple data types (e.g., Image input -> Text description).

## 4. Prompt Engineering Basics
-   **Prompt**: The input given to the model.
-   **In-Context Learning**: Teaching the model without re-training it.
    -   *Zero-shot*: No examples provided. "Translate this."
    -   *Few-shot*: Providing a few examples in the prompt to guide the style/format.
-   **Hallucination**: When an LLM generates a response that looks confident but is factually incorrect.
-   **Temperature**: A parameter controlling randomness.
    -   *Low Temperature (0.0)*: Deterministic, factual, repetitive.
    -   *High Temperature (1.0)*: Creative, random, diverse.

## 5. Key AWS Services for Domain 2
-   **Amazon Bedrock**: The serverless, fully managed service to access FMs via API.
    -   *Model Choice*: Amazon Titan, Anthropic Claude, AI21 Jurassic, Cohere Command, Meta Llama, Mistral.
    -   *Serverless*: No servers to manage. Pay-per-token.
-   **Amazon Q Developer (formerly CodeWhisperer)**: AI coding companion. Generates code snippets, security scans.
-   **Amazon Q Business**: GenAI assistant for enterprise data (RAG-based).
