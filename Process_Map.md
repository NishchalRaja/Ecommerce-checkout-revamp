# Process Map — E-Commerce Checkout Revamp

## As-Is Process (Current State)

```mermaid
flowchart TD
    A[Shopper adds items to cart] --> B[Clicks Checkout]
    B --> C{Logged in?}
    C -- No --> D[Forced Account Creation Page]
    D --> E[Enter Shipping Address Page]
    C -- Yes --> E
    E --> F[Enter Billing Address Page]
    F --> G[Enter Payment Details Page - Card Only]
    G --> H[Review Order Page]
    H --> I[Place Order]
    I --> J[Confirmation]
    D -.->|~38% drop-off| X1[Abandon]
    G -.->|~24% drop-off| X2[Abandon]
```

**Pain points identified**
- Mandatory account creation before any shipping or payment info is entered — the single largest drop-off point.
- Five separate page loads, each an additional chance to abandon.
- Card-only payment excludes wallet users, disproportionately affecting mobile shoppers.
- No visibility into remaining steps or running total until the review page.

## To-Be Process (Redesigned)

```mermaid
flowchart TD
    A[Shopper adds items to cart] --> B[Clicks Checkout]
    B --> C[Single-Page Checkout Loads]
    C --> D[Guest or Log In choice - inline, optional]
    D --> E[Shipping section - expandable]
    E --> F[Payment section - Card, Apple Pay, Google Pay, PayPal]
    F --> G[Review section - order summary always visible]
    G --> H[Place Order]
    H --> I[Confirmation + optional one-click account creation]
```

**Key changes**
- Account creation moved from a blocking gate to an optional, post-purchase prompt.
- Shipping, billing, and payment collapsed into one scrollable page with expandable sections, replacing five separate pages.
- Payment options expanded to include digital wallets, cutting manual data entry.
- A persistent order summary and step indicator (not shown in the diagram, see [BRD](./BRD.md) FR-04/FR-05) remain visible throughout.

## Estimated Funnel Impact

| Stage | As-Is Completion | To-Be Target |
|---|---|---|
| Reach checkout | 100% | 100% |
| Pass account/guest step | 62% | 95% |
| Complete shipping + payment | 76% of remaining | 90% of remaining |
| Place order (overall) | 28% | 45% |
