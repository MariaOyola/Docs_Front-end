# Docs FaceLit

Documentación centralizada del proyecto: prototipo, tableros de trabajo, repositorios y credenciales de entorno necesarias para levantar el proyecto.

---

## 🎨 Prototipo (Figma)

[Ver diseño en Figma](https://www.figma.com/design/fRPJLroPiL9Jeu4zhfy0Zf/FaceID-completo?node-id=745-1789&t=pSYeXb7vLPRofZC8-1)

---

## 📋 Kanban (GitHub Projects)

| Tablero | Descripción | Link |
|---|---|---|
| Backlog Front-end | Backlog para avanzar el desarrollo del front | [Ver tablero](https://github.com/orgs/FaceID-Proyect-2026/projects/1/views/1) |
| Backlog Back-end | Backlog para el desarrollo del back | [Ver tablero](https://github.com/orgs/FaceID-Proyect-2026/projects/7) |

---

## 💻 Repositorios (Móvil y Web)

### 1. Front-end (rama `dev`)

Repositorio para ver el avance del front-end con datos quemados (mock). Aquí solo se refleja el progreso visual del front como tal.

**Para ejecutar:** revisar la imagen de referencia con los comandos de instalación.

<img width="605" height="113" alt="image" src="https://github.com/user-attachments/assets/e9a9176e-20f8-4595-963e-e03b6c6db22f" />

**Repo:** https://github.com/FaceID-Proyect-2026/FaceLit/tree/dev

---

### 2. Front-end (rama `feature/profile-integration`)

Mismo repositorio del front, pero en esta rama sí está integrada la conexión con el backend.

**Comandos de ejecución:**
```bash
npx expo install expo@~54.0.37 expo-constants@~18.0.14
npx expo start -c
```

**Repo:** https://github.com/FaceID-Proyect-2026/FaceLit/tree/feature/profile-integration

---

### 3. Base de Datos (rama `main` — en producción)

**Comandos de ejecución:**
```bash
docker compose -p facelit-docker-compose down --volumes --remove-orphans
docker compose -p facelit-docker-compose up -d postgres
docker compose -p facelit-docker-compose --profile tooling run --rm liquibase validate
docker compose -p facelit-docker-compose --profile tooling run --rm liquibase update
```

**Repo:** https://github.com/FaceID-Proyect-2026/FaceLit-DB

---

### 4. Back-end (rama `hotfix-03`)

**Cómo se ejecuta:**

<img width="101" height="53" alt="image" src="https://github.com/user-attachments/assets/ccc11604-4213-4db0-b642-b3bbac56ca59" />

Como el archivo `.env` está ignorado por el `.gitignore` (no se sube al repo), aquí está su contenido para que el proyecto funcione correctamente:

```env
# ─── BASE DE DATOS ───────────────────────────────────────────
DB_URL=jdbc:postgresql://localhost:5439/facelit-db
DB_USERNAME=facelit_user
DB_PASSWORD=facelit_password

# ─── DOCKER / POSTGRES ───────────────────────────────────────
POSTGRES_DB=facelit-db
POSTGRES_USER=facelit_user
POSTGRES_PASSWORD=facelit_password
POSTGRES_PORT=5439

# ─── JWT ─────────────────────────────────────────────────────
JWT_SECRET=FaceLit2025$ClaveSecretaSuperSegura#SENA@Backend!

# ─── GMAIL ───────────────────────────────────────────────────
MAIL_USERNAME=facelit.system@gmail.com
MAIL_PASSWORD=pgkyeljftwhclykr
```

**Repo:** https://github.com/FaceID-Proyect-2026/FaceLit-Backend/tree/hotfix-03

---

## 📁 Documentación (Drive)

[Ver carpeta en Google Drive](https://drive.google.com/drive/folders/12F8O-47Z7yD8U6IcIgIYGl62aKOA1aNf?usp=drive_link)

