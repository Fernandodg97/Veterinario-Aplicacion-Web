# Clinica Veterinaria

[![Java](https://img.shields.io/badge/Java_21-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring_Boot_3-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)](https://spring.io/projects/spring-boot)
[![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Couchbase](https://img.shields.io/badge/Couchbase-EA2328?style=for-the-badge&logo=couchbase&logoColor=white)](https://www.couchbase.com/)

---

## 👋 Para recruiters

Aplicacion web fullstack para la gestion de una clinica veterinaria: usuarios, mascotas y tratamientos. Backend desarrollado con **Java + Spring Boot** y frontend SPA con **React + TypeScript**, conectados a traves de una API REST.

**Stack:** Java 21 · Spring Boot 3.4 · React · TypeScript · Couchbase · Vite · Axios

**Destacado:**
- Arquitectura fullstack desacoplada: API REST en Spring Boot consumida por SPA en React
- Base de datos NoSQL documental con **Couchbase**, modelo de datos anidado (usuario > mascotas > tratamientos)
- **SPA con React Router** con navegacion fluida entre usuarios, mascotas y tratamientos
- **Dashboard** con contadores en tiempo real de usuarios, mascotas y tratamientos
- Diseño responsive con navegacion adaptada a distintos dispositivos

---

## 🛠️ Stack tecnologico

**Backend** Java 21 · Spring Boot 3.4.4 · Spring Data Couchbase · Spring Web · Maven

**Frontend** React · TypeScript · React Router DOM · Axios · Vite · CSS

**Base de datos** Couchbase Server (NoSQL documental)

---

## ✨ Funcionalidades

| Modulo | Descripcion |
|---|---|
| **Usuarios** | CRUD completo de propietarios de mascotas |
| **Mascotas** | Gestion de mascotas vinculadas a cada usuario |
| **Tratamientos** | Registro de tratamientos por mascota (medicamento, dosis, duracion) |
| **Dashboard** | Contadores globales y listados de actividad reciente |

---

## 📮 API REST

### Usuarios

| Metodo | Endpoint | Descripcion |
|---|---|---|
| POST | `/api/usuarios` | Crear un usuario |
| GET | `/api/usuarios` | Obtener todos los usuarios |
| GET | `/api/usuarios/{id}` | Obtener un usuario por ID |
| PUT | `/api/usuarios/{id}` | Editar un usuario |
| DELETE | `/api/usuarios/{id}` | Eliminar un usuario |

### Mascotas

| Metodo | Endpoint | Descripcion |
|---|---|---|
| POST | `/api/usuarios/{id}/mascotas` | Agregar mascota a un usuario |
| GET | `/api/usuarios/{id}/mascotas` | Obtener mascotas del usuario |
| PUT | `/api/usuarios/{usuarioId}/mascotas/{mascotaId}` | Editar una mascota |
| DELETE | `/api/usuarios/{id}/mascotas/{mascotaId}` | Eliminar una mascota |

### Tratamientos

| Metodo | Endpoint | Descripcion |
|---|---|---|
| POST | `/api/usuarios/{usuarioId}/mascotas/{mascotaId}/tratamientos` | Agregar tratamiento |
| GET | `/api/usuarios/{usuarioId}/mascotas/{mascotaId}/tratamientos` | Obtener tratamientos |
| DELETE | `/api/usuarios/{usuarioId}/mascotas/{mascotaId}/tratamientos/{tratamientoId}` | Eliminar tratamiento |

---

## 🌐 Rutas del frontend

| Ruta | Descripcion |
|---|---|
| `/` | Dashboard principal |
| `/users` | Lista de usuarios |
| `/users/new` | Crear usuario |
| `/users/edit/:id` | Editar usuario |
| `/pets` | Lista de mascotas |
| `/users/:userId/pets` | Mascotas de un usuario |
| `/treatments` | Lista de tratamientos |
| `/pets/:petId/treatments` | Tratamientos de una mascota |

---

## 🚀 Instalacion y puesta en marcha

### Prerrequisitos

- Java 21 y Maven
- Node.js v14+
- Couchbase Server con bucket `veterinario` creado

### Backend

```bash
cd backend
mvn spring-boot:run
```

Disponible en `http://localhost:4040`

### Frontend

```bash
cd frontend
npm install
npm run dev
```

Disponible en `http://localhost:5173`

### Configuracion de Couchbase

```properties
spring.couchbase.connection-string=localhost
spring.couchbase.bucket.name=veterinario
spring.couchbase.username=usuario
spring.couchbase.password=usuario
```

---

## 📚 Documentacion

| Archivo | Descripcion |
|---|---|
| [`Presentacion_Comunidad.pdf`](./Presentacion_Comunidad.pdf) | Presentacion del proyecto |

---

## 👨‍💻 Autor

| | |
|---|---|
| **Fernando Diaz** | [github.com/Fernandodg97](https://github.com/Fernandodg97) |

---

## 📄 Licencia

[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es)
