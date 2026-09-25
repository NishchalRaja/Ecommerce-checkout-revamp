# E-Commerce Checkout Revamp

**Author:** Nishchal Raja | Business Analyst
**Category:** Requirements Analysis / Process Improvement

> This is a self-directed portfolio project built around a simulated retailer, "ShopSwift," to demonstrate an end-to-end BA workflow — from problem framing through requirements, process mapping, and sprint-ready user stories.

---

## 📋 Executive Summary

ShopSwift, a fictional mid-sized online retailer, was losing 72% of shoppers at checkout despite healthy top-of-funnel traffic. This project analyzed the checkout funnel, identified the mandatory account-creation gate and limited payment options as the primary blockers, and produced a full requirements package — BRD, user stories, and process maps — for a redesigned, guest-friendly, single-page checkout.

---

## 🎯 Business Problem

### Context
ShopSwift's site traffic had grown steadily quarter over quarter, but overall conversion stayed flat. Checkout was the prime suspect, and the retailer had no documented checkout requirements or process map to work from.

### Challenge
Checkout abandonment sat at 72%, well above the site's target conversion rate, with the steepest drop-offs at the account-creation step and at payment-details entry — both worse on mobile than desktop.

### Objective
Define and document the requirements for a redesigned checkout that removes the account-creation barrier, adds modern payment methods, and cuts checkout time — reducing abandonment from 72% to a target of 55%.

---

## 📊 Methodology & Analysis Conducted

### Approach
A funnel-first analysis: identify where shoppers drop off, root-cause why, then translate findings into a requirements package a delivery team could build from directly.

### Data Collection
- Stakeholder interviews: Product, Engineering, Customer Support, and Marketing leads
- Checkout funnel/analytics review to pinpoint step-by-step drop-off rates
- Competitive benchmarking against modern checkout flows (guest checkout, wallet payments)
- Current-state process mapping of the existing 5-page checkout

### Tools & Techniques Used
- **Funnel analysis:** Quantified drop-off at each checkout step
- **Process mapping:** As-is and to-be flows (see [Process_Map.md](./Process_Map.md))
- **Root cause identification:** Isolated account creation and payment-method limits as primary causes
- **Requirements documentation:** BRD with business, functional, and non-functional requirements
- **Backlog structuring:** User stories with acceptance criteria, grouped into epics and estimated for two sprints

---

## 🔍 Key Findings

### Finding 1: Mandatory account creation is the single largest drop-off point
**Impact:** Roughly 38% of shoppers who reach checkout abandon at the forced account-creation step, before ever entering shipping or payment details.

**Evidence:**
- Funnel data shows only 62% of checkout starts pass this step
- Customer Support's top recurring complaint theme was "why do I need an account to buy one item"

### Finding 2: The five-page checkout multiplies opportunities to abandon
**Impact:** Each additional page load (shipping → billing → payment → review) is a fresh exit point, and checkout takes an average of 4.5 minutes to complete.

**Evidence:**
- Step-by-step funnel data shows incremental loss at every page transition
- Competitive benchmarking showed leading retailers consolidating checkout into one or two screens

### Finding 3: Card-only payment underserves mobile shoppers
**Impact:** Mobile checkout completion trails desktop, driven partly by the friction of manually typing card details on a small screen.

**Evidence:**
- No wallet-based payment options (Apple Pay, Google Pay, PayPal) exist today
- Payment-details entry is the second-largest drop-off point in the funnel, at ~24%

---

## 💡 Recommendations

### Recommendation 1: Make account creation optional
**Description:** Introduce guest checkout requiring only email, shipping, and payment details; offer one-click account creation after order confirmation.

**Benefits:**
- Removes the largest single drop-off point
- Preserves the option to convert guests to accounts post-purchase

**Implementation Timeline:** Sprint 1

### Recommendation 2: Consolidate to a single-page checkout
**Description:** Merge shipping, billing, and payment into one scrollable page with expandable sections and a persistent order summary and progress indicator.

**Benefits:**
- Fewer page loads means fewer exit points
- Persistent summary reduces uncertainty that drives abandonment

**Implementation Timeline:** Sprint 1–2

### Recommendation 3: Add digital wallet payments
**Description:** Introduce Apple Pay, Google Pay, and PayPal as one-tap alternatives to manual card entry.

**Benefits:**
- Cuts payment friction, especially on mobile
- Matches checkout options shoppers already expect from competitors

**Implementation Timeline:** Sprint 2

---

## 📈 Expected Impact & Business Value

| Metric | Current State | Projected State | Impact |
|---|---|---|---|
| Checkout abandonment rate | 72% | 55% | -17 percentage points |
| Average checkout completion time | 4.5 min | <2 min | ~55% faster |
| Mobile checkout completion | Below desktop | Parity (±5pp) | Closes mobile gap |
| Overall funnel completion (cart → order) | 28% | 45% | +17 percentage points |

**Overall Business Value:** A projected 17-point reduction in abandonment, applied against ShopSwift's existing checkout traffic, translates into a substantial lift in completed orders without any change in top-of-funnel spend.

---

## 📁 Project Files

This repository contains:

- `README.md` — This file
- `BRD.md` — Full business requirements document (objectives, scope, functional/non-functional requirements, risks)
- `User_Stories.md` — Backlog of user stories by epic, with acceptance criteria and sprint allocation
- `Process_Map.md` — As-is and to-be checkout flow diagrams with funnel impact estimates

---

## 🛠️ Technical Details

### Tools Used
- **Funnel/analytics review:** Identifying step-level drop-off rates
- **Mermaid diagrams:** As-is and to-be process flows
- **Requirements documentation:** BRD authoring, MoSCoW prioritization
- **Agile backlog structuring:** Epics, user stories, story points, sprint planning

### Data Sources
- Simulated checkout funnel data (constructed for this portfolio project)
- Simulated stakeholder interview themes (Product, Engineering, Support, Marketing)
- Public benchmarking of modern e-commerce checkout patterns

### Assumptions
- Existing payment gateway supports wallet tokenization without a new PCI assessment
- No changes required to inventory or tax-calculation services
- Engineering capacity available for a two-sprint delivery window

---

## 📝 Limitations & Caveats

- This is a simulated case study built for portfolio purposes, not a real client engagement — funnel figures and stakeholder quotes are illustrative, not audited data.
- Analysis assumes a single retailer archetype; findings may not generalize to marketplaces or B2B checkout flows.
- Fraud/chargeback impact of guest checkout is flagged as a risk but not modeled in detail.

---

## 🎓 Key Learnings

**What I learned from this project:**

1. The biggest checkout wins often come from removing a step entirely (account creation), not just polishing the steps that remain.
2. Translating funnel data into prioritized, acceptance-criteria-backed user stories makes a BRD immediately actionable for a delivery team.
3. Process mapping the as-is state first made it much easier to justify each to-be design decision with a specific pain point.

---

## 📞 Contact & Questions

**Author:** Nishchal Raja
**Email:** [your.email@example.com]
**LinkedIn:** [Your LinkedIn profile]

For questions about this analysis or project details, feel free to reach out!

---

## 📜 License & Usage

This analysis and recommendations are provided for educational and professional portfolio purposes.
