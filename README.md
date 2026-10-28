# Motion

Repositorio del proyecto organizado en dos aplicaciones independientes:

```text
frontend/   App móvil/web con Expo, React Native y TypeScript
backend/    API con Next.js Route Handlers y TypeScript
```

## Requisitos

- Node.js 20.9 o superior para Next.js.
- npm y Git.

## Instalar y ejecutar

Usamos pnpm 11 en ambas aplicaciones. Requiere Node.js 22 o superior y Corepack (o pnpm instalado). Instala las dependencias por separado:

```bash
cd frontend
pnpm install
pnpm start
```

En otra terminal:

```bash
cd backend
pnpm install
pnpm dev
```

La app Expo muestra opciones para abrir Android, iOS o web. El servidor Next.js queda en `http://localhost:3000`; su endpoint de comprobación es `http://localhost:3000/api/health`.

Para probar el frontend con el backend, configura después la URL base de la API según el dispositivo. En un emulador o teléfono, `localhost` puede referirse al propio dispositivo y no a la computadora.

## Historias backend

- `auth/`: registro, verificación de correo e inicio de sesión (JN: HU-02 a HU-04).
- `tasks/`: ver, editar y eliminar tareas (FA: HU-08 a HU-10).

Antes de implementar las historias, acuerden el contrato de la API, el modelo de datos, la base de datos y cómo se identifica el usuario autenticado. Cada persona trabaja en su módulo y coordina cambios compartidos mediante Pull Requests.

## Flujo de ramas

Usen `main` como rama estable y creen una rama corta por historia, por ejemplo `feature/HU-02-registro`. Abran un Pull Request hacia `main` y borren la rama de feature una vez integrado el PR. GitHub permite eliminar ramas ya fusionadas; los commits siguen formando parte del historial de `main`. No hace falta conservar una rama por cada historia completada.
