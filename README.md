---

# template-diocese

This repository hosts the **Journey Of Life** Diocese website template—built on Bitrix24 CRM Sites & Stores—to accelerate deployment of GDPR-compliant, multilingual diocesan sites with parish directories, bishop communications, events, and donations.

---

## Table of Contents

1. [Project Overview](#project-overview)  
2. [Features](#features)  
3. [Architecture & Tech Stack](#architecture--tech-stack)  
4. [Getting Started](#getting-started)  
   - [Prerequisites](#prerequisites)  
   - [Installation](#installation)  
   - [Configuration](#configuration)  
   - [Local Development](#local-development)  
5. [Directory Structure](#directory-structure)  
6. [Deployment](#deployment)  
7. [Contributing](#contributing)  
8. [Security & Compliance](#security--compliance)  
9. [License](#license)  
10. [Contact & Support](#contact--support)  

---

## Project Overview

The **gyvenimo-kelias-template-diocese** repository provides a turnkey website template for dioceses. It includes global layouts, shared components, and a tenant-onboarding dashboard for multi-tenant setups on Bitrix24. Designed for diocesan administrators, it supports parish listings, bishop messages, news, events, and donations across Lithuanian, English, and Russian.

---

## Features

- **Key Pages**  
  - Home with hero, value proposition, and CTA  
  - Diocese Overview & History  
  - Regional Parish Directory  
  - Bishop’s Message & Pastoral Letters  
  - News & Announcements Feed  
  - Event Calendar & Registration  
  - Secure Donation & E-Giving  
  - Contact & Location (Google Maps)  
  - Blog / Resources  
  - FAQ / Help Center  

- **Core Modules**  
  - Donation / Online Giving via Bitrix24 CRM  
  - Event Calendar / Ticketing  
  - Blog / News Feed Integration  
  - Parish Directory Component  
  - Staff / Leadership Profiles  
  - Social Media Integration  
  - Testimonials & Feedback  
  - Image Gallery & Media  
  - FAQ / Support Articles  

- **Design & Branding**  
  - Primary Colors: Deep Blue (#1A237E), Gold (#FFD700), White (#FFFFFF)  
  - Typography: Montserrat (headings), Roboto (body)  
  - Flat-style SVG icons with warm, accessible imagery  

---

## Architecture & Tech Stack

| Layer                  | Technology                                    |
|------------------------|-----------------------------------------------|
| Frontend               | Bitrix24 Site Builder, Semantic HTML5, SASS   |
| Shared Components      | SVG icon library, Montserrat & Roboto fonts   |
| CMS                    | 1C-Bitrix Multi-Site                          |
| CRM & E-Commerce       | Bitrix24 CRM Online Store Enterprise          |
| Middleware (optional)  | Django REST Framework, API Gateway            |
| Database               | PostgreSQL (structured), MongoDB (analytics)  |
| CI/CD                  | GitHub Actions, Docker                        |
| Hosting                | Linux Home Server / Google Cloud (hybrid)     |
| Containerization       | Kubernetes (optional scaling)                 |

---

## Getting Started

### Prerequisites

- Git 2.20+  
- Node.js 14+ & npm or Yarn  
- Access to Bitrix24 Sites & CRM modules  
- Docker (optional for local containers)  

### Installation

1. Clone the repo  
   ```bash
   git clone https://github.com/gyvenimo-kelias/gyvenimo-kelias-template-diocese.git
   cd gyvenimo-kelias-template-diocese
   ```
2. Install dependencies  
   ```bash
   npm install
   # or
   yarn install
   ```

### Configuration

1. Copy `.env.example` to `.env`  
2. Populate environment variables:  
   ```
   BITRIX24_WEBHOOK_URL=
   TEMPLATE_ID=DIOCESE
   DEFAULT_LANGUAGE=lt
   ```
3. Import the template ZIP via Bitrix24 admin and map pages.

### Local Development

```bash
npm run dev
```

Preview at `http://localhost:3000`. Edit SASS variables in `src/styles/variables.scss`.

---

## Directory Structure

```
/
├── .github/                  # CI/CD workflows
├── src/
│   ├── pages/                # Page templates (home, directory, events...)
│   ├── components/           # Shared UI components
│   ├── styles/               # SASS partials, variables, mixins
│   └── assets/               # Images, SVG icons
├── .env.example
├── package.json
└── docker-compose.yml        # Optional local containers
```

---

## Deployment

1. Build production assets:  
   ```bash
   npm run build
   ```
2. Package as Bitrix24-compatible ZIP.  
3. Import via Bitrix24 Sites → Templates → Import.  
4. Assign to diocese tenant subdomain.

---

## Contributing

1. Fork the repo  
2. Create a feature branch: `git checkout -b feature/XYZ`  
3. Commit with clear messages  
4. Push branch and open a Pull Request  
5. Ensure CI checks pass

Refer to [CONTRIBUTING.md](CONTRIBUTING.md) for full guidelines.

---

## Security & Compliance

- GDPR-compliant data handling  
- Cookie banner & Privacy Policy via Bitrix modules  
- Role-based access control (RBAC)  
- Regular dependency vulnerability scans  

---

## License

This template is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.

---

## Contact & Support

For assistance, reach out to:

- **Lead Architect:** Gintaras Kazlauskas  
- **Email:** gintaras.kazlauskas@gyvenimo-kelias.lt  
- **GitHub Issues:** https://github.com/gyvenimo-kelias/gyvenimo-kelias-template-diocese/issues
