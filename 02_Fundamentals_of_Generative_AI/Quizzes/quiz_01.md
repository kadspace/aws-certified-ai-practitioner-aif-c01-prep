# Domain 2: Fundamentals of Generative AI - Quiz 1

**Instructions:**
Read the question and options. Try to answer before expanding the "Answer" section.

---

### Question 1
Which of the following best describes the core function of a "Foundation Model" (FM)?

A) A model designed specifically and only for image classification.
B) A large-scale model pre-trained on vast amounts of unstructured data that can be adapted for many downstream tasks.
C) A specialized database used to store customer transaction logs.
D) A model that requires training from scratch for every single new application.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
Foundation Models are "foundational" because they are trained on massive datasets and can be adapted (fine-tuned) for many different specific tasks (chat, summary, extraction) without starting from zero.
</details>

---

### Question 2
You need to explain "Tokens" to a non-technical stakeholder. Which explanation is most accurate regarding AWS pricing and limits?

A) A token is exactly one word.
B) A token is a basic unit of text (word, part of a word, or character) processed by the model. 1000 tokens is roughly 750 words.
C) A token represents one API call, regardless of the text length.
D) Tokens are used for authentication only, not for measuring text.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
This is the standard definition. Tokens are the atomic units of input/output. The 1000 tokens ≈ 750 words is a common AWS rule of thumb.
</details>

---

### Question 3
What is "In-Context Learning" in the context of Generative AI?

A) Retraining the model with new data every night.
B) Providing examples or instructions within the prompt itself to guide the model's behavior without updating model weights.
C) Connecting the model to a SQL database.
D) The process of installing the model on a local laptop.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
In-Context Learning (like Zero-shot or Few-shot prompting) involves giving the model context *inside the prompt window* to change how it answers, without actually changing the model's underlying training (weights).
</details>

---

### Question 4
Which AWS service allows you to access models like Claude 3, Amazon Titan, and Meta Llama 3 via a single API without managing servers?

A) Amazon SageMaker JumpStart
B) Amazon Bedrock
C) AWS Lambda
D) Amazon Q Developer

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
Amazon Bedrock is the serverless, API-based service for accessing a variety of Foundation Models from top providers.
</details>

---

### Question 5
You are using a text generation model and want the output to be highly creative and varied. How should you adjust the inference parameters?

A) Set Temperature to 0.
B) Set Temperature to a high value (e.g., 0.9 or 1.0).
C) Decrease the Max Tokens limit.
D) Enable "Stop Sequences".

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
Temperature controls randomness. High temperature (near 1) makes the output more random/creative. Low temperature (near 0) makes it more deterministic/focused.
</details>
