# RealFilms – Gestor de Portafolio de Proyectos Freelance  

<div align="center">
  <h3>Plataforma Geek de Películas, Series y Animes</h3>
  <p>Aplicación Full-Stack para registrar, calificar y rankear contenido geek</p>
</div>

---
<div align="center">
## Introducción  

**RealFilms** (nombre inicial *KarenFlix*) es una aplicación **full-stack** que permite a los usuarios:  
- Registrar y explorar películas, animes y series.  
- Crear reseñas con calificaciones y reacciones (likes/dislikes).  
- Visualizar rankings ponderados en base a popularidad y notas.  
- Administrar contenido y usuarios según roles.  

El proyecto está dividido en:  
- **Backend** → Node.js + Express + MongoDB.  
- **Frontend** → HTML, CSS y JavaScript puro.  

Incluye autenticación con JWT, validaciones robustas, manejo transaccional en MongoDB y documentación de API con Swagger.

El objetivo de este proyecto es desarrollar una aplicación **full-stack** usando **Node.js + Express** para el backend y **HTML + CSS puro** para el frontend, que permita a los usuarios registrar, calificar y rankear películas, animes y series geek. Esta herramienta debe incluir funcionalidades para gestionar usuarios, reseñas, categorías y rankings, diferenciando permisos de usuario y administrador. Además, debe contar con autenticación segura, validaciones robustas y un frontend que consuma la API desarrollada.


---

## Objetivos  

- Implementar un sistema de gestión de usuarios con autenticación segura.  
- Permitir a los usuarios crear reseñas, calificar y reaccionar (likes/dislikes).  
- Gestionar películas y categorías con control de administrador.  
- Calcular un ranking ponderado de películas basado en calificaciones, popularidad y reacciones.  
- Desarrollar un frontend amigable, conectado al backend mediante API REST.  

---

## Tecnologías usadas  

### Backend  
- Node.js + Express  
- MongoDB (driver oficial)  
- JWT (autenticación)  
- bcrypt (hashing)  
- dotenv (configuración de entorno)  
- express-rate-limit (seguridad)  
- express-validator (validaciones)  
- passport-jwt (roles y auth)  
- swagger-ui-express (documentación API)  
- semver (versionado)  

### Frontend  
- HTML5  
- CSS3  
- JavaScript puro  

### Gestión del proyecto  
- GitHub (repositorio y control de versiones)  
- SCRUM (metodología ágil)  

---

## Estructura del proyecto  

```bash
.
├── html
│   ├── createAccount.html
│   ├── inicioAdmin.html
│   ├── inicioUser.html
│   └── usuariosAdmin.html
├── script
│   ├── createAccount.js
│   ├── inicioAdmin.js
│   ├── inicioUser.js
│   ├── login.js
│   └── usuarios.js
├── storage
│   ├── font/
│   └── img/
├── styles
│   ├── index.css
│   ├── inicioAdmin.css
│   └── inicioUser.css
└── index.html
```

## Repositorio de BackEnd 
https://github.com/Danny200523/Proyecto_Express_BackEnd_GuerreroDaniel_AbrilJuan.git


# Endpoints principales
Usuarios
POST /api/v1/auth/register → Registrar usuario
POST /api/v1/auth/login → Iniciar sesión
GET /api/v1/usuarios → Listar usuarios (admin)
Películas
POST /api/v1/peliculas → Crear película (admin)
GET /api/v1/peliculas → Listar todas las películas
GET /api/v1/peliculas/:id → Ver detalle de una película
Reseñas
POST /api/v1/reseñas → Crear reseña


##  Endpoints Principales
Autenticación

POST /api/auth/register → Registro de usuario.

POST /api/auth/login → Inicio de sesión.

Películas / Series / Animes

GET /api/movies → Listar contenido.

POST /api/movies → Crear nuevo (admin).

GET /api/movies/:id → Detalle de película.

PUT /api/movies/:id → Actualizar.

DELETE /api/movies/:id → Eliminar (admin).

Reseñas

POST /api/reviews → Crear reseña.

GET /api/reviews/:movieId → Listar reseñas de una película.

Documentación completa en Swagger: http://62.169.28.169/docs

GET /api/v1/reseñas/:id_pelicula → Listar reseñas de una película
PUT /api/v1/reseñas/:id → Editar reseña
DELETE /api/v1/reseñas/:id → Eliminar reseña
Reacciones
POST /api/v1/reacciones → Dar like/dislike
GET /api/v1/reacciones/:id_pelicula → Obtener reacciones de película
