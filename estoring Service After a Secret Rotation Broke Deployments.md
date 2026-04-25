### **Interview‑Style Answer: Restoring Service After a Secret Rotation Broke Deployments**

If deployments start failing after a secret was rotated, my first priority is to **restore service safely without introducing security risks**.

First, I would **pause the deployment pipeline** to stop repeated failures and prevent partial or inconsistent releases. Then I would quickly assess the **blast radius**—checking whether only new deployments are failing or if existing production services are also impacted. In most cases, running services continue to work with the old secret until restarted.

Next, I would **validate the rotated secret** by checking:

*   Whether the new secret value is correct
*   Whether it has been propagated to all required locations (CI/CD pipeline, deployment config, runtime environment)
*   Whether the service or pipeline still has permission to access it (for example, IAM or RBAC issues)

To restore service safely, I would take one of these controlled paths:

*   **Rollback if necessary:** Temporarily revert to the previous working secret (if policy allows) to immediately unblock deployments.
*   **Fix forward (preferred):** Update the deployment configuration to use the new secret correctly, test it in a lower environment, and then redeploy to production in a controlled rollout.

Once deployments succeed, I would **restart or redeploy affected services** so they pick up the correct secret and closely **monitor logs and metrics** to ensure stability.

Finally, I would implement **prevention measures**, such as automating secret propagation, adding validation checks in the pipeline to catch secret issues early, and testing secret rotation regularly in non‑production environments.

**One‑line interview summary:**

> *I restore service by stopping the pipeline, validating and correcting the rotated secret through rollback or fix‑forward, redeploying safely, and strengthening secret management to prevent future failures.*
