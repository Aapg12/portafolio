# Portafolio — Andrés Pariche

## Qué es

Mi portafolio personal como desarrollador full stack. Presenta mis proyectos
como casos de estudio: el problema, las decisiones técnicas y el resultado.

El diseño sigue una estética editorial japonesa: espacio negativo (_ma_),
tipografía con mucho contraste y un único acento bermellón.

El propio portafolio es también un proyecto de aprendizaje: lo construyo por
fases aplicando buenas prácticas de full stack, seguridad y DevOps.

## Stack

**Frontend**

- Astro + TypeScript (modo strict)
- CSS con design tokens (variables CSS), sin frameworks de estilos
- View Transitions y animaciones con CSS / Web Animations API

**Backend** _(planificado — Fase 5)_

- API de contacto en ASP.NET Core
- Validación de entradas, rate limiting y protección antispam

**Infraestructura** _(planificado — Fase 2)_

- Docker Compose
- Caddy como servidor web y proxy inverso (HTTPS automático)
- VPS propio

**Seguridad y CI** _(planificado — Fase 6)_

- GitHub Actions
- Gitleaks (secretos), CodeQL (SAST), Trivy (contenedores),
  OWASP ZAP (DAST), Dependabot
- Playwright + axe (tests E2E y accesibilidad)

## Estructura

web/ → Frontend en Astro
api/ → API de contacto en ASP.NET Core
infra/ → Docker Compose y configuración de Caddy
docs/ → Documentación y decisiones técnicas (ADR)

## Estado

- [x] Fase 0 — Estructura del repositorio y convenciones
- [ ] Fase 1 — Web estática en español
- [ ] Fase 2 — Despliegue en VPS con Docker + Caddy
- [ ] Fase 3 — Design tokens y modo oscuro
- [ ] Fase 4 — Versión en inglés (i18n)
- [ ] Fase 5 — API de contacto segura
- [ ] Fase 6 — Pipeline DevSecOps
- [ ] Fase 7 — Animaciones y View Transitions
- [ ] Fase 8 — Auditoría final (Lighthouse, ZAP, securityheaders)

## Cómo arrancarlo

Pendiente.

## Decisiones técnicas

Ver [docs/decisions](docs/decisions/).
