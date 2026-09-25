# Business Requirements Document (BRD)
## E-Commerce Checkout Revamp - ShopSwift

**Prepared by:** Nishchal Raja, Business Analyst
**Version:** 1.0 | **Status:** Approved for Development

---

## 1. Document Control

| Version | Stage | Change Description |
|---|---|---|
| 0.1 | Week 1 | Initial draft following stakeholder kickoff |
| 0.2 | Week 2 | Updated after funnel analysis and stakeholder interviews |
| 1.0 | Week 3 | Final version, approved by Product & Engineering leads |

## 2. Project Overview

ShopSwift is a mid-sized online retailer selling home goods. Site traffic has grown steadily quarter over quarter, but overall conversion has stayed flat — the checkout funnel is the primary suspect.

### 2.1 Business Objective
Reduce cart abandonment at checkout and increase completed-order conversion by simplifying the checkout flow, removing the account-creation barrier, and adding modern payment options.

### 2.2 Problem Statement
Checkout abandonment currently sits at **72%**, well above the site's target conversion rate. Funnel analysis shows the steepest drop-offs occur at (1) the mandatory account-creation step and (2) payment-details entry — both disproportionately on mobile.

## 3. Scope

**In Scope**
- Redesign of the checkout flow (cart → shipping → payment → review → confirmation)
- Guest checkout capability
- Digital wallet integration (Apple Pay, Google Pay, PayPal)
- Mobile checkout UX improvements
- Persistent order summary and progress indicator

**Out of Scope**
- Product catalog / product detail page changes
- Loyalty program redesign
- Post-purchase order tracking
- Payment gateway migration (existing gateway retained; wallets added as additional methods on top of it)

## 4. Stakeholders

| Stakeholder | Role | Primary Interest |
|---|---|---|
| VP Product | Sponsor | Conversion rate improvement |
| Engineering Lead | Delivery | Technical feasibility, sprint capacity |
| UX Designer | Delivery | Checkout redesign, design system fit |
| Customer Support Manager | SME | Recurring complaint themes |
| Marketing Manager | SME | Promo-code and cart messaging |
| QA Lead | Delivery | Test coverage for payment flows |

## 5. Business Requirements

| ID | Requirement |
|---|---|
| BR-01 | Reduce checkout abandonment from 72% to 55% within two quarters of launch |
| BR-02 | Enable purchase completion without mandatory account creation |
| BR-03 | Support at least two additional payment methods beyond credit/debit card |
| BR-04 | Reduce average checkout completion time from 4.5 minutes to under 2 minutes |
| BR-05 | Achieve mobile checkout completion parity (±5pp) with desktop |

## 6. Functional Requirements

| ID | Requirement |
|---|---|
| FR-01 | System shall allow users to complete checkout as a guest, capturing only email, shipping, and payment details |
| FR-02 | System shall consolidate shipping, billing, and payment entry into a single scrollable page with expandable sections, replacing the current 5-page flow |
| FR-03 | System shall offer Apple Pay, Google Pay, and PayPal as one-tap options alongside standard card entry |
| FR-04 | System shall display a persistent order summary panel (items, subtotal, shipping estimate) throughout checkout |
| FR-05 | System shall display a 3-step progress indicator (Shipping → Payment → Review) |
| FR-06 | System shall auto-populate saved address/payment details for returning logged-in users while still permitting guest flow |
| FR-07 | System shall validate form fields inline in real time rather than only on submission |
| FR-08 | Mobile checkout shall support native OS/browser autofill for address and card fields |

## 7. Non-Functional Requirements

| ID | Requirement |
|---|---|
| NFR-01 | Checkout page load under 2 seconds on 4G mobile connections |
| NFR-02 | Payment handling remains PCI-DSS compliant with no increase in PCI scope |
| NFR-03 | Checkout meets WCAG 2.1 AA accessibility standard |
| NFR-04 | Checkout renders without layout defects on Safari iOS, Chrome Android, and Samsung Internet |

## 8. Assumptions & Constraints

- Existing payment gateway supports wallet tokenization without requiring a new PCI assessment.
- No changes needed to inventory or tax-calculation services.
- Engineering capacity is available for a single two-sprint delivery window.
- Design-system components exist for standard form fields; the progress indicator is a new component requiring design sign-off.

## 9. Risks

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| Wallet integration delayed by gateway sandbox access | Medium | High | Request sandbox credentials in Sprint 0 |
| Guest checkout increases fraud/chargeback rate | Medium | Medium | Retain existing fraud-scoring rules; monitor post-launch |
| Single-page checkout increases initial page weight | Low | Medium | Lazy-load payment SDKs until the user reaches the payment section |

## 10. Success Metrics / KPIs

- Checkout abandonment rate (target: ≤55%)
- Mobile checkout completion rate (target: parity with desktop, ±5pp)
- Average checkout completion time (target: <2 minutes)
- Adoption rate of new wallet payment options

## 11. Sign-off

| Name/Role | Approval |
|---|---|
| VP Product (Sponsor) | Approved |
| Engineering Lead | Approved |
