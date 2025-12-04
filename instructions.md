# Senior Engineering Manager — Systems Thinking & Architecture Exercise
*High-level strategy, decision-making, and technical leadership*

Thank you for taking the time to complete this exercise.  
This is not a coding assignment — we are evaluating **how you think**, how you make decisions, and how you communicate complex tradeoffs.

Please provide your answer in a file named **response.md**.

---

# Summary of the Scenario

Imagine a subscription-based commerce company that uses:

- a **billing provider** to manage subscriptions and recurring charges  
- a **backend system** that creates customer orders when subscriptions renew  
- an **e-commerce platform** to store and expose these orders  
- a **3PL partner** that retrieves orders nightly from the e-commerce platform to fulfill them  

Over time, misalignment between these systems has created challenges in subscription flows, product management, and fulfillment.

The company is evaluating whether the current e-commerce platform is still the right long-term fit or if a different approach is needed.

---

# Full Scenario

## Subscription & Order Flow Challenges
- Subscription logic lives outside the commerce platform  
- Timing issues or webhook failures can create inconsistent / duplicate orders  
- Supporting advanced subscription behavior requires workarounds  
- Debugging across systems is difficult  

## Product Management Challenges
- The e-commerce platform’s product/variant model does not reflect internal product rules  
- Custom attributes require manual sync or custom processes  
- No clear “source of truth” for product data  

## Fulfillment / 3PL Challenges
- The 3PL relies on the e-commerce platform as the record of orders  
- Platform limitations affect packaging logic, metadata, and shipping rules  
- Failed syncs cause downstream issues for support and operations  

**The core question:**  
Is the existing e-commerce platform still the right fit — or should the company refactor, replace, or rebuild this part of the system?

---

# Your Task

Provide a **high-level technical and strategic assessment**, focusing on how you would guide engineering direction and collaborate with cross-functional teams.

You do *not* need to design a full architecture.  
We are evaluating **reasoning, clarity, and leadership**.

---

# 1. Decision Framework  
Explain how you would evaluate whether the current e-commerce platform should remain in the architecture.

Consider:
- engineering concerns  
- operational concerns  
- product constraints  
- long-term scalability  

**Also include:**  
1–2 tools, platforms, or techniques you would use to support this evaluation.

---

# 2. Options Analysis  
Discuss the strengths and limitations of these paths:

1. **Keep the existing platform**, but isolate or refactor it  
2. **Replace it** with another commerce or subscription-focused platform  
3. **Build an internal service** for products, checkout, and order routing  
   (while keeping the current billing provider)

For each option, evaluate the impact on:
- complexity  
- product catalog modeling  
- subscription → order flow  
- fulfillment and 3PL behavior  
- cross-team collaboration  
- maintenance over time  

**Also include:**  
1–2 tools or platforms you might consider for each option.

---

# 3. Recommended Approach  
Provide your recommended path forward.

Consider:
- short- and medium-term engineering effort  
- reliability  
- product flexibility  
- team experience and capacity  
- long-term maintainability  

**Also include:**  
1–2 tools or technologies that would support your chosen direction.

---

# 4. High-Level Architecture (Optional Depth)
If you recommend reducing or replacing the commerce platform, describe at a high level what the future architecture *might* look like.

You may touch on:
- checkout and identity  
- product catalog as a source of truth  
- subscription alignment with the billing provider  
- order orchestration  
- fulfillment routing  
- event-driven communication  
- data consistency / retries  

**Also include:**  
1–2 tools or technologies you would consider for key components.

A diagram is welcome but not required.

---

# 5. Migration Strategy  
Explain how you would approach migration with minimal risk.

Consider:
- parallel systems  
- gradual rollout  
- product catalog sync  
- fallback mechanisms  
- 3PL cutover strategy  
- QA and communication with Ops, CS, and Product  

**Also include:**  
1–2 tools or processes to support migration and rollout.

---

# 6. Communication  
Explain how you would present your recommendation to:
- Product  
- Ops  
- CS  
- Leadership  

Focus on tradeoffs, clarity, and realistic expectations.

You may optionally reference tools for documentation or decision-tracking.

---

# Submission Guidelines
- Put your response in **response.md**  
- 1–3 pages is sufficient  
- Use bullet points or structure as you see fit  
- No coding required  

Thank you again for your time — we look forward to reviewing your work.
