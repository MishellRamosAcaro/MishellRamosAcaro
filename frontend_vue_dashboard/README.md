# Frontend Vue Dashboard

## Project overview / Descripción general
Starter dashboard built with Vue and TypeScript to showcase analytics, ML insights, and modular UI components. It highlights clean state management, reusable charts, and security-conscious frontend practices.

## Architecture / Arquitectura
```mermaid
graph TD
    U-->|[User]|Browser| A [Vue SPA]
    A -->|API calls| B[API Gateway]
    A -->|State updates| C[Store (Pinia/Vuex)]
    A -->|Charts & Widgets| D[Components Library]
    C -->|Persists| E[Local Storage (scoped)]
    A -->|Telemetry| F[Monitoring / Sentry]
```

- **Vue SPA:** Routed single-page app built with Vite and TypeScript.
- **Store:** Centralized state (Pinia/Vuex) with typed modules.
- **Components Library:** Reusable charts, tables, and cards for analytics.
- **API Gateway:** Backend endpoints consumed via secure HTTP clients.
- **Monitoring:** Hooks for error tracking and performance metrics.

## Tech stack / Stack técnico
- Language: TypeScript
- Framework: Vue 3 + Vite
- UI: Component library friendly (e.g., Vuetify/Tailwind, to be decided)
- Tooling (suggested): vitest, eslint, prettier, cypress

## Installation & Run / Instalación y ejecución
1. Install dependencies:
   ```bash
   npm install
   ```
2. Start development server:
   ```bash
   npm run dev
   ```
3. Build for production:
   ```bash
   npm run build
   ```
4. Run tests (once added):
   ```bash
   npm run test:unit
   npm run test:e2e
   ```

## Folder structure / Estructura de carpetas
- `src/components/` — Reusable UI components.
- `src/views/` — Routed views/pages.
- `src/store/` — Global state management.
- `src/services/` — API clients and adapters.
- `tests/unit/` and `tests/e2e/` — Vitest and Cypress suites.

## Roadmap / Mejoras futuras
- Add authentication-aware layouts and protected routes.
- Include accessibility audits and performance budgets.
- Integrate analytics widgets for ML predictions and metrics.
- Configure CI for linting, testing, and preview deployments.

## Security / Seguridad
- Sanitize and validate all user-facing inputs.
- Use scoped storage with clear expiration for tokens; prefer httpOnly cookies when backend supports it.
- Enforce HTTPS-only assets and strict Content Security Policy recommendations.
- Guard API clients against injection by centralizing request builders.
