<p align="center">
  <img src="https://raw.githubusercontent.com/Orux-Solutions/.github/main/profile/assets/banner.svg" alt="Áurea Ecosystem" width="100%" />
</p>

<p align="center">
  <strong>Plataforma SaaS Multi-Tenant modular de alto rendimiento para gestión integral de negocios y servicios</strong>
</p>

<p align="center">
  <a href="https://github.com/Orux-Solutions/orux-docs"><img src="https://img.shields.io/badge/Docs-Central_Architecture-8b5cf6?style=for-the-badge&logo=gitbook&logoColor=white" alt="Docs"/></a>
  <a href="https://github.com/Orux-Solutions/backoffice-fe-orux"><img src="https://img.shields.io/badge/Frontend-React_19_%2B_Vite-61dafb?style=for-the-badge&logo=react&logoColor=black" alt="Frontend"/></a>
  <a href="https://github.com/Orux-Solutions/backoffice-be-orux"><img src="https://img.shields.io/badge/Backend-NestJS_%2B_MongoDB-e0234e?style=for-the-badge&logo=nestjs&logoColor=white" alt="Backend"/></a>
  <a href="https://github.com/Orux-Solutions/orux-ci"><img src="https://img.shields.io/badge/CI%2FCD-Automated_Workflows-2088FF?style=for-the-badge&logo=githubactions&logoColor=white" alt="CI/CD"/></a>
</p>

---

### 🌐 Ecosistema de Repositorios

| Repositorio | Rol en el Ecosistema | Stack Tecnológico | Acceso |
| :--- | :--- | :--- | :---: |
| [**`orux-docs`**](https://github.com/Orux-Solutions/orux-docs) | **Documentación Central**: Arquitectura canónica, especificaciones técnicas de módulos dinámicos, ADRs y guías de contribución. | Markdown · Mermaid · JSON Schema | Public |
| [**`backoffice-fe-orux`**](https://github.com/Orux-Solutions/backoffice-fe-orux) | **Frontend del Backoffice**: Interfaz de operador multi-tenant con activación dinámica de componentes por capabilities. | React 19 · Vite · TailwindCSS v4 · TanStack Query · Zustand | Public |
| [**`backoffice-be-orux`**](https://github.com/Orux-Solutions/backoffice-be-orux) | **API Core Backend**: Motor transaccional con aislamiento estricto por tenant, autenticación JWT y guards de autorización. | NestJS · TypeScript · MongoDB · Mongoose | Public |
| [**`orux-ci`**](https://github.com/Orux-Solutions/orux-ci) | **Infraestructura CI/CD**: Pipelines reutilizables, validaciones de commits, trazabilidad automatizada de issues y releases. | GitHub Actions · Python · Docker | Public |

---

### 📐 Principios de Arquitectura

El ecosistema **Áurea** se rige por especificaciones técnicas rigurosas para garantizar escalabilidad, seguridad multi-inquilino y consistencia en el código:

#### 1. Jerarquía Canónica Estricta de 3 Niveles
```text
1. SECCIÓN   (Área departamental macro: services, commerce, gastronomy, crm, marketing, core)
   └── 2. PÁGINA   (Pantalla concreta navegable: bookings, catalog, orders, pos, tables)
         └── 3. MÓDULOS (Capabilities dinámicas que se activan/desactivan según el plan del tenant)
```

#### 2. Seguridad & Aislamiento Tenant-Scoped
* **El backend es la única fuente de verdad para autorización.** Las validaciones frontend optimizan la UX pero jamás sustituyen las guards en los endpoints.
* **Aislamiento Multi-Tenant Estricto:** Toda consulta o mutación a la base de datos filtra de forma obligatoria e inmutable por `tenantId`.
* **Zero-Leakage:** Respuestas `403 Forbidden` neutrales que nunca exponen la existencia de recursos de otros inquilinos.

#### 3. Módulos Dinámicos & Capabilities
* Cada funcionalidad dentro de una página (`sección.página.módulo`) es evaluada contra las capabilities activas del tenant y del plan comercial suscrito.

---

### 🛠️ Stack Tecnológico Global

<p align="left">
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/React_19-20232A?style=flat-square&logo=react&logoColor=61DAFB" alt="React" />
  <img src="https://img.shields.io/badge/Vite-646CFF?style=flat-square&logo=vite&logoColor=white" alt="Vite" />
  <img src="https://img.shields.io/badge/Tailwind_CSS_v4-38B2AC?style=flat-square&logo=tailwind-css&logoColor=white" alt="Tailwind" />
  <img src="https://img.shields.io/badge/NestJS-E0234E?style=flat-square&logo=nestjs&logoColor=white" alt="NestJS" />
  <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" alt="MongoDB" />
  <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=github-actions&logoColor=white" alt="GitHub Actions" />
</p>

---

### 📖 Primeros Pasos y Contribución

Para explorar los lineamientos de arquitectura, convenciones de ramas y desarrollo local:
* Consultá el [**Mapa de Documentación en orux-docs**](https://github.com/Orux-Solutions/orux-docs).
* Revisá la [**Guía de Contribución**](https://github.com/Orux-Solutions/orux-docs/blob/main/docs/contributing.md).

<div align="center">
  <sub>© 2026 Áurea Ecosystem · Built for modern modular business operations</sub>
</div>
