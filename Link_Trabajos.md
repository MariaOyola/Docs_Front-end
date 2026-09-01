# Docs_Front-end

## Link_Prototipado (Figma)

https://www.figma.com/design/fRPJLroPiL9Jeu4zhfy0Zf/FaceID-completo?node-id=745-1789&t=pSYeXb7vLPRofZC8-1

## Kanban (Realizado en git)

- Este es el Baclos que es para  adelantar el frond 

https://github.com/orgs/FaceID-Proyect-2026/projects/1/views/1

-----------------------------------------------------------

- este es el backlod para  el backend
https://github.com/orgs/FaceID-Proyect-2026/projects/7


## Git (Movil y web)
- este es el repo de Fron ( ESTE ES PARA VER EL ABANSE QUE EMOS REALIZADO EN EL FORND CON DATOS QUEMAS ) AQUI SOLO SE VE ABANSES DEL FROND COMO TAL, PARA PODER EJECUTAR INGRESAR 

<img width="605" height="113" alt="image" src="https://github.com/user-attachments/assets/e9a9176e-20f8-4595-963e-e03b6c6db22f" />

Repo : 

https://github.com/FaceID-Proyect-2026/FaceLit/tree/dev

------------------------

- ESTE ES EL MISMO REPO DE FROND SOLO QUE CON DIFERENTE RAMA ( ESTE SI TIENE INTEGRADA LA CONECION CON EL BACKED Y ESTE SE EJECUTA DE LA SIGUIENTE FORMA

npx expo install expo@~54.0.37 expo-constants@~18.0.14
npx expo start -c
 https://github.com/FaceID-Proyect-2026/FaceLit/tree/feature/profile-integration

--------------------------------------------------
-   esta es la de la base de datos, de nuestro proyecto ( este ya esta en producion ( main ) y se ejecuta de la siguiente forma

docker compose -p facelit-docker-compose down --volumes --remove-orphans
docker compose -p facelit-docker-compose up -d postgres
docker compose -p facelit-docker-compose --profile tooling run --rm liquibase validate
docker compose -p facelit-docker-compose --profile tooling run --rm liquibase update

repo : 

https://github.com/FaceID-Proyect-2026/FaceLit-DB

----------------------------------

- este es el repo del Backend, en el cual esta en la rama  hotfix-03
como yo lo ejecuto 
<img width="101" height="53" alt="image" src="https://github.com/user-attachments/assets/ccc11604-4213-4db0-b642-b3bbac56ca59" />


y como  no esta el .env ya que nuestro gitnore lo inora ( no deja subir al repo  ) aqui esta ( para que funcione ) 

- este es el .env
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

- repo
https://github.com/FaceID-Proyect-2026/FaceLit-Backend/tree/hotfix-03


## Docs (Drive)

https://drive.google.com/drive/folders/12F8O-47Z7yD8U6IcIgIYGl62aKOA1aNf?usp=drive_link





