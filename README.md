# Junior App · Frontend

Frontend de Junior App desarrollado con React, TypeScript y Vite. Actualmente contiene la pantalla inicial de la plantilla, con un contador de ejemplo y estilos CSS propios.

## Stack tecnológico

Las versiones indicadas corresponden a las declaradas en [package.json](./package.json).

| Tecnología | Versión | Uso |
| --- | --- | --- |
| React y React DOM | `^19.3.1` | Componentes e interfaz de usuario en el navegador. |
| TypeScript | `~6.0.3` | Tipado estático del código. |
| Vite | `^8.3.6` | Servidor de desarrollo y compilación para producción. |
| @vitejs/plugin-react | `^6.1.2` | Integración de React con Vite y actualización de componentes durante el desarrollo. |
| ESLint | `^10.14.0` | Análisis estático, con reglas de TypeScript, React Hooks y React Refresh. |
| CSS | — | Estilos globales y del componente principal. |

Las dependencias se gestionan con npm. [package-lock.json](./package-lock.json) registra las versiones resueltas para reproducir la instalación.

## Requisitos

- Node.js compatible con Vite y ESLint: `20.19.x` o superior dentro de la rama 20, `22.13.x` o superior dentro de la rama 22, o `24` en adelante.
- npm disponible en el entorno.

## Instalación y desarrollo

Desde la raíz del repositorio:

```bash
cd front
npm ci
npm run dev
```

Abre la dirección que indique Vite en la terminal. Los cambios en los componentes y estilos se reflejan durante el desarrollo mediante HMR.

La aplicación actual no requiere variables de entorno ni conexión a un backend para ejecutarse.

## Comandos disponibles

Ejecuta estos comandos desde la carpeta del frontend:

| Comando | Descripción |
| --- | --- |
| `npm run dev` | Inicia el servidor de desarrollo de Vite. |
| `npm run build` | Comprueba TypeScript con `tsc -b` y genera la compilación en `dist/`. |
| `npm run lint` | Ejecuta ESLint sobre el proyecto. |
| `npm run preview` | Sirve localmente la compilación generada para revisarla. Requiere ejecutar antes `npm run build`. |

## Estructura

```text
front/
├── public/             # Recursos estáticos servidos directamente
├── src/
│   ├── assets/         # Imágenes y recursos importados desde el código
│   ├── App.tsx         # Componente principal y pantalla inicial
│   ├── App.css         # Estilos del componente principal
│   ├── index.css       # Estilos globales
│   └── main.tsx        # Montaje de React en el DOM con StrictMode
├── index.html          # Documento HTML de entrada
├── vite.config.ts      # Configuración de Vite y del plugin de React
├── eslint.config.js    # Reglas de análisis estático
├── tsconfig.json       # Referencias a las configuraciones de TypeScript
├── tsconfig.app.json   # Configuración TypeScript de la aplicación
├── tsconfig.node.json  # Configuración TypeScript para las herramientas
├── package.json        # Dependencias y scripts
└── package-lock.json   # Versiones resueltas de las dependencias
```

Para modificar la pantalla inicial, edita [src/App.tsx](./src/App.tsx) y sus estilos en [src/App.css](./src/App.css). Los estilos compartidos se encuentran en [src/index.css](./src/index.css).

## Validación y producción

Antes de entregar cambios, ejecuta:

```bash
npm run lint
npm run build
```

El proyecto todavía no tiene un framework ni un script de pruebas automatizadas configurado.

Para revisar la compilación localmente:

```bash
npm run preview
```

El resultado de `npm run build` se genera en `dist/` y puede publicarse en un servicio de alojamiento de archivos estáticos. El comando `preview` se utiliza para comprobar esa compilación en el entorno local.
