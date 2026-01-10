# Domain 5: Security, Compliance, and Governance - Quiz 1 (Hard)

**Instructions:**
Focus on the specific *purpose* of each security service. Many look similar but handle different layers (Storage vs. Network vs. AI Model).

---

### Question 1
Your company has terabytes of unlabelled text data in Amazon S3 that you plan to use for custom model training. Before training begins, you must ensure that this *storage* bucket contains no Personally Identifiable Information (PII).

Which service should you use to scan the existing stored data?

A) Amazon Bedrock Guardrails
B) Amazon Macie
C) Amazon Inspector
D) Amazon GuardDuty

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Amazon Macie uses ML to discover and protect sensitive data (PII) specifically in **Amazon S3**.
*   **A (Wrong)**: Bedrock Guardrails filters data *during inference* (live chat), not data resting in storage.
*   **C (Wrong)**: Inspector scans EC2 instances/containers for software vulnerabilities (CVEs), not text data for PII.
*   **D (Wrong)**: GuardDuty detects *threats* (malicious IP addresses, anomalies), not PII.
</details>

---

### Question 2
You need to grant a team of data scientists access to Amazon SageMaker. You want to follow the principle of least privilege but avoid the operational overhead of manually writing complex JSON policies for every single specific SageMaker action.

Which feature provides pre-configured permission templates specifically for ML activities?

A) AWS IAM Access Analyzer
B) Amazon SageMaker Role Manager
C) AWS Identity and Access Management (IAM) Users
D) Amazon SageMaker Model Registry

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: SageMaker Role Manager provides persona-based templates (e.g., "Data Scientist", "MLOps Engineer") with pre-vetted permissions, saving you from writing raw IAM policies.
*   **C (Wrong)**: While you *can* use raw IAM, the question asks for a way to "avoid operational overhead" of manual policies. Role Manager is the specific tool for this.
</details>

---

### Question 3
An auditor asks for proof of exactly *who* invoked a specific Amazon Bedrock model at 2:00 PM yesterday.

Which service provides this specific audit log?

A) Amazon CloudWatch Logs
B) AWS CloudTrail
C) AWS Config
D) AWS Artifact

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: CloudTrail logs API activity ("Who did what"). It records the `InvokeModel` API call, the user identity, and the timestamp.
*   **A (Wrong)**: CloudWatch Logs stores *application* logs (error messages, print statements), not the API audit trail of the AWS control plane.
*   **C (Wrong)**: AWS Config tracks *resource configuration changes* (e.g., "Did the security group change?"), not API invocation history.
</details>

---

### Question 4
Under the AWS Shared Responsibility Model for AI, which of the following is the **customer's** responsibility?

A) Physical security of the data centers hosting Amazon Bedrock.
B) Patching the underlying OS of the serverless Bedrock compute fleet.
C) Ensuring the training data used for fine-tuning does not violate copyright laws.
D) Securing the network infrastructure that connects AWS Regions.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** C

**Explanation:**
*   **C (Correct)**: Customers are responsible for "Security IN the cloud," which includes their data, content, and legal compliance of that data.
*   **A/B/D (Wrong)**: These are "Security OF the cloud" (Hardware, Global Infrastructure, Managed Services), which solely AWS handles.
</details>

---

### Question 5
You want to centrally track the inventory of all your ML models, their version history, and their approval status (e.g., "Approved for Production", "Rejected") across your entire organization to ensure governance.

Which service is purpose-built for this?

A) Amazon SageMaker Model Registry
B) AWS Service Catalog
C) Amazon S3
D) AWS Systems Manager

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** A

**Explanation:**
*   **A (Correct)**: Model Registry is the governance repository for tracking model versions, metadata, and approval workflows.
*   **B (Wrong)**: Service Catalog is for managing approved *IT services/stacks* (CloudFormation templates), not specifically ML model versions.
</details>
