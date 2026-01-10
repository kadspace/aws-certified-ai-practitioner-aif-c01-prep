# Domain 4: Guidelines for Responsible AI (14%)

## 1. Core Principles of Responsible AI
-   **Fairness**: AI systems should treat all people fairly and avoid bias against protected groups/attributes (Race, Gender, Age).
-   **Explainability**: The ability to understand *why* a model made a specific prediction.
-   **Privacy & Security**: Protecting user data and ensuring models don't leak sensitive info.
-   **Robustness**: The model stays accurate even when input data is slightly different or malicious (adversarial attacks).
-   **Veracity**: The truthfulness of the output. Preventing hallucinations.
-   **Transparency**: Being open about the limitations and intended use of the AI system (e.g., "This is an AI chatbot, not a human").

## 2. Key AWS Services for Responsibility
-   **Amazon Bedrock Guardrails**:
    -   *Content Filters*: Block Hate, Abuse, Sexual, Violence at different thresholds (Low/Medium/High).
    -   *Denied Topics*: Custom list of topics the bot refuses to discuss (e.g., "Don't give financial advice").
    -   *Word Filters*: Block specific profanity or competitor names.
    -   *Sensitive Information Filters (PII)*: Redact or block Name, Email, SSN, Credit Card info.
    -   *Contextual Grounding Check*: Detects if the response is supported by the source or if it's a hallucination.
-   **Amazon SageMaker Clarify**:
    -   Detects **Bias** in your training data (Pre-training bias) and your model's predictions (Post-training bias).
    -   Provides **Explainability** (SHAP values) to show which features contributed most to a prediction.
-   **AWS AI Service Cards**:
    -   Public transparency documentation for AWS AI services (like nutrition labels).
    -   Explains capabilities, limitations, and intended use cases.
-   **Human-in-the-Loop (Augmented AI / A2I)**:
    -   Sending low-confidence predictions to a human for manual review.

## 3. Governance
-   **Governance**: The framework of people, processes, and tools to manage AI risks.
-   **Legal & IP**: Understanding who owns the generated content and ensuring you don't infringe on copyrights.
