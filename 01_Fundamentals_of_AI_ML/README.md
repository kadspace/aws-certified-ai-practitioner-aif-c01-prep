# Domain 1: Fundamentals of AI and ML (20%)

## 1. Core Concepts & Terminology

### The AI Hierarchy
- **Artificial Intelligence (AI)**: Any technique that enables computers to mimic human intelligence. It is the broad umbrella term.
- **Machine Learning (ML)**: A subset of AI that uses algorithms to learn patterns from data and make predictions. It relies on data rather than explicit programming rules.
- **Deep Learning (DL)**: A subset of ML that uses multi-layered neural networks (like the human brain) to solve complex problems (e.g., image recognition, NLP).

### Types of Machine Learning
1.  **Supervised Learning**:
    -   **Data**: Labeled (Input + Correct Output is known).
    -   **Goal**: Train a model to predict the output for new, unseen inputs.
    -   **Examples**: Classification (Spam vs. Not Spam), Regression (Predicting House Prices).
2.  **Unsupervised Learning**:
    -   **Data**: Unlabeled (Only Input data).
    -   **Goal**: Find hidden structures or patterns in the data.
    -   **Examples**: Clustering (Customer Segmentation), Anomaly Detection (Fraud detection).
3.  **Reinforcement Learning (RL)**:
    -   **Mechanism**: Agent learns by interacting with an environment.
    -   **Feedback**: Rewards for good actions, Penalties for bad ones.
    -   **Examples**: Gaming bots, Robotics, Self-driving cars.

### Inferencing
-   **Inference**: The phase where a trained model makes predictions on new, live data.
-   **Batch Inference**: Processing a large group of data inputs at once (offline). Good for large datasets where immediate results aren't needed (e.g., nightly reports).
-   **Real-time Inference**: Processing strictly one input at a time with low latency demands (online). Good for instant responses (e.g., fraud block, chatbot reply).

## 2. Data in AI/ML

### Data Types
-   **Structured**: Highly organized, rows and columns (e.g., SQL databases, Excel).
-   **Unstructured**: No pre-defined format (e.g., Images, Video, Audio, PDF documents, Social media posts).
-   **Semi-structured**: Contains tags/markers but no strict schema (e.g., JSON, XML, Email logs).

### Data Handling
-   **Training Data**: The dataset used to initially teach the model.
-   **Validation Data**: Used effectively during training to tune hyperparameters and prevent overfitting.
-   **Test Data**: Used *after* training to evaluate the model's final performance (unseen data).

## 3. The ML Lifecycle (MLOps)
1.  **Business Problem Framing**: Define what you are trying to solve.
2.  **Data Preparation**: Collection, Cleaning, Labeling, Feature Engineering.
3.  **Model Training**: Selecting an algorithm and training the model.
4.  **Model Evaluation**: Testing accuracy, precision, recall.
5.  **Model Deployment**: Putting the model into production for inference.
6.  **Monitoring**: Watching for **Model Drift** (performance degrading over time) or **Data Drift** (input data changing significantly).

## 4. Key AWS Services for Domain 1
-   **Amazon SageMaker**: The central hub for building, training, and deploying ML models.
    -   *SageMaker Ground Truth*: For data labeling.
    -   *SageMaker Canvas*: No-code ML for business analysts.
    -   *SageMaker JumpStart*: Pre-built models and solutions.
-   **AWS AI Services** (High-level, no ML expertise needed):
    -   *Rekognition* (Image/Video)
    -   *Polly* (Text-to-Speech)
    -   *Transcribe* (Speech-to-Text)
    -   *Translate* (Language Translation)
    -   *Comprehend* (NLP/Text Analytics)
