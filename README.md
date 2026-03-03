# MisUsuarios API

API REST para gestionar navegadores y ventanas con huella dactilar personalizada usando Node.js, Express y Puppeteer. Incluye cliente Python para automatización.

## Características
- Crear navegadores con configuración de fingerprint (userAgent, etc.)
- Abrir y cerrar ventanas en navegadores Puppeteer
- API fácil de consumir desde cualquier lenguaje
- Ejemplo de integración con Python

## Instalación

### 1. Instalar dependencias Node.js
```bash
npm install
```

### 2. Iniciar el servidor
```bash
node server.js
```
El servidor estará disponible en `http://localhost:3000`

### 3. Instalar dependencias Python
```bash
pip install requests
```

## Uso de la API

### Crear navegador
```http
POST /api/browser/create
{
  "browserId": "test1",
  "fingerprintConfig": {
    "userAgent": "Mozilla/5.0 ..."
  }
}
```

### Abrir ventana
```http
POST /api/window/create
{
  "browserId": "test1",
  "url": "https://google.com"
}
```

### Cerrar ventana
```http
POST /api/window/close
{
  "windowId": "..."
}
```

### Cerrar navegador
```http
POST /api/browser/close
{
  "browserId": "test1"
}
```

### Estado de la API
```http
GET /api/status
```

## Cliente Python

Ejecuta el ejemplo:
```bash
python client.py
```

## Subir a GitHub

1. Inicializa git:
   ```bash
   git init
   git add .
   git commit -m "Primer commit: API Node.js y cliente Python"
   git branch -M main
   git remote add origin https://github.com/samuel28058/misusuarios-api.git
   git push -u origin main
   ```
2. Reemplaza `samuel28058` por tu usuario real de GitHub.

---

¡Listo para compartir y automatizar navegadores! 🚀