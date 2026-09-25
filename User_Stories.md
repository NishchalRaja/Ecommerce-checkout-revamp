# User Stories - E-Commerce Checkout Revamp

Derived from the [BRD](./BRD.md) functional requirements (FR-01 through FR-08), organized into five epics.

---

## Epic 1: Guest Checkout
*Related requirements: FR-01, FR-06*

### US-01 — Guest checkout access
**As a** first-time shopper, **I want** to complete my purchase without creating an account, **so that** I can check out quickly without extra friction.

**Acceptance Criteria**
- Given items in cart, when the shopper proceeds to checkout, then a "Continue as Guest" option appears alongside "Log In."
- Given guest checkout is selected, when the order is completed, then only email, shipping, and payment details were required — no password.
- Given a guest order is confirmed, when the confirmation page loads, then a one-click account-creation prompt appears using the details already entered.

**Priority:** Must Have | **Story Points:** 5

### US-02 — Returning user autofill
**As a** returning logged-in user, **I want** my saved address and payment method to autofill, **so that** I don't re-enter information I've already saved.

**Acceptance Criteria**
- Given a logged-in user has a saved address, when they reach checkout, then the address is pre-filled and editable.
- Given a logged-in user has a saved card, when they reach payment, then the last 4 digits display with an option to use it or add a new one.

**Priority:** Must Have | **Story Points:** 3

---

## Epic 2: Single-Page Checkout Redesign
*Related requirements: FR-02, FR-07*

### US-03 — Consolidated checkout page
**As a** shopper, **I want** shipping, billing, and payment on one page with clear sections, **so that** I can complete checkout without multiple page reloads.

**Acceptance Criteria**
- Given checkout starts, when the page loads, then shipping, billing, and payment appear as expandable sections on a single scrollable page.
- Given a section is completed, when the shopper moves to the next, then the completed section collapses into a summary view.

**Priority:** Must Have | **Story Points:** 8

### US-04 — Inline field validation
**As a** shopper, **I want** immediate feedback on invalid fields (expired card, malformed zip, etc.), **so that** I can fix errors before submitting.

**Acceptance Criteria**
- Given a field value is entered, when the shopper tabs out, then invalid input is flagged immediately with a specific error message.
- Given all fields are valid, when the shopper reaches review, then nothing blocks submission.

**Priority:** Should Have | **Story Points:** 5

---

## Epic 3: Digital Wallet Integration
*Related requirement: FR-03*

### US-05 — One-tap wallet payment
**As a** mobile shopper, **I want** to pay with Apple Pay or Google Pay, **so that** I don't have to type card details on a small screen.

**Acceptance Criteria**
- Given a supported device/browser, when payment is reached, then Apple Pay/Google Pay appears above manual card entry.
- Given a wallet option is selected, when the shopper authenticates via biometrics, then the order completes without further form entry.

**Priority:** Must Have | **Story Points:** 8

### US-06 — PayPal checkout
**As a** shopper who prefers not to enter card details on-site, **I want** to pay via PayPal, **so that** I can use my existing PayPal balance or linked card.

**Acceptance Criteria**
- Given PayPal is selected, when the shopper authenticates and returns, then order details are pre-filled from PayPal's response.

**Priority:** Should Have | **Story Points:** 5

---

## Epic 4: Mobile Checkout Optimization
*Related requirements: FR-08, NFR-04*

### US-07 — Native autofill support
**As a** mobile shopper, **I want** my browser/OS to autofill address and card fields, **so that** I can check out faster on my phone.

**Acceptance Criteria**
- Given a mobile shopper taps an address field, when the OS offers saved data, then it populates the correct fields.
- Given a mobile shopper taps the card-number field, when a saved card is offered, then it populates without layout shift.

**Priority:** Must Have | **Story Points:** 5

---

## Epic 5: Order Summary & Progress Indicator
*Related requirements: FR-04, FR-05*

### US-08 — Persistent order summary
**As a** shopper, **I want** to see my cart contents and total cost throughout checkout, **so that** I have confidence in what I'm paying without navigating away.

**Acceptance Criteria**
- Given the shopper is anywhere in checkout, when they scroll, then an order summary panel (items, subtotal, shipping estimate, total) stays visible.

**Priority:** Must Have | **Story Points:** 3

### US-09 — Checkout progress indicator
**As a** shopper, **I want** to see how many steps remain, **so that** I know what to expect and don't abandon out of uncertainty.

**Acceptance Criteria**
- Given checkout starts, when the page loads, then a 3-step indicator (Shipping → Payment → Review) shows the shopper's current position.

**Priority:** Should Have | **Story Points:** 2

---

## Sprint Planning Summary

**Total estimated story points:** 44

| Sprint | Stories | Points |
|---|---|---|
| Sprint 1 | US-01, US-02, US-03, US-08, US-09 | 21 |
| Sprint 2 | US-04, US-05, US-06, US-07 | 23 |
