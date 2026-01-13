# Exam Prep Progress Log

## Quick Summary
| Domain | Quiz | Score | Status |
| :--- | :--- | :--- | :--- |
| **Domain 1** | Quiz 01 | **5/5 (100%)** | ✅ Ready |
| **Domain 1** | Quiz 02 | **5/5 (100%)** | ✅ Ready |
| **Domain 2** | Quiz 01 | **5/5 (100%)** | ✅ Ready |
| **Domain 2** | Quiz 02 | **5/5 (100%)** | ✅ Ready |
| **Domain 3** | Quiz 01 | **4/5 (80%)** | ⚠️ Review |
| **Domain 4** | Quiz 01 | **4/5 (80%)** | ⚠️ Review |
| **Domain 5** | Quiz 01 | **4/5 (80%)** | ⚠️ Review |
| **Cheat Sheet**| Quiz 01 | **4/5 (80%)** | ⚠️ Review |
| **Mixed** | Mock 01 | **3/5 (60%)** | 🛑 Focus Area |

---

## Detailed Breakdown
<details>
<summary><strong>Domain 1: Fundamentals of AI and ML</strong> (5/5)</summary>

*   **Quiz 01 Score**: 5/5
*   **Quiz 02 Score (Advanced)**: 5/5
*   **Strengths**: Solid grasp of core definitions (AI vs ML vs DL), Inference types, and identifying basic services (SageMaker Canvas).
*   **Action Items**: None. Move to next domain.
</details>

<details>
<summary><strong>Domain 2: Fundamentals of Generative AI</strong> (5/5)</summary>

*   **Quiz 01 Score**: 5/5
*   **Quiz 02 Score (Advanced)**: 5/5
*   **Strengths**: Foundation Models, Tokens, Bedrock access, Inference parameters (Temperature).
*   **Notes**: User requested a "Service Name Cheat Sheet" to help memorize specific AWS product names.
</details>

<details>
<summary><strong>Domain 3: Applications of Foundation Models</strong> (4/5)</summary>

*   **Quiz 01 Score**: 4/5
*   **Missed Concept**: **Agents vs. RAG**
    *   *Confusion*: Used RAG (Knowledge) when the scenario required taking action (Booking a flight).
    *   *Fix*: Remember, **RAG = Reading**. **Agents = Doing** (Action Groups + Lambda).
*   **Quiz 02 Score (Advanced)**: 4/5
    *   **Missed Concept**: **Knowledge Base Syncing (Ingestion)**
    *   *Confusion*: Thought restarting the Agent updates the data.
    *   *Fix*: Agents are code; they don't hold data. The **Vector Database** holds data. You must run an **Ingestion Job** to sync S3 -> Vector DB.
</details>

<details>
<summary><strong>Domain 4: Guidelines for Responsible AI</strong> (4/5)</summary>

*   **Quiz 01 Score**: 4/5
*   **Missed Concept**: **SageMaker Clarify vs. Amazon Inspector**
    *   *Confusion*: Confused AI Bias detection with infrastructure scanning.
    *   *Fix*: **Clarify** = AI Bias/Fairness. **Inspector** = OS/Code Vulnerabilities (CVEs).
*   **Quiz 02 Score (Advanced)**: 5/5
    *   **Strengths**: Solid grasp of Responsible AI (SHAP, Guardrails, Drift).
    *   **Note**: User asked about SHAP relevance; yes, specifically "Feature Attribution" is a key exam topic.
</details>

<details>
<summary><strong>Domain 5: Security, Compliance, and Governance</strong> (4/5)</summary>

*   **Quiz 01 Score**: 4/5
*   **Missed Concept**: **SageMaker Role Manager**
    *   *Confusion*: Tried to use manual IAM users instead of managed templates.
*   **Quiz 02 Score (Advanced)**: 4/5
    *   **Missed Concept**: **Service Control Policies (SCPs) vs. Permission Boundaries**
    *   *Confusion*: Picked Permission Boundaries (Identity-level) instead of SCPs (Organization-level).
    *   *Fix*: **SCPs** = Global rules for the whole Account (Root). **Boundaries** = Rules for specific Users/Roles.
    *   **Note**: For Encryption, **Customer Managed Keys (CMK)** is the standard answer for "User wants control".
</details>

<details>
<summary><strong>Mixed Mock Exam</strong> (3/5)</summary>

*   **Mock Quiz 01 Score**: 3/5
*   **Missed Concept 1**: **AWS Config vs GuardDuty**
    *   *Fix*: **Config** checks *settings* (preventative/compliance). **GuardDuty** checks *threats* (active attacks).
*   **Missed Concept 2**: **Unsupervised vs Reinforcement Learning**
    *   *Fix*: **Unsupervised** = finding hidden patterns (Clustering) with no labels. **Reinforcement** = learning via rewards/punishment.
</details>

<details>
<summary><strong>Cheat Sheet & Metrics</strong> (4/5)</summary>

*   **Quiz 01 Score**: 4/5
*   **Missed Concept**: **Recall vs Precision (ROUGE vs BLEU)**
    *   *Confusion*: Mixed up Summarization metric (ROUGE) with Translation metric (BLEU).
    *   *Fix*: **ROUGE** = **R**ecall (Did I get all the key words? -> Summarization). **BLEU** = Precision (Is the phrase exact? -> Translation).
</details>
