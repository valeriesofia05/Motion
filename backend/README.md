# Backend Motion

API HTTP construida con Next.js App Router y TypeScript. Los endpoints se implementan como Route Handlers en `src/app/api/**/route.ts`. Next.js también puede servir páginas web; en este repositorio se usa principalmente para el servidor de la API.

## Requisitos e instalación

Se requiere Node.js 22 o superior para la versión de pnpm fijada en este proyecto.

```bash
cd backend
pnpm install
pnpm dev
```

La API local se ejecuta en `http://localhost:3000`. Endpoint inicial: `GET /api/health`.

Scripts disponibles: `pnpm dev` para desarrollo, `pnpm lint` para ESLint, `pnpm build` para generar la compilación y `pnpm start` para servirla.

## Organización propuesta

- `src/app/api/health/`: estado del servicio.
- `src/app/api/auth/`: registro, verificación de correo e inicio de sesión (JN: HU-02, HU-03 y HU-04).
- `src/app/api/tasks/`: lectura, edición y eliminación de tareas (FA: HU-08, HU-09 y HU-10).

Las rutas de negocio requieren definir persistencia, validación, seguridad y contrato de respuestas antes de implementarse. Coordinen el modelo de usuario y autenticación con el módulo de tareas.
