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
| **Translate Languages** | **Amazon Translate** | Localization. |
| **No-Code ML Predictions** | **SageMaker Canvas** | Business analysts, drag-and-drop, CSV input. |
