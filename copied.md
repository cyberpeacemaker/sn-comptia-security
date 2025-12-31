This is a great catch. You are absolutely right—from a purely technical security standpoint, allowing fallback is **less secure** than requiring encryption.

However, in professional network engineering and cybersecurity, we have to balance the **"Security Triad" (CIA)**: Confidentiality, Integrity, and **Availability**.

If you "Require Security" on day one of a 3-month rollout, you break **Availability**. Half your servers won't be able to talk to the other half, and your business stops. Here is exactly what "fallback" means in this context and why it's used despite the security trade-off.

---





---

### Why we accept "Less Security" (for now)

You are right that an attacker could technically perform a **"Downgrade Attack"** during this phase. They could trick Machine A into thinking Machine B doesn't support IPsec, forcing the communication to stay unsecure.

We accept this risk during a rollout for three reasons:

* **Connectivity is King:** During a migration, "working but unsecure" is usually considered better than "secure but broken."
* **Gradual Hardening:** As more machines are updated, the *percentage* of your traffic that is encrypted naturally increases from 0% to 100%.
* **The "Final Switch":** On the very last day of the 3-month rollout, once you verify every machine is updated, you change the policy from "Allow Fallback" to **"Require Security."** This is when you "lock the door" and disable all unsecure communication.

### Summary of the Strategy

| Phase | Policy Setting | Security Level | Business Impact |
| --- | --- | --- | --- |
| **Rollout (Months 1-3)** | **Allow Fallback** | Medium (mixed) | **Zero Downtime** |
| **Post-Rollout (Final)** | **Require Security** | High (enforced) | Secure & Fully Functional |

> **Analogy:** It’s like installing a new keycard system in an office building. For the first week, you keep the old physical locks functional so people who haven't received their new cards yet don't get locked out in the cold. Once everyone has a card, you remove the old locks.

Would you like to see how a **Downgrade Attack** actually works so you can see the specific risk you're concerned about?