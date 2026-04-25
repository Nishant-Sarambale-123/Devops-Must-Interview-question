### **Interview‑Style Answer (GitHub Actions Perspective): What are self‑hosted runners, and when would you use them?**

In **GitHub Actions**, **self‑hosted runners** are machines that we manage ourselves—such as on‑prem servers, cloud VMs, or Kubernetes pods—that execute GitHub Actions workflows instead of GitHub‑hosted runners. These runners are registered with a GitHub repository, organization, or enterprise and pull jobs directly from GitHub Actions.

### **When and why we use self‑hosted runners in GitHub Actions:**

1.  **Access to Private Network Resources**  
    We use self‑hosted runners when workflows need access to **private infrastructure**, such as internal databases, private APIs, on‑prem systems, or private Kubernetes (EKS) clusters that GitHub‑hosted runners cannot reach.

2.  **Security and Compliance**  
    Self‑hosted runners are useful when source code, secrets, or artifacts **must not leave our controlled environment**. This helps meet compliance or regulatory requirements by keeping everything within our VPC or data center.

3.  **Custom Tooling or Environment**  
    When builds require **custom software**, internal libraries, specific OS configurations, or licensed tools, self‑hosted runners give full control over the environment, which isn’t possible with standard GitHub‑hosted runners.

4.  **Performance and Cost Optimization**  
    For **long‑running or high‑frequency workflows**, self‑hosted runners can be faster and more cost‑effective since we avoid GitHub usage limits and reduce queue wait times.

5.  **Kubernetes and Autoscaling Use Cases**  
    In many setups, self‑hosted runners are deployed in **Kubernetes clusters** and auto‑scaled based on workload, which is ideal for dynamic CI/CD demands.

### **Example**

In one setup, we used **self‑hosted GitHub Actions runners on EC2 inside a private VPC**. This allowed our workflows to:

*   Deploy directly to a private EKS cluster
*   Access internal services securely
*   Use custom Docker images and tooling  
    while still being triggered and audited through GitHub Actions.

### **One‑line interview summary**

> *In GitHub Actions, self‑hosted runners are agents we manage ourselves, used when we need private network access, stronger security control, custom environments, or better performance than GitHub‑hosted runners.*

If you want, I can also explain:

*   How to **register and secure self‑hosted runners**
*   **Autoscaling GitHub Actions runners on Kubernetes**
*   Security **best practices and pitfalls** specific to GitHub Actions
