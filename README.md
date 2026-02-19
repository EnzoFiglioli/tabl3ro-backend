# Tabl3ro

**Tabl3ro** es una aplicación de microblogging inspirada en Twitter que permite a los usuarios publicar mensajes cortos, seguir a otros usuarios y visualizar un feed personalizado con contenido actualizado dinámicamente.

El objetivo del proyecto fue construir una aplicación full-stack aplicando buenas prácticas de arquitectura REST, autenticación stateless con JWT y modelado relacional con Sequelize sobre MySQL.

---

## 🚀 Demo

👉 [https://tabl3ro.vercel.app/](https://tabl3ro.vercel.app/)

---

## 🧱 Stack Tecnológico

### Frontend

* React
* Tailwind CSS
* Axios
* React Router

### Backend

* Node.js
* Express
* Sequelize (ORM)
* JWT (JSON Web Tokens)
* Bcrypt (hash de contraseñas)
* Nodemailer

### Base de Datos

* MySQL

---

## 🏗 Arquitectura

La aplicación sigue una arquitectura cliente-servidor:

Frontend (React)
⬇
API REST (Express)
⬇
Base de datos relacional (MySQL)

* El frontend consume la API mediante Axios.
* El backend implementa controladores, middlewares y modelos Sequelize.
* La autenticación es stateless mediante JWT.
* Las relaciones entre entidades están normalizadas en MySQL.

---

## 🔐 Autenticación y Seguridad

* Registro de usuarios
* Login con generación de token JWT
* Middleware de verificación de token
* Hash de contraseñas con bcrypt
* Protección de rutas privadas
* Variables sensibles gestionadas con `.env`

---

## ✨ Funcionalidades

* Crear publicaciones
* Visualizar feed personalizado
* Seguir y dejar de seguir usuarios
* Perfil de usuario
* Notificaciones por correo electrónico
* Persistencia de sesión mediante token

---

## 📊 Modelo de Datos (Simplificado)

### Entidades principales:

* **User**
* **Post**
* **Follow**

### Relaciones:

* Un usuario puede tener múltiples publicaciones (1:N).
* Un usuario puede seguir a múltiples usuarios (N:M).
* La relación N:M se resuelve mediante una tabla intermedia `Follows`.

---

## 🛠 Instalación Local

### Requisitos

* Node.js v18+
* MySQL 8+

---

### 1. Clonar el repositorio

```bash
git clone https://github.com/EnzoFiglioli/tablero-webapp.git
cd tablero-webapp
```

---

### 2. Instalar dependencias

```bash
npm install
```

---

### 3. Configurar variables de entorno

Crear un archivo `.env` en la raíz del proyecto:

```
DB_HOST=localhost
DB_USER=root
DB_PASS=tu_password
DB_NAME=tabl3ro
JWT_SECRET=clave_super_secreta
EMAIL_USER=tu_email
EMAIL_PASS=tu_password_email
```

---

### 4. Ejecutar el servidor

```bash
npm run dev
```
