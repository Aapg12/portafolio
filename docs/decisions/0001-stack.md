# 0001 — Elección del stack

- **Fecha:** 2026-11-14
- **Estado:** Aceptada

## Contexto

El portafolio es una web de contenido: presenta tres proyectos como casos de
estudio y cambia poco una vez publicada. Aun así necesita varias funciones:
dos idiomas (español e inglés), modo claro y oscuro, transiciones entre
páginas, animaciones SVG y un formulario de contacto seguro.

Además de presentar mi trabajo, el proyecto tiene que demostrar mi perfil
full stack con enfoque en seguridad y servirme para aprender tecnologías
nuevas sin abandonar las que ya domino.

## Decisión

- **Frontend: Astro + TypeScript (strict).** Genera HTML estático, envía casi
  cero JavaScript al navegador y trae de serie lo que necesito: i18n,
  View Transitions y content collections para escribir los proyectos en
  Markdown con tipos comprobados.
- **Estilos: CSS puro con design tokens.** Sin frameworks de estilos, para
  dominar variables CSS, cascada y especificidad, que son la base del modo
  oscuro.
- **API de contacto: ASP.NET Core.** Validación de entradas, rate limiting
  integrado y tests con xUnit.
- **Infraestructura: Docker Compose + Caddy en un VPS.** Caddy sirve los
  estáticos, hace de proxy inverso hacia la API y gestiona HTTPS
  automáticamente.

## Alternativas descartadas

- **Next.js:** lo conozco, pero está pensado para aplicaciones con mucha
  lógica en servidor. Para una web de contenido añade JavaScript y
  complejidad que no necesito.
- **Angular:** es el framework que más domino, pero está orientado a
  aplicaciones empresariales. Para una web estática resulta pesado y no me
  aportaría aprendizaje nuevo.
- **NestJS para la API:** ya lo uso en Bitácora y en el ERP de la Federación
  Venezolana. Usar .NET aquí permite que el portafolio demuestre los dos
  ecosistemas.
- **Hosting estático gestionado (Netlify, Vercel):** más cómodo, pero me
  quitaría la práctica de administrar y asegurar un servidor propio.

## Consecuencias

**Positivas**

- Web muy rápida y con poca superficie de ataque, porque no hay código
  ejecutándose en el servidor en cada visita.
- Aprendo Astro, CSS avanzado y administración de servidores.
- El repositorio muestra frontend, backend, infraestructura y seguridad.

**Negativas**

- Curva de aprendizaje de Astro: avanzaré más despacio al principio.
- Dos lenguajes en un repo (TypeScript y C#) implican dos toolchains y dos
  pipelines de CI.
- Mantener un VPS propio me hace responsable de su seguridad y sus
  actualizaciones.
