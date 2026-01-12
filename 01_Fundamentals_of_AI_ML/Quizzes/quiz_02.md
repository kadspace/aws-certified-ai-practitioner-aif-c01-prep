# Domain 1: Fundamentals of AI and ML - Quiz 2 (Advanced)

**Instructions:**
These questions focus on "Best Fit" service selection and specific ML lifecycle nuances.

---

### Question 1
A retail company wants to build a recommendation engine. They have a team of data scientists who want full control over the model training and deployment process, including choosing specific instance types for training jobs to optimize costs. However, they do not want to manage the underlying EC2 clusters or OS patching.

Which service is the **most appropriate** choice?

A) Amazon SageMaker (Training & Inference)
B) Amazon Personalize
C) Amazon Bedrock
D) AWS DeepLearning AMIs on EC2

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** A

**Explanation:**
*   **A (Correct)**: SageMaker gives full control over the ML process (custom code, instance selection) but abstracts the infrastructure management (Patching, Cluster health).
*   **B (Wrong)**: Personalize is high-level/auto-generated. It DOES NOT give "full control" over training instances or custom model code.
*   **D (Wrong)**: EC2 requires managing OS patching, which the requirement explicitly excludes.
</details>

---

### Question 2
You are preprocessing a dataset that contains many images of varying sizes. You need to standardize them to 224x224 pixels before training a computer vision model. You want a managed solution that integrates directly into your SageMaker training pipeline.

Which tool should you use?

A) AWS Glue
B) Amazon SageMaker Processing Jobs
C) Amazon Kinesis Data Firehose
D) Amazon Athena

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: SageMaker Processing is designed specifically for running data processing scripts (scikit-learn, etc.) as part of an ML pipeline.
*   **A (Wrong)**: Glue is for ETL on tabular/structured data, not ideal for resizing images.
</details>

---

### Question 3
An organization wants to use AI to analyze customer sentiment from call logs. The "call logs" are currently stored as .mp3 audio files in S3.

Which combination of services achieves this with the **least development effort**?

A) Transcribe the audio using Amazon Transcribe, then analyze the text using Amazon Comprehend.
B) Use Amazon SageMaker to train a custom speech-to-sentiment model.
C) Use Amazon Polly to convert the audio to text, then use Amazon Bedrock.
D) Use Amazon Rekognition to analyze the audio waveform.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** A

**Explanation:**
*   **A (Correct)**: "Least development effort" points to AI Services (High-level APIs). Transcribe (Speech->Text) + Comprehend (Text->Sentiment) is the standard pattern.
*   **C (Wrong)**: Polly is Text-to-Speech (Talking), not Speech-to-Text (Listening).
</details>

---

### Question 4
What is the primary difference between **Regression** and **Classification** in Supervised Learning?

A) Regression predicts a continuous number (e.g., Price); Classification predicts a category (e.g., Yes/No).
B) Regression is Unsupervised; Classification is Supervised.
C) Classification is for text; Regression is for images.
D) Regression requires more training data than Classification.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** A

**Explanation:**
*   **A (Correct)**: The definition.
    *   Regression: "How much?" (Temperature, Stock Price).
    *   Classification: "Which one?" (Cat/Dog, Spam/Ham).
</details>

---

### Question 5
You are evaluating a model's performance. You observe that the model performs extremely well on the training data (99% accuracy) but performs poorly on the validation data (70% accuracy).

What is this phenomenon called?

A) Underfitting
B) Overfitting
C) Data Leakage
D) Model Drift

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Overfitting = Memorizing the training data but failing to generalize to new data.
*   **A (Wrong)**: Underfitting = Doing poorly on *both* training and validation.
</details>
