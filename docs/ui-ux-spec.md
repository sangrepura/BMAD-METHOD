# Product Requirements Document (PRD): Coastal Sites (v1.2)

### Change Log
| Date       | Version | Description                                                                | Author   |
| :---       | :---    | :---                                                                       | :---     |
| 2025-06-29 | 1.2     | Incorporated PO recommendation to move Client Portal MVP to Epic 1.      | Sarah, PO|
| 2025-06-28 | 1.1     | Incorporated feedback on site structure, client portal, and tech stack. | John, PM |
| 2025-06-27 | 1.0     | Initial PRD draft                                                          | John, PM |

## 1. Requirements

### 1.1. Functional Requirements
* **FR1:** The system must build professional, single-page sites with smooth-scrolling sections.
* **FR2:** The system must support full e-commerce websites with shopping carts and checkouts.
* **FR3:** The system must integrate with Stripe for payment processing.
* **FR4:** The agency workflow must include brand identity and logo creation.
* **FR5:** All client sites must have foundational Local SEO applied.
* **FR6:** A secure client portal is required for project tracking, approvals, and payments.
* **FR7:** The system must support an ongoing maintenance retainer service.
* **FR8:** All client sites must have analytics integration.
* **FR9:** All client sites must be integrated with a Headless CMS (PayloadCMS).

### 1.2. Non-Functional Requirements
* **NFR1:** Performance: >90 Google PageSpeed score.
* **NFR2:** Speed of Delivery: <21-day delivery for core e-commerce package.
* **NFR3:** Responsiveness: Fully responsive across all devices.
* **NFR4:** Accessibility: WCAG 2.1 Level AA compliance.
* **NFR5:** Security: HTTPS and modern security best practices.

## 2. Epics & Stories

### Epic 1: Agency Foundation & Core Service Delivery
**Goal:** To establish the foundational code, assets, and processes required to successfully market the agency, onboard new clients via a basic client portal, and deliver the single-page "Digital Presence" website package.
* **Story 1.1:** Monorepo & Tooling Setup (Turborepo, pnpm, Vitest).
* **Story 1.2:** Develop Core Component Library (ShadCN, 21st.dev).
* **Story 1.3:** Integrate Headless CMS (PayloadCMS) & Analytics.
* **Story 1.4:** Develop the Coastal Sites Agency Website.
* **Story 1.5:** Define "Digital Presence" Package Workflow.
* **Story 1.6:** **Client Portal MVP - Authentication & Dashboard:** As a Client, I want to securely log in to a portal and see a dashboard listing my current projects and their status, so that I have a central place to manage my engagement with the agency.

### Epic 2: E-commerce Engine Service Rollout
**Goal:** To build the integrations and specialized components required to deliver the "E-commerce Engine" website package.
* **Story 2.1:** Integrate Headless E-commerce Backend.
* **Story 2.2:** Develop E-commerce UI Components.
* **Story 2.3:** Build Shopping Cart & Checkout Flow.

### Epic 3: Client Management Portal (Full)
**Goal:** To build a comprehensive portal where clients can track project progress, communicate with the agency, approve deliverables, and manage their invoices.
* **Story 3.1:** Project Progress & Approval System.
* **Story 3.2:** Invoice & Payment Integration.

### Epic 4: Client Retainer & Maintenance System
**Goal:** To develop the automated systems required to efficiently service clients on the "AI Maintenance & Growth" retainer.
* **Story 4.1:** Set up Automated Site Monitoring.
* **Story 4.2:** Create a Dependency Update Workflow.