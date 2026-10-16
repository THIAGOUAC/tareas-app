# ✅ App de Tareas — React + Node.js

Aplicación full-stack de lista de tareas (CRUD) con **React (Vite)** en el frontend y una **API REST en Node.js + Express** en el backend.

Práctica de la **Guía 8** — Plataformas para el Desarrollo de Aplicaciones · Ingeniería de Sistemas · 2026-II

## 🌐 Demo en vivo

| Parte | URL |
|---|---|
| Frontend (Vercel) | https://TU-APP.vercel.app |
| API (Render) | https://TU-API.onrender.com/api/tareas |

> ⏳ La API está en el plan gratuito de Render: si no se usó en 15 min, la primera carga tarda ~1 minuto en despertar.

## 🧱 Tecnologías

- **Frontend:** React 18, Vite 5
- **Backend:** Node.js 18+, Express 4, CORS
- **Despliegue:** Vercel (frontend) + Render (backend)

## 📁 Estructura

```
tareas-app/
├── server/          ← Backend (API REST)
│   ├── package.json
│   └── index.js
└── client/          ← Frontend (React + Vite)
    ├── index.html
    ├── vite.config.js
    ├── .env.example
    └── src/
        ├── main.jsx
        ├── App.jsx
        ├── App.css
        └── components/
            ├── Formulario.jsx
            ├── ListaTareas.jsx
            └── Tarea.jsx
```

## 🔌 Endpoints de la API

| Verbo | Ruta | Acción | Respuesta |
|---|---|---|---|
| GET | `/api/tareas` | Lista todas las tareas | 200 |
| POST | `/api/tareas` | Crea una tarea `{ "titulo": "..." }` | 201 / 400 |
| PUT | `/api/tareas/:id` | Completa / descompleta `{ "completada": true }` | 200 / 404 |
| DELETE | `/api/tareas/:id` | Elimina la tarea | 204 / 404 |

## 💻 Ejecución local

Requisito: Node.js v18 o superior (`node -v`).

**Terminal 1 — Backend**
```bash
cd server
npm install
npm run dev      # http://localhost:3001/api/tareas
```

**Terminal 2 — Frontend**
```bash
cd client
npm install
npm run dev      # http://localhost:5173
```

## 🚀 Despliegue

### Backend en Render
1. New → Web Service → conectar este repositorio.
2. Root Directory: `server` · Build: `npm install` · Start: `node index.js` · Instance: Free.
3. Variable de entorno: `CLIENTE_URL` = URL del frontend en Vercel (sin `/` al final).

### Frontend en Vercel
1. Add New → Project → importar este repositorio.
2. Root Directory: `client` (Vercel detecta Vite).
3. Build: `npm run build` · Output: `dist`.
4. Variable de entorno: `VITE_API_URL` = `https://TU-API.onrender.com/api/tareas`.

## 🔐 Variables de entorno

| Variable | Dónde | Para qué |
|---|---|---|
| `PORT` | Render (automática) | Puerto del servidor |
| `CLIENTE_URL` | Render | Origen permitido por CORS |
| `VITE_API_URL` | Vercel | URL de la API que consume React |

Los archivos `.env` no se suben al repositorio (ver `.gitignore`).

## 📸 Capturas

### Panel de Render
![Render](capturas/render.png)

### Panel de Vercel
![Vercel](capturas/vercel.png)

### App en vivo
![App](capturas/app.png)

## 👤 Autor

TU NOMBRE — TU CÓDIGO
