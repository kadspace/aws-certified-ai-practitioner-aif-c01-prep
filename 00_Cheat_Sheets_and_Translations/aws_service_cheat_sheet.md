# AWS AI Service Name Cheat Sheet

A rapid mapping of **Generic AI Concept** -> **Specific AWS Service Name**.

## 1. The Core Platforms
| If you want to... | The Service is... | Key Keywords |
| :--- | :--- | :--- |
| **Use Pre-trained Models** (via API) | **Amazon Bedrock** | Serverless, FMs, Claude, Titan, Knowledge Bases, Agents. |
| **Build/Train Custom Models** | **Amazon SageMaker** | JupyterLab, Training Jobs, Inference Endpoints, MLOps. |

## 2. Data & Labeling
| If you want to... | The Service is... | Key Keywords |
| :--- | :--- | :--- |
| **Label Data with Humans** | **SageMaker Ground Truth** | Bounding boxes, text classification, human workforce. |
| **Review Low-Confidence Predictions** | **Amazon A2I (Augmented AI)** | Human loop *during inference*, "Human Review Workflows". |
| **Store Vector Embeddings** | **OpenSearch Serverless** (Vector Engine) | RAG, Similarity Search, k-NN. |

## 3. Responsible AI & Governance
| If you want to... | The Service is... | Key Keywords |
| :--- | :--- | :--- |
| **Block Harmful Content** | **Bedrock Guardrails** | Denied topics, content filters, PII redaction (Real-time). |
| **Detect Bias / Explainability** | **SageMaker Clarify** | Class imbalance, SHAP values, Fairness metrics. |
| **Scan S3 for Sensitive Data** | **Amazon Macie** | PII discovery in *storage*, data privacy. |
| **Scan Infrastructure/EC2** | **Amazon Inspector** | Vulnerabilities (CVEs), Network reachability. |
| **Track Model Versions** | **SageMaker Model Registry** | Approval status (Approved/Rejected), versioning. |
| **Create IAM Policies Easily** | **SageMaker Role Manager** | Personas, pre-configured permissions. |
| **Transparent Documentation** | **AI Service Cards** | "Nutrition label", intended use, limitations. |

## 4. High-Level AI Services (No ML Skills Needed)
| If you want to... | The Service is... | Key Keywords |
| :--- | :--- | :--- |
| **Speech -> Text** | **Amazon Transcribe** | Subtitles, clinical documentation (Health). |
| **Text -> Speech** | **Amazon Polly** | "Talking", voices, pronunciation. |
| **Analyze Text** | **Amazon Comprehend** | Sentiment, entity recognition, PII detection in text. |
| **Analyze Images/Video** | **Amazon Rekognition** | Face detection, content moderation, celebrity recognition. |
| **Extract Text from Docs** | **Amazon Textract** | OCR, PDFs, Forms, Tables, Handwriting. |
| **Translate Languages** | **Amazon Translate** | Localization. |
| **Intelligent Search** | **Amazon Kendra** | Enterprise search, document crawler (S3/SharePoint), Semantic search for RAG. |
| **Build Chatbots** | **Amazon Lex** | Conversational AI, Intent, Utterance, Slot, Alexa-style. |
| **Personalized Recs** | **Amazon Personalize** | "Customers who bought this also bought...", recommendation engine. |
| **Predictive Analytics** | **Amazon Forecast** | Time-series, inventory planning, demand forecasting. |
| **No-Code ML Predictions** | **SageMaker Canvas** | Business analysts, drag-and-drop, CSV input. |

## 5. Key Metrics (The "Scorecard")
| Metric | Use Case | What it measures |
| :--- | :--- | :--- |
| **ROUGE** | **Summarization** | Reviewing text overlap. "Did the model find the *Recall* words?" (Used for text). |
| **BLEU** | **Translation** | "Did the model get the *Exact Precision* of the phrase?" (Used for French->English). |
| **F1 Score** | **Classification** | The harmonic balance between Precision and Recall. "Did it catch the bad guys (Recall) without flagging innocents (Precision)?" |
| **Accuracy** | **Simple Classification** | Simply "Right / Total". Bad for imbalance (e.g., 99% of transactions are legit, so a model saying "All Legit" is 99% accurate but useless). |
| **Perplexity** | **LLM Fluency** | How "surprised" the model is by language. Lower is better. |
| **RMSE** | **Regression** | Root Mean Square Error. How far off the numeric prediction was (e.g., predicted $100, actual $105). |
