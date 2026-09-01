FaceLit — Documentación Front-end y Backend

Documentación general del proyecto FaceLit, incluyendo prototipado, tableros Kanban, repositorios, ejecución del Front-end, Backend y Base de Datos.

1. 🎨 Prototipado — Figma

Diseños y prototipos del proyecto realizados en Figma:

{"fallbackMarkdown":"Prototipo FaceID — Figma","reference":{"matched_text":"","prefix":null,"start_idx":758,"end_idx":894,"safe_urls":[],"refs":[],"alt":"Prototipo FaceID — Figma","prompt_text":"Prototipo FaceID — Figma","type":"url","item":{"title":"Prototipo FaceID — Figma","url":"https://www.figma.com/design/fRPJLroPiL9Jeu4zhfy0Zf/FaceID-completo?node-id=745-1789&t=pSYeXb7vLPRofZC8-1&utm_source=chatgpt.com","attribution":"figma.com","pub_date":null,"snippet":null,"attribution_segments":null,"supporting_websites":null,"refs":[],"hue":null,"attributions":null},"logo":null,"layout":null,"title":"Prototipo FaceID — Figma"},"showLoginRequiredCard":false}

2. 📋 Kanban — GitHub Projects
Front-end

Tablero utilizado para gestionar las tareas y avances relacionados con el Front-end:

{"fallbackMarkdown":"Kanban Front-end","reference":{"matched_text":"","prefix":null,"start_idx":1040,"end_idx":1125,"safe_urls":[],"refs":[],"alt":"Kanban Front-end","prompt_text":"Kanban Front-end","type":"url","item":{"title":"Kanban Front-end","url":"https://github.com/orgs/FaceID-Proyect-2026/projects/1/views/1?utm_source=chatgpt.com","attribution":"github.com","pub_date":null,"snippet":null,"attribution_segments":null,"supporting_websites":null,"refs":[],"hue":null,"attributions":null},"logo":null,"layout":null,"title":"Kanban Front-end"},"showLoginRequiredCard":false}

Back-end

Tablero utilizado para gestionar las tareas y avances relacionados con el Back-end:

{"fallbackMarkdown":"Kanban Back-end","reference":{"matched_text":"","prefix":null,"start_idx":1230,"end_idx":1306,"safe_urls":[],"refs":[],"alt":"Kanban Back-end","prompt_text":"Kanban Back-end","type":"url","title":"Kanban Back-end","item":{"title":"Kanban Back-end","url":"https://github.com/orgs/FaceID-Proyect-2026/projects/7?utm_source=chatgpt.com","attribution":"github.com","pub_date":null,"snippet":null,"attribution_segments":null,"supporting_websites":null,"refs":[],"hue":null,"attributions":null},"layout":null,"logo":null},"showLoginRequiredCard":false}

3. 💻 Repositorios
3.1 Front-end — FaceLit

Repositorio principal del Front-end desarrollado para el proyecto.

Rama dev

Esta rama contiene los avances del Front-end con datos quemados (mock data).

Su objetivo principal es visualizar y revisar el avance de las interfaces sin depender de la conexión con el Back-end.

{"fallbackMarkdown":"Repositorio Front-end — rama dev","reference":{"matched_text":"","prefix":null,"start_idx":1648,"end_idx":1742,"safe_urls":[],"refs":[],"alt":"Repositorio Front-end — rama dev","prompt_text":"Repositorio Front-end — rama dev","type":"url","item":{"title":"Repositorio Front-end — rama dev","url":"https://github.com/FaceID-Proyect-2026/FaceLit/tree/dev?utm_source=chatgpt.com","attribution":"github.com","pub_date":null,"snippet":null,"attribution_segments":null,"supporting_websites":null,"refs":[],"hue":null,"attributions":null},"logo":null,"layout":null,"title":"Repositorio Front-end — rama dev"},"showLoginRequiredCard":false}

Nota: Esta rama se utiliza principalmente para visualizar los avances de las interfaces y funcionalidades del Front-end.

3.2 Front-end integrado con Back-end

Esta es la misma aplicación Front-end, pero utilizando una rama diferente que contiene la integración con el Back-end.

Rama feature/profile-integration

{"fallbackMarkdown":"Repositorio Front-end — integración Back-end","reference":{"matched_text":"","prefix":null,"start_idx":2082,"end_idx":2212,"safe_urls":[],"refs":[],"alt":"Repositorio Front-end — integración Back-end","prompt_text":"Repositorio Front-end — integración Back-end","type":"url","item":{"title":"Repositorio Front-end — integración Back-end","url":"https://github.com/FaceID-Proyect-2026/FaceLit/tree/feature/profile-integration?utm_source=chatgpt.com","attribution":"github.com","pub_date":null,"snippet":null,"attribution_segments":null,"supporting_websites":null,"refs":[],"hue":null,"attributions":null},"logo":null,"layout":null,"title":"Repositorio Front-end — integración Back-end"},"showLoginRequiredCard":false}

Instalación y ejecución

Ejecutar los siguientes comandos:

npx expo install expo@~54.0.37 expo-constants@~18.0.14
npx expo start -c


El comando npx expo start -c inicia el proyecto y limpia la caché de Expo.

4. 🗄️ Base de Datos

Repositorio correspondiente a la Base de Datos del proyecto.

Actualmente se encuentra en la rama principal (main) y contiene la configuración relacionada con PostgreSQL y Liquibase.

{"fallbackMarkdown":"Repositorio FaceLit-DB","reference":{"matched_text":"","prefix":null,"start_idx":2656,"end_idx":2734,"safe_urls":[],"refs":[],"alt":"Repositorio FaceLit-DB","prompt_text":"Repositorio FaceLit-DB","type":"url","item":{"title":"Repositorio FaceLit-DB","url":"https://github.com/FaceID-Proyect-2026/FaceLit-DB?utm_source=chatgpt.com","attribution":"github.com","pub_date":null,"snippet":null,"attribution_segments":null,"supporting_websites":null,"refs":[],"hue":null,"attributions":null},"logo":null,"layout":null,"title":"Repositorio FaceLit-DB"},"showLoginRequiredCard":false}

4.1 Ejecución de la Base de Datos

Primero detener y eliminar los contenedores existentes:

docker compose -p facelit-docker-compose down --volumes --remove-orphans


Luego iniciar PostgreSQL:

docker compose -p facelit-docker-compose up -d postgres


Validar las migraciones de Liquibase:

docker compose -p facelit-docker-compose --profile tooling run --rm liquibase validate


Finalmente, ejecutar las migraciones:

docker compose -p facelit-docker-compose --profile tooling run --rm liquibase update

Orden recomendado
1. Detener y limpiar contenedores
        ↓
2. Levantar PostgreSQL
        ↓
3. Validar Liquibase
        ↓
4. Ejecutar las migraciones

5. ⚙️ Back-end

Repositorio correspondiente al Back-end del proyecto.

Actualmente se está trabajando sobre la rama:

hotfix-03


{"fallbackMarkdown":"Repositorio FaceLit-Backend — hotfix-03","reference":{"matched_text":"","prefix":null,"start_idx":3609,"end_idx":3724,"safe_urls":[],"refs":[],"alt":"Repositorio FaceLit-Backend — hotfix-03","prompt_text":"Repositorio FaceLit-Backend — hotfix-03","type":"url","item":{"title":"Repositorio FaceLit-Backend — hotfix-03","url":"https://github.com/FaceID-Proyect-2026/FaceLit-Backend/tree/hotfix-03?utm_source=chatgpt.com","attribution":"github.com","pub_date":null,"snippet":null,"attribution_segments":null,"supporting_websites":null,"refs":[],"hue":null,"attributions":null},"logo":null,"layout":null,"title":"Repositorio FaceLit-Backend — hotfix-03"},"showLoginRequiredCard":false}

5.1 Variables de entorno

El archivo .env no se encuentra dentro del repositorio debido a que está incluido en el .gitignore.

Para ejecutar correctamente el Back-end, se debe crear un archivo .env local con las variables necesarias.

Ejemplo de .env
# ─── BASE DE DATOS ───────────────────────────────────────────
DB_URL=jdbc:postgresql://localhost:5439/facelit-db
DB_USERNAME=facelit_user
DB_PASSWORD=<TU_PASSWORD>

# ─── DOCKER / POSTGRES ───────────────────────────────────────
POSTGRES_DB=facelit-db
POSTGRES_USER=facelit_user
POSTGRES_PASSWORD=<TU_PASSWORD>
POSTGRES_PORT=5439

# ─── JWT ─────────────────────────────────────────────────────
JWT_SECRET=<TU_JWT_SECRET>

# ─── GMAIL ───────────────────────────────────────────────────
MAIL_USERNAME=<TU_EMAIL>
MAIL_PASSWORD=<TU_PASSWORD>


⚠️ Seguridad: nunca subir el archivo .env al repositorio. Las contraseñas, secretos JWT y credenciales de correo deben mantenerse únicamente como variables de entorno o mediante un gestor de secretos.

6. 📚 Documentación adicional

Documentación complementaria del proyecto almacenada en Google Drive:

{"fallbackMarkdown":"Documentación del proyecto — Google Drive","reference":{"matched_text":"","prefix":null,"start_idx":4870,"end_idx":5005,"safe_urls":[],"refs":[],"alt":"Documentación del proyecto — Google Drive","prompt_text":"Documentación del proyecto — Google Drive","type":"url","item":{"title":"Documentación del proyecto — Google Drive","url":"https://drive.google.com/drive/folders/12F8O-47Z7yD8U6IcIgIYGl62aKOA1aNf?usp=drive_link&utm_source=chatgpt.com","attribution":"drive.google.com","pub_date":null,"snippet":null,"attribution_segments":null,"supporting_websites":null,"refs":[],"hue":null,"attributions":null},"logo":null,"layout":null,"title":"Documentación del proyecto — Google Drive"},"showLoginRequiredCard":false}

7. 🗂️ Resumen de recursos
Recurso	Descripción	Enlace
🎨 Figma	Prototipos y diseños	Figma
📋 Kanban Front-end	Gestión de tareas Front-end	GitHub Projects
📋 Kanban Back-end	Gestión de tareas Back-end	GitHub Projects
💻 FaceLit dev	Front-end con datos quemados	GitHub
🔗 FaceLit feature/profile-integration	Front-end integrado con Back-end	GitHub
🗄️ FaceLit-DB	Base de Datos	GitHub
⚙️ FaceLit-Backend	Back-end	GitHub
📚 Google Drive	Documentación complementaria	Drive
8. 🚀 Orden general para levantar el proyecto

Para trabajar con el proyecto completo, se recomienda seguir este orden:

┌─────────────────────┐
│  1. Base de Datos   │
│     PostgreSQL      │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│  2. Migraciones     │
│     Liquibase       │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│  3. Back-end        │
│     Spring/API      │
└──────────┬──────────┘
           ↓
┌─────────────────────┐
│  4. Front-end       │
│     Expo            │
└─────────────────────┘


De esta forma, el Front-end puede consumir los servicios proporcionados por el Back-end, y el Back-end puede conectarse correctamente con la Base de Datos.



