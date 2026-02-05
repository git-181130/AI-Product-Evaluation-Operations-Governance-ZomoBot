# Executive Summary

**AI Product Evaluation, Operations & Governance — ZomoBot**

---

## Problem

Modern GenAI products often fail **not because they are inaccurate**, but because their **behaviour influences users in unsafe ways**.

In trust-sensitive domains, risks emerge from:

- Overconfident or authoritative tone  
- False precision presented as guaranteed guidance  
- Disproportionate escalation in ambiguous situations  
- Subtle erosion of user judgment and agency  

These failures are **behavioural, not technical**, and frequently pass traditional accuracy or policy checks.  
Once released, such risks are difficult to detect, govern, or roll back.

**ZomoBot was evaluated to answer a single product-critical question:**

> *Is this AI system safe and governable enough to be released to real users?*

---

## Approach

This project applied an **end-to-end AI Product Evaluation, Operations, and Governance framework**, designed to surface **real-world behavioural risk** and translate it into **defensible release decisions**.

---

### 1. Evaluation Framework (EvalOps)

Evaluation was structured, repeatable, and decision-oriented:

- **Evaluation Charter** defining authority and decision rules  
- **Evaluation Dimensions** aligned to AUMI (AI–User–Model Interaction), including:
  - Tone and framing  
  - Response structure and actionability  
  - Escalation proportionality  
  - Misuse and panic risk  
  - Hallucination and false precision  
  - Boundary and refusal integrity  
- **Category-based testing**, not random prompts  

#### Key Evaluation Scenarios

- Everyday low-risk food questions  
- Ambiguous or mild symptom scenarios  
- Child and vulnerable-user contexts  
- Time-based or rule-seeking queries  
- Boundary-challenging and persistence prompts  

Evaluation focused on **plausible user interpretation and action**, not model intent.

---

### 2. Behavioural Risk Analysis

Behavioural evaluation treated AI responses as **user experiences**, not text outputs.

Key behavioural dimensions analysed:

- Whether tone induced calm versus panic  
- Whether precision masked uncertainty  
- Whether escalation matched evidence  
- Whether authority cues reduced user judgment  

Failures were assessed as **risk signals**, even when answers were factually correct.

---

### 3. Risk & Safety Modelling

Findings were interpreted through a formal **Safety Risk Model**, covering:

- Behavioural safety risk  
- Hallucination and false precision risk  
- Misuse and panic induction  
- Boundary and scope drift  
- Child and vulnerable-context amplification  
- Edge-case instability under ambiguity  

Risk severity was based on **plausible real-world impact**, not frequency.

---

### 4. Operations & Governance

Evaluation findings were operationalised through:

- Incident classification  
- Root Cause Analysis (RCA)  
- Mitigation and re-test loops  
- Release gating and no-ship logic  
- Explicit decision ownership and auditability  

**“No-ship” was treated as a first-class operational outcome**, not a failure.

---

## Outcomes

### 1. Systemic Risk Patterns Identified

Across scenarios and variations, ZomoBot exhibited **reproducible behavioural risk patterns**, including:

- **False precision** — variable guidance presented as fixed or guaranteed  
- **Over-escalation** — urgency introduced in ambiguous, low-risk contexts  
- **Authority overreach** — framing that reduced user judgment  
- **Boundary instability** — partial compliance under repeated or pressured prompts  

These were **system-level behaviours**, not isolated errors.

---

### 2. Mitigation Was Insufficient

Mitigation attempts (tone softening, phrasing changes) were evaluated through controlled re-testing.

Results:

- Improvements were superficial  
- Risk patterns re-emerged under variation  
- New inconsistencies were introduced  

This indicated **instruction- or design-level root causes**, not prompt-level defects.

---

### 3. Operational Readiness Was Not Met

Given the identified risks:

- Behavioural failures could not be reliably constrained  
- Post-release governance would be insufficient  
- “Ship and monitor” would shift risk to users  

The system was deemed **not governable at release time**.

---

## Key Decisions

### Decision 1: Classify Behavioural Failures as Safety-Critical

Behavioural risks (panic induction, false certainty, authority cues) were treated as **release-relevant safety issues**, even without factual error.

---

### Decision 2: Reject Prompt-Level Fixes as Sufficient Mitigation

Fixes that improved individual responses but failed under variation were **explicitly rejected**.

---

### Decision 3: Enforce Release Gating

Based on evaluation, risk, operations, and governance criteria:

## **Final Decision: NO-SHIP**

This decision was:

- Evidence-based  
- Documented  
- Auditable  
- Explicitly owned  

No risk acceptance criteria were met.

---

## Final Takeaway

This project demonstrates a core principle of responsible AI Product Operations:

> **AI systems should not be released because they are often helpful —  
> they should be released only when unsafe behaviour is reliably constrained.**

ZomoBot was **correctly blocked from release** because its behavioural risks could not be governed with sufficient confidence.

That outcome reflects **operational maturity**, not failure.
