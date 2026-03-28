# Legend Alu — Production Platform Case Study

**Live site:** [legendalu.com](https://legendalu.com)

> End-to-end full-stack platform for a 25-year-old Egyptian aluminum manufacturer exporting to Europe and the Middle East.

---

## Overview

Legend Alu needed a production-grade web platform to present their catalog of aluminum profiles to international buyers. The business had no digital presence — only physical catalogues and manual sales processes. I designed and built the entire platform from scratch: UI/UX, backend, database, deployment, and third-party integrations.

<img width="1897" height="915" alt="Screenshot 2026-03-28 113929" src="https://github.com/user-attachments/assets/16121e55-3bde-4def-a7ea-b11dc3cd9811" />

---

## Technical Stack

| Layer | Technology |
|---|---|
| Frontend | Next.js, Tailwind CSS, Framer Motion |
| State Management | Zustand |
| Backend | Next.js API Routes |
| Database | MongoDB |
| i18n / RTL | next-intl, RTL layout support |
| Email | Zoho Mail (professional domain integration) |
| Deployment | Vercel |

---

## Key Engineering Challenges

### 1. Catalog Data Modeling at Scale
The client had 755+ aluminum profiles across 18 categories — existing only in physical catalogues. I manually structured and curated the entire dataset, extracting product images, defining consistent schema across categories, and modeling it into MongoDB with filtering and search in mind.

**Decision:** MongoDB over relational DB here was deliberate — product profiles have varying attributes per category (different specs for doors vs. windows vs. industrial profiles), making a flexible document model the right fit.

<img width="1897" height="916" alt="Screenshot 2026-03-28 114014" src="https://github.com/user-attachments/assets/81b46b5e-0a4e-4d6d-bf8f-80c780583664" />

### 2. Multilingual + RTL Interface
The platform serves Arabic and English markets with full RTL layout switching. This isn't just `direction: rtl` on a wrapper — it required rethinking component layout logic, icon mirroring, spacing direction, and typography hierarchy across both languages.

**Used:** `next-intl` for translation management and locale routing, custom Tailwind config for RTL-aware utilities.

<img width="1897" height="916" alt="Screenshot 2026-03-28 114044" src="https://github.com/user-attachments/assets/af185d58-5064-4d17-a745-dc5093bf535d" />

### 3. Automated Client Communication
Integrated Zoho Mail with a professional domain to automate inquiry responses. Buyers submitting product inquiries receive immediate branded confirmation emails, reducing manual follow-up load on the client.

### 4. Performance
Focused on LCP optimization, lazy loading for product images, and code splitting. The catalog pages load fast despite the large image-heavy product dataset.

---

## What I Owned

This was a solo, end-to-end engagement:

- **Discovery** — Translated physical catalogues and client requirements into a technical spec
- **Design** — UI/UX design from scratch, no template
- **Frontend** — All components, pages, animations, responsive layouts
- **Backend** — API routes, database queries, email integration
- **Data** — Manual data modeling and entry of 755+ products
- **Deployment** — Vercel setup, domain configuration, environment management
- **Handoff** — Client training and documentation

<img width="1901" height="913" alt="Screenshot 2026-03-28 114120" src="https://github.com/user-attachments/assets/3c2adcad-4df1-47b4-a948-f91702166d66" />

---

## Outcome

A live, production platform actively used by an exporting manufacturer to reach international buyers across Europe and the Middle East.

→ **[legendalu.com](https://legendalu.com)**
