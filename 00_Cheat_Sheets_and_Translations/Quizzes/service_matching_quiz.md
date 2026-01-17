# AWS Service Matching Quiz

**Instructions:**
This quiz focuses on mapping business requirements to the correct AWS Service. No deep ML theory here—just "Which tool for which job?"

---

### Question 1
Your company has 50,000 PDF documents stored in SharePoint and S3. You want to build a search interface that allows employees to ask questions like "What is our policy on remote work?" and get a direct answer based on the documents.
You want a service that can **automatically crawl** these sources and provide **semantic search** results.

Which service is the best fit?
A) Amazon OpenSearch Serverless
B) Amazon Kendra
C) Amazon Textract
D) Amazon Comprehend

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: **Amazon Kendra** is an intelligent search service that includes built-in connectors for S3, SharePoint, Salesforce, etc. It uses ML to understand the context of questions and search documents semantically.
*   **A**: OpenSearch is a raw search engine. You would have to build the crawler and the embedding logic yourself. Kendra does it out-of-the-box.
</details>

---

### Question 2
You are building a customer service application. You need a service that can handle **multi-turn conversations**, understand user **intents** (like "I want to book a flight"), and extract **slots** (like "Destination" and "Date").

Which service should you use?
A) Amazon Polly
B) Amazon Transcribe
C) Amazon Lex
D) Amazon Bedrock Agents

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: **Amazon Lex** is the service for building conversational interfaces (chatbots). It uses the same technology as Alexa.
*   **D**: While Bedrock Agents *can* do this, Lex is the purpose-built service for standard intent/slot-based chatbots.
</details>

---

### Question 3
An e-commerce website wants to show a "Recommended for You" section on their homepage based on a user's past browsing history and purchase behavior.

Which service provides these **personalized recommendations**?
A) Amazon Personalize
B) Amazon Forecast
C) Amazon Rekognition
D) SageMaker Canvas

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** A

**Explanation:**
*   **A (Correct)**: **Amazon Personalize** is a managed service that uses ML to create high-quality recommendations.
*   **B**: Forecast is for time-series data (e.g., "How many shirts will we sell next month?").
</details>

---

### Question 4
A logistics company wants to predict how many delivery drivers they will need in New York City for the upcoming holiday season based on 5 years of historical delivery data.

Which service is designed for this **time-series forecasting**?
A) Amazon Personalize
B) Amazon Forecast
C) Amazon Kendra
D) Amazon Transcribe

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: **Amazon Forecast** is specifically for time-series forecasting (demand, inventory, etc.).
</details>

---

### Question 5
You have a collection of handwritten medical notes that have been scanned as images. You need to extract the text from these images into a machine-readable format.

Which service should you use?
A) Amazon Rekognition
B) Amazon Comprehend
C) Amazon Textract
D) Amazon Translate

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: **Amazon Textract** goes beyond simple OCR; it can extract text, handwriting, tables, and forms from documents.
*   **A**: Rekognition is for "What is in this picture?" (e.g., "A dog", "A face"). Textract is for "Read this document".
</details>

---

### Question 6
You want to analyze the **sentiment** (Positive, Negative, Neutral) of customer reviews posted on your website to identify unhappy customers automatically.

Which service is best for this **Natural Language Processing (NLP)** task?
A) Amazon Comprehend
B) Amazon Lex
C) Amazon Polly
D) Amazon Bedrock

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** A

**Explanation:**
*   **A (Correct)**: **Amazon Comprehend** is the NLP service for sentiment analysis, entity recognition, and keyphrase extraction.
</details>

---

### Question 7
You need to provide a "Read Aloud" feature for your blog posts to make them more accessible. You want the voice to sound natural and human-like.

Which service converts **Text to Speech**?
A) Amazon Transcribe
B) Amazon Polly
C) Amazon Translate
D) Amazon Lex

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: **Amazon Polly** turns text into lifelike speech.
*   **A**: Transcribe is the opposite (Speech to Text).
</details>

---

### Question 8
A security team wants to automatically detect and redact **Personally Identifiable Information (PII)** like Social Security Numbers and Credit Card numbers from a large set of text files.

Which service has built-in **PII detection** capabilities?
A) Amazon Macie
B) Amazon Comprehend
C) Both A and B
D) Amazon GuardDuty

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: Both **Macie** (for data in S3) and **Comprehend** (for general text analysis) can detect PII.
</details>
