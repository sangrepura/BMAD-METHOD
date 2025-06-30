# Technical Architecture Document: Coastal Sites (v1.3)

## 1. Introduction
This document defines the fullstack architecture for the Coastal Sites platform, prioritizing unambiguous instructions for AI-driven development.

* **Foundational Approach:** We are creating a **proprietary agency boilerplate** built on a modern stack, designed as a "factory" for producing websites.
* **Architectural Principles:** 1) Developer Velocity & Reusability, 2) Cost-Effective Scalability, 3) Security by Design.
* **Core Technical Strategy:** The system uses a **Turborepo-managed monorepo**, with backend logic implemented as **Next.js Route Handlers**. Configuration is managed via `.env` files and platform-level variables, with no secrets committed to Git.

## 2. The Coastal Sites Method (AI-Accelerated Workflow)
This proprietary framework is our core "secret sauce."

* **Core Philosophy:** Human experts act as "Vibe CEOs" directing specialized AI agents who perform the methodical work. The end-goal is a hyper-automated production line.
* **Production Line:** A document-driven process: Project Brief -> PRD -> UI/UX Spec -> Architecture -> Development.
* **Two-Phase Model:** 1) **Planning & Design** in a Web UI for creative work. 2) **Development & Implementation** in an IDE using sharded stories for focused execution.

## 3. High-Level Architecture
* **Platform:** **Vercel** for hosting and deployment.
* **Database:** **Neon** serverless PostgreSQL, leveraging its **database branching** for safe, isolated development and testing.
* **Authentication:** **Clerk** for production-ready, enterprise-grade user and client authentication.
* **Repository & Versioning:** A Turborepo-managed monorepo, using **Changesets** for versioning shared packages.

## 4. Tech Stack (Definitive)
| Category       | Technology         | Version         |
| :---           | :---               | :---            |
| Language       | TypeScript         | `5.4.5`         |
| Framework      | Next.js            | `14.2.3`        |
| Styling        | Tailwind CSS       | `4.1.x`         |
| UI Primitives  | ShadCN UI / Radix  | `~0.8.0`        |
| Database       | Neon (PostgreSQL)  | `16`            |
| CMS            | PayloadCMS         | `3.0.0-beta.27` |
| Authentication | Clerk              | `5.1.x`         |
| Monorepo Tool  | Turborepo          | `2.0.0`         |
| Package Manager| pnpm               | `9.1.0`         |
| Testing        | Vitest             | `1.6.0`         |
| Deployment     | Vercel             | N/A             |

## 5. Data Models & Database Schema
* **Agency Operations Schema:** A robust SQL schema defines `Business`, `Client`, `Project`, `Deliverable`, and `Invoice` tables, using `ENUM` types for data integrity.
* **CMS Architecture:** A flexible, **Block-Based Content** strategy using PayloadCMS's Blocks feature, allowing for the creation of a library of reusable content sections.
* **Versioning:** All shared UI and CMS components will be versioned to prevent breaking changes in client projects.

## 6. Components & Workflows
* **Core Applications:** `apps/internal/agency-site`, `apps/internal/client-portal`. Client projects will reside in `apps/clients/`.
* **Core Packages:** `packages/ui` (our "Coastal UI" library), `packages/cms-starters` (reusable PayloadCMS configs), `packages/lib` (shared utilities), and `packages/database` (migrations).
* **E-commerce Flow:** A secure sequence using server-side price calculation and Stripe Webhooks for order creation to ensure reliability and prevent client-side manipulation.
* **Deployment:** A CI/CD pipeline managed by Vercel. Each pull request generates a **preview deployment** connected to its own **isolated database branch** from Neon.
* **Database Migrations:** An automated process using Vercel **Deployment Hooks** will run database migrations immediately after a successful production deployment, ensuring the schema and code are always in sync.

## 7. Coding & Testing Standards
* **Coding Standards:** Strict enforcement of TypeScript, Prettier for formatting, and ESLint for static analysis.
* **Test Strategy:** A "testing pyramid" approach using **Vitest** for unit/integration tests and **Playwright** for E2E tests on critical flows. Unit tests must have >80% coverage for shared packages.