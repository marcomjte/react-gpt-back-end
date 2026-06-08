# react-gpt-back-end

Backend de la aplicación **React GPT**, construido con [NestJS](https://nestjs.com/) y la [API de OpenAI](https://platform.openai.com/). Expone endpoints REST que son consumidos por el frontend en React.

## Stack tecnológico

- **Framework**: NestJS 10
- **Lenguaje**: TypeScript 5
- **IA**: OpenAI SDK v4
- **Archivos/imágenes**: Multer + Sharp
- **Validación**: class-validator / class-transformer
- **Runtime**: Node.js

## Requisitos previos

- Node.js 18+
- Una API Key de OpenAI → [platform.openai.com/api-keys](https://platform.openai.com/api-keys)

## Instalación (desarrollo)

1. Clonar el repositorio:

```bash
git clone https://github.com/marcomjte/react-gpt-back-end.git
cd react-gpt-back-end
```

2. Instalar dependencias:

```bash
npm install -f
```

3. Crear el archivo de variables de entorno basado en la plantilla:

```bash
cp .env.template .env
```

4. Editar `.env` y agregar tu API Key:

```env
OPENAI_API_KEY=sk-...
SERVER_URL=http://localhost:3000
```

5. Levantar el servidor en modo desarrollo:

```bash
npm run start:dev
```

El servidor quedará corriendo en `http://localhost:3000`.

## Scripts disponibles

| Comando | Descripción |
|---|---|
| `npm run start:dev` | Servidor en modo watch (desarrollo) |
| `npm run start:debug` | Servidor con debugger adjunto |
| `npm run start:prod` | Servidor en producción (requiere build previo) |
| `npm run build` | Compilar TypeScript a `dist/` |
| `npm run lint` | Linting con ESLint + auto-fix |
| `npm run format` | Formato con Prettier |
| `npm run test` | Ejecutar tests unitarios |
| `npm run test:cov` | Tests con reporte de cobertura |
| `npm run test:e2e` | Tests end-to-end |

## Variables de entorno

| Variable | Descripción |
|---|---|
| `OPENAI_API_KEY` | Clave de la API de OpenAI (requerida) |
| `SERVER_URL` | URL base del servidor (default: `http://localhost:3000`) |

## Estructura del proyecto

```
src/
├── gpt/              # Módulo principal de integración con OpenAI
│   ├── dtos/         # Data Transfer Objects (validación de entrada)
│   └── ...
generated/            # Archivos generados (imágenes, audio, etc.)
```

## Licencia

MIT
