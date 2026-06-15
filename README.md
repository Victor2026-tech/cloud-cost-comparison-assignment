# cloud-cost-comparison-assignment
# Cloud Pricing Comparison: AWS vs Azure

## 1. Project Overview

This project compares the cost of deploying a small-scale web application across AWS and Microsoft Azure. The comparison evaluates compute, storage, database, and network costs using official cloud pricing calculators.

The goal is to understand how architectural decisions and provider pricing models affect overall cloud expenditure.

---

## 2. System Architecture Assumptions

The application is assumed to be a basic web system with:

* 2 vCPU, 4 GB RAM virtual machine
* 100 GB object/file storage
* 20 GB relational database
* 500 GB monthly outbound data transfer
* 24/7 availability

---

## 3. Service Equivalency Mapping

| Function   | AWS Service        | Azure Service      |
| ---------- | ------------------ | ------------------ |
| Compute    | EC2 (t3.medium)    | Azure VM (B2s)     |
| Storage    | Amazon S3          | Azure Blob Storage |
| Database   | Amazon RDS (MySQL) | Azure SQL Database |
| Networking | Data Transfer      | Bandwidth (Egress) |

---

## 4. Monthly Cost Comparison

| Service   | AWS ($)   | Azure ($) | Cheaper Provider | Difference |
| --------- | --------- | --------- | ---------------- | ---------- |
| Compute   | 30.00     | 32.00     | AWS              | 6.25%      |
| Storage   | 2.30      | 2.00      | Azure            | 15%        |
| Database  | 18.00     | 20.00     | AWS              | 10%        |
| Network   | 36.00     | 42.00     | AWS              | 14.29%     |
| **TOTAL** | **86.30** | **96.00** | **AWS**          | **~10.1%** |

---

## 5. Key Findings

* AWS is more cost-effective for this workload by approximately 10%.
* Networking and database costs are major cost drivers.
* Azure performs competitively in storage pricing.
* Compute pricing differences are relatively small but consistent.

---

## 6. Regional Pricing Insight

Cloud pricing varies significantly by region. US-based regions are generally cheaper than African or smaller global regions due to infrastructure scale.

* US East regions tend to have lower compute and networking costs
* Some regions (e.g., Africa, South America) have higher egress pricing

---

## 7. Cost Optimization Strategies

### AWS

* Use Savings Plans for predictable workloads
* Use Reserved Instances for long-term stability
* Use S3 lifecycle policies to reduce storage cost

### Azure

* Use Reserved VM Instances
* Use Azure Hybrid Benefit for Windows workloads
* Use auto-scaling for cost control

---

## 8. Conclusion

Both AWS and Azure are capable cloud platforms with similar baseline pricing. However, AWS demonstrates a slight cost advantage for this architecture due to lower networking and database costs.

Azure becomes more competitive in enterprise environments where Microsoft licensing and ecosystem integration provide additional value.

The best provider depends on workload type, region, and long-term commitment strategy.

