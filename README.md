# 🐾 Clínica Veterinaria - Proyecto Completo

Este proyecto consiste en una aplicación completa para la gestión de una clínica veterinaria, dividida en dos partes: backend y frontend.

## 📦 Tecnologías Utilizadas

### Backend
- Java 21
- Spring Boot 3.4.4
- Spring Data Couchbase
- Spring Web
- Maven (WAR packaging)
- Couchbase Server
- Tomcat (servidor embebido)

### Frontend
- React 
- TypeScript
- React Router DOM
- Axios
- CSS

## 🚀 Características Principales

- Gestión completa de usuarios (propietarios de mascotas)
- Administración de mascotas asociadas a usuarios
- Registro y seguimiento de tratamientos médicos
- Interfaz intuitiva con diseño responsive
- Navegación fluida entre secciones relacionadas

## 🔧 Configuración del Entorno

### Requisitos Previos
- Node.js (v14 o superior)
- npm o yarn
- Java 21
- Couchbase Server

### Backend

#### Couchbase
Asegúrate de tener Couchbase Server corriendo en `localhost` y con el bucket `veterinario` creado. Usuario y contraseña deben ser `usuario`.

#### Configuración
```properties
spring.application.name=veterinario
server.port=4040

# Configuración de Couchbase
spring.mvc.pathmatch.matching-strategy=ANT_PATH_MATCHER
spring.couchbase.connection-string=localhost
spring.couchbase.bucket.name=veterinario
spring.couchbase.username=usuario
spring.couchbase.password=usuario
```

### Frontend

#### Instalación
```bash
# Clonar el repositorio
git clone https://github.com/tu-usuario/clinica-veterinaria-frontend.git

# Entrar al directorio
cd clinica-veterinaria-frontend

# Instalar dependencias
npm install
# o
yarn install

# Iniciar la aplicación en modo desarrollo
npm start
# o
yarn start
```

## 📁 Estructura del Proyecto

### Backend
```
net.xeill.elpuig.veterinario
├── configs
│   ├── CouchbaseConfig.java
│   └── CorsConfig.java
├── controllers
│   ├── UsuarioController.java
│   └── MascotaController.java
├── models
│   ├── Usuario.java
│   ├── Mascota.java
│   └── Tratamiento.java
├── repositories
│   └── UsuarioRepository.java
└── services
    └── UsuarioService.java
```

### Frontend
```
frontend/
├── src/
│   ├── components/
│   │   ├── common/
│   │   │   └── ConfirmDialog.tsx
│   │   ├── users/
│   │   │   ├── UserList.tsx
│   │   │   └── UserForm.tsx
│   │   ├── pets/
│   │   │   ├── PetList.tsx
│   │   │   └── PetForm.tsx
│   │   ├── treatments/
│   │   │   ├── TreatmentList.tsx
│   │   │   └── TreatmentForm.tsx
│   │   └── Dashboard.tsx
│   ├── services/
│   │   ├── api.tsx
│   │   └── apiController.tsx
│   ├── types/
│   │   └── index.tsx
│   ├── App.tsx
│   └── index.tsx
└── public/
```

## 📮 API REST

### Usuarios
| Método | Endpoint                     | Descripción                       |
|--------|------------------------------|-----------------------------------|
| POST   | `/api/usuarios`              | Crear un usuario                  |
| GET    | `/api/usuarios`              | Obtener todos los usuarios        |
| GET    | `/api/usuarios/{id}`         | Obtener un usuario por ID         |
| GET    | `/api/usuarios/{email}`      | Obtener un usuario por email      |
| PUT    | `/api/usuarios/{id}`         | Editar un usuario por ID          |
| DELETE | `/api/usuarios/{id}`         | Eliminar un usuario               |

### Mascotas
| Método | Endpoint                                               | Descripción                              |
|--------|--------------------------------------------------------|------------------------------------------|
| POST   | `/api/usuarios/{id}/mascotas`                          | Agregar mascota a un usuario             |
| GET    | `/api/usuarios/{id}/mascotas`                          | Obtener todas las mascotas del usuario   |
| PUT    | `/api/usuarios/{usuarioId}/mascotas/{mascotaId}`      | Editar una mascota                       |
| DELETE | `/api/usuarios/{id}/mascotas/{mascotaId}`             | Eliminar una mascota                     |

### Tratamientos
| Método | Endpoint                                                                           | Descripción                                |
|--------|------------------------------------------------------------------------------------|--------------------------------------------|
| POST   | `/api/usuarios/{usuarioId}/mascotas/{mascotaId}/tratamientos`                     | Agregar tratamiento a una mascota          |
| GET    | `/api/usuarios/{usuarioId}/mascotas/{mascotaId}/tratamientos`                     | Obtener todos los tratamientos de mascota  |
| DELETE | `/api/usuarios/{usuarioId}/mascotas/{mascotaId}/tratamientos/{tratamientoId}`     | Eliminar tratamiento                       |

## 🌐 Rutas de la Aplicación Frontend

- `/` - Dashboard principal
- `/users` - Lista de usuarios
- `/users/new` - Formulario para crear usuario
- `/users/edit/:id` - Formulario para editar usuario
- `/pets` - Lista de todas las mascotas
- `/pets/new` - Formulario para crear mascota
- `/pets/edit/:id` - Formulario para editar mascota
- `/users/:userId/pets` - Mascotas de un usuario específico
- `/users/:userId/pets/new` - Crear mascota para un usuario específico
- `/treatments` - Lista de todos los tratamientos
- `/treatments/new` - Formulario para crear tratamiento
- `/pets/:petId/treatments` - Tratamientos de una mascota específica
- `/pets/:petId/treatments/new` - Crear tratamiento para una mascota específica

## 📊 Dashboard

La aplicación incluye un dashboard que muestra:
- Número total de usuarios registrados
- Número total de mascotas
- Número total de tratamientos
- Usuarios y mascotas añadidos recientemente

## 👨‍💻 Autores
- [@Fernandodg97](https://github.com/Fernandodg97)
- [@Msedjari10](https://github.com/Msedjari10)

## 📄 Licencia

[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.es) 