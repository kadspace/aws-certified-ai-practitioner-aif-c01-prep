# Domain 5: Security, Compliance, and Governance - Quiz 2 (Advanced)

**Instructions:**
Focus on Network Security (VPC), Encryption nuances, and specific IAM/Governance roles.

---

### Question 1
A financial company requires that *no* traffic to Amazon Bedrock ever traverses the public internet. They also require that the Bedrock endpoint can *only* be accessed from a specific VPC, and valid API calls from other VPCs (even if authenticated) must be denied.

Which combination of controls achieves this?

A) Use a NAT Gateway and an IAM Policy with `aws:SourceIp`.
B) Use an **Interface VPC Endpoint (PrivateLink)** and attach a **VPC Endpoint Policy** that allows access only from the specific VPC ID.
C) Use AWS WAF to block foreign IP addresses.
D) Use a Service Control Policy (SCP) to deny Bedrock.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: PrivateLink keeps traffic private (off public internet). A **VPC Endpoint Policy** is a resource-based policy attached to the endpoint itself that controls *who* can use that private pipe.
*   **A (Wrong)**: NAT Gateway goes to the public internet.
</details>

---

### Question 2
You are using Amazon Bedrock with a Provisioned Throughput model. You need to ensure that the data stored in the model (for fine-tuning) is encrypted with a key that *you* control and can revoke immediately if a breach occurs.

What should you use?

A) AWS Owned Key (SSE-S3)
B) Customer Managed Key (CMK) in AWS KMS
C) Client-Side Encryption
D) TLS 1.3

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: "Customer Managed Key" gives you full control (Rotation, Revocation). "AWS Owned Key" is managed by AWS (you can't revoke it).
</details>

---

### Question 3
An auditor requires a report showing exactly which AI models are currently deployed in production, their approval status, and their lineage (where they came from).

Which service dashboard provides this view directly?

A) Amazon CloudWatch Dashboard
B) Amazon SageMaker Model Dashboard
C) AWS Security Hub
D) AWS Personal Health Dashboard

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: SageMaker Model Dashboard is a centralized view within the SageMaker console specifically for tracking model cards, lineage, and endpoint status.
</details>

---

### Question 4
You want to implement a "Guardrail" that prevents your developers from spinning up expensive GPU instances (e.g., `p4d.24xlarge`) in development accounts. This must be enforced at the **Account Level**, overriding any local administrator permissions.

Which tool is designed for this?

A) AWS IAM Permission Boundaries
B) Service Control Policies (SCPs) in AWS Organizations
C) Amazon SageMaker Role Manager
D) AWS Cost Explorer

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: SCPs are the "Root/Org" level guardrails. If an SCP denies `p4d` instances, even the Account Administrator cannot launch them.
*   **C (Wrong)**: Role Manager generates policies, but doesn't enforcement them at the Account level globally.
</details>

---

### Question 5
What is the primary security risk associated with **Prompt Injection**?

A) The model consumes too many tokens and costs money.
B) The attacker overrides the system instructions to force the model to perform unauthorized actions or reveal sensitive training data.
C) The model output becomes biased.
D) The encryption key is exposed.

<details>
<summary><strong>View Answer</strong></summary>

**Correct Answer:** B

**Explanation:**
*   **B (Correct)**: Prompt Injection is "Hacking the Model Brain" by telling it to ignore safety rules. The primary risk is unauthorized access/action (like an SQL injection).
</details>
