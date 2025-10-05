#  Capstone Project: DevOps Transformation for KMIT Solutions Services

## 1. **Project Overview**

**Company:** KMIT Solutions Services
**Client:** Banking Domain Customer
**Existing Application:** Internet Banking Suite (Spring Boot Java Applications)

KMIT Solutions currently operates multiple layered Java Spring Boot applications — *Internet Banking*, *Withdraw Service*, *Deposit Service*, and *Customer Care* — deployed on **Apache Tomcat** servers. The applications serve critical banking operations but face increasing challenges due to scalability, maintainability, and slow release cycles.

---
<img width="512" height="512" alt="image" src="https://github.com/user-attachments/assets/c4b3630c-7172-4985-bbf2-58bc279cf1de" />


## 2. **Current Challenges**

1. **Manual Build and Deployment**

   * Developers manually build JAR/WAR files using local Maven commands.
   * Deployments to Tomcat servers are done manually, causing inconsistencies.

2. **Frequent Code Changes & Developer Coordination**

   * Multiple developers commit code independently.
   * Merging changes into the final branch is complex and error-prone.

3. **Testing Bottlenecks**

   * Integration testing is manual and time-consuming.
   * Developers lose productivity waiting for test results.

4. **Dependency and Environment Drift**

   * Application works differently some times in Test, UAT, and Production environments.
   * Configuration mismatches cause failures during production deployment.

5. **Infrastructure & Configuration Management**

   * Server setup, configuration, and software installations are handled manually.
   * No Infrastructure-as-Code (IaC) or configuration automation.

6. **Lack of Monitoring**

   * No standard automated alerting or monitoring mechanism.
   * Issues are discovered post-impact rather than proactively.

---

