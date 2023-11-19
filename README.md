# quevi

# Proyecto de Desarrollo Full Stack: Registro de Películas

**Nombre de la App:** Que vi?

## Objetivos:

Desarrollar una aplicación web que permita a los usuarios gestionar un registro personalizado de películas vistas, facilitando la adición, búsqueda y clasificación de películas según la calificación de IMDb.

## Objetivos Adicionales:

1. **Mantenimiento del Registro:** Los usuarios podrán mantener un historial completo de todas las películas que han visto.
2. **Disponibilidad en Apple Store:** Desarrollar la aplicación para que sea compatible con la Apple Store y esté disponible en dispositivos iOS.

## Requisitos:

1. Permitir a los usuarios agregar películas a su lista de películas vistas.
2. Posibilitar a los usuarios buscar películas por título, actores, año de lanzamiento, lugar de realización o director.
3. Permitir ordenar las películas de mayor a menor calificación IMDb.

## Requisitos No Funcionales:

1. **Rendimiento:** La aplicación debe ser capaz de cargarse y funcionar de manera eficiente, incluso en situaciones de alta demanda.
2. **Seguridad:** Proteger los datos de los usuarios, incluyendo información como nombre de usuario, contraseña y calificaciones de películas. Además, implementar validación de datos de entrada para prevenir posibles vulnerabilidades.
3. **Accesibilidad:** Diseñar la aplicación de manera que sea accesible para todas las personas, incluyendo aquellas con discapacidades visuales que utilizan lectores de pantalla. Verificar la compatibilidad con diferentes navegadores para garantizar una experiencia consistente.

## Tecnologías Utilizadas:

**Frontend (React):**

- Redux Toolkit: Facilita la gestión del estado global de la aplicación.
- React Router: Para la navegación dentro de la aplicación.
- Axios: Para realizar solicitudes HTTP al backend de manera eficiente.
- Tailwind CSS: Un framework de diseño utilizable con React para una interfaz de usuario atractiva y responsiva.

**Backend (Node.js con Express):**

- Express.js: Framework para construir el servidor web y manejar las rutas.
- Mongoose: Facilita la interacción con MongoDB desde Node.js.
- Passport.js: Para la autenticación de usuarios.
- JWT (JSON Web Tokens): Para la gestión segura de tokens de autenticación.

**Base de Datos (MongoDB con Mongoose):**

- MongoDB Atlas: Ofrece una base de datos en la nube fácil de configurar y escalar.
- Mongoose: Para modelar y gestionar la conexión con la base de datos MongoDB.

## Librerías Adicionales:

**Pruebas:**

- Jest y Enzyme: Para pruebas unitarias y de componentes en React.
- Supertest: Para realizar pruebas de integración en el backend.
- Pruebas de extremo a extremo en el frontend para garantizar un funcionamiento correcto de la interfaz de usuario.

## Despliegue:

- Heroku o AWS: Plataformas de alojamiento que facilitan el despliegue de aplicaciones web.

## Seguridad:

- Helmet: Para mejorar la seguridad del servidor Express mediante la configuración de encabezados HTTP.
- Bcrypt: Para el hash seguro de contraseñas.

## Accesibilidad:

- React Aria: Para mejorar la accesibilidad en aplicaciones React.
- A11y (Accessibility) Checker Tools: Herramientas para verificar la accesibilidad de tu aplicación.
- Compatibilidad con diferentes navegadores para una experiencia consistente.

## Características Adicionales:

- **Modo Oscuro:** Implementar un modo oscuro en la interfaz de usuario para mejorar la experiencia visual en condiciones de baja luminosidad. Utilizar estilos y paletas de colores adecuadas para garantizar una transición suave entre el modo claro y oscuro.
- Redux Persist: Para persistir el estado de Redux en el almacenamiento local y mantener el historial de películas incluso después de cerrar la aplicación.
- React Native (para la versión iOS): Para la creación de la versión móvil de la aplicación compatible con la Apple Store.

## Características Técnicas:

- CDN para librerías comunes: Utiliza servicios como CDN para cargar librerías comunes, mejorando la velocidad de carga.
- SSL/TLS (HTTPS): Asegura la comunicación entre el cliente y el servidor.
- Lighthouse: Herramienta de Google para auditar el rendimiento, accesibilidad, buenas prácticas, SEO, etc.

## Desarrollo y Mantenimiento:

- Git y GitHub: Para el control de versiones y alojamiento del código fuente.
- Docker: Para la contenerización y facilitar el despliegue en diferentes entornos.

## Plan de Acción: Desarrollo de la Aplicación de Registro de Películas

### Etapa 1: Requisitos y Diseño

- **Objetivos:** Comprender los requisitos del proyecto y crear un documento de requisitos que los documente.
- **Actividades:**

  1. Investigar los requisitos de los usuarios.
  2. Desarrollar un documento de requisitos que especifique los requisitos funcionales y no funcionales del proyecto.

- **Calendario:** 2 semanas

### Etapa 2: Implementación

- **Objetivos:** Desarrollar la aplicación según el diseño.

- **Actividades:**

  1. Desarrollar el frontend de la aplicación utilizando React.
  2. Desarrollar el backend de la aplicación utilizando Node.js y Express.
  3. Implementar la base de datos MongoDB.
  4. Implementar las características adicionales, como el modo oscuro y la persistencia del estado.

- **Calendario:** 8 semanas

### Etapa 3: Pruebas

- **Objetivos:** Realizar pruebas exhaustivas de la aplicación para garantizar que funcione correctamente.

- **Actividades:**

  1. Desarrollar un plan de pruebas que especifique los casos de prueba.
  2. Implementar las pruebas unitarias y de integración.
  3. Realizar pruebas de extremo a extremo en el frontend.
  4. Ejecutar las pruebas y corregir cualquier error que se encuentre.

- **Calendario:** 2 semanas

### Etapa 4: Despliegue

- **Objetivos:** Desplegar la aplicación en un entorno de producción.

- **Actividades:**

  1. Elegir una plataforma de alojamiento.
  2. Configurar la aplicación para el despliegue.
  3. Desplegar la aplicación en producción.

- **Calendario:** 1 semana

### Etapa 5: Mantenimiento

- **Objetivos:** Mantener la aplicación actualizada y funcionando correctamente.

- **Actividades:**

  1. Monitorear el rendimiento de la aplicación.
  2. Implementar correcciones de errores y nuevas características.
  3. Realizar auditorías de seguridad periódicas.

- **Calendario:** Continuo
  Dependencias del Frontend (React)
  "dependencies": {
  "react": "^18.0.0",
  "react-dom": "^18.0.0",
  "react-redux": "^7.3.0",
  "react-router-dom": "^6.2.2",
  "axios": "^0.26.0",
  "tailwindcss": "^2.3.0"
  }

Dependencias del Backend (Node.js con Express)
"dependencies": {
"express": "^4.18.1",
"mongoose": "^6.2.15",
"passport": "^0.5.0",
"passport-jwt": "^4.5.0",
"bcrypt": "^5.0.2",
"dotenv": "^16.0.1",
"cors": "^2.8.5"
}

Dependencias de Pruebas (Frontend y Backend)
"devDependencies": {
"jest": "^28.0.3",
"enzyme": "^3.15.0",
"enzyme-to-json": "^3.10.0",
"supertest": "^6.4.0"
}

Herramientas de Desarrollo y Despliegue:
"devDependencies": {
"nodemon": "^2.0.16"
}

"dependencies": {
"heroku": "^7.60.3"
}

## Dependencias del Frontend (React)

Para instalar las dependencias del frontend, puedes utilizar los siguientes comandos:

npm install react@^18.0.0
npm install react-dom@^18.0.0
npm install react-redux@^7.3.0
npm install react-router-dom@^6.2.2
npm install axios@^0.26.0
npm install tailwindcss@^2.3.0

## Dependencias del Backend (Node.js con Express)

Para instalar las dependencias del backend, puedes utilizar los siguientes comandos:

npm install express@^4.18.1
npm install mongoose@^6.2.15
npm install passport@^0.5.0
npm install passport-jwt@^4.5.0
npm install bcrypt@^5.0.2
npm install dotenv@^16.0.1
npm install cors@^2.8.5

## Dependencias de Pruebas (Frontend y Backend)

Para instalar las dependencias de pruebas, puedes utilizar los siguientes comandos:

npm install jest@^28.0.3
npm install enzyme@^3.15.0
npm install enzyme-to-json@^3.10.0
npm install supertest@^6.4.0

## Herramientas de Desarrollo y Despliegue

Para instalar las herramientas de desarrollo y despliegue, puedes utilizar los siguientes comandos:

npm install nodemon@^2.0.16
npm install heroku@^7.60.3

**Proyecto Estructura**

|-- frontend/
| |-- public/
| |-- src/
| | |-- components/
| | | |-- Movie/
| | | | |-- MovieCard.jsx
| | | | |-- MovieList.jsx
| | | |-- Search/
| | | | |-- SearchBar.jsx
| | | |-- Auth/
| | | | |-- AuthForm.jsx
| | |-- pages/
| | | |-- Home/
| | | | |-- HomePage.jsx
| | | |-- Auth/
| | | | |-- LoginPage.jsx
| | | | |-- RegisterPage.jsx
| | | |-- User/
| | | | |-- UserProfilePage.jsx
| | |-- features/  
| | | |-- movies/
| | | | |-- moviesSlice.js
| | | |-- user/
| | | | |-- userSlice.js
| | |-- redux/
| | | |-- store.js  
| | |-- services/
| | | |-- api.jsx
| | |-- styles/
| | | |-- App.css
| | | |-- Movie/
| | | | |-- MovieCard.css
| | | | |-- MovieList.css
| | | |-- Search/
| | | | |-- SearchBar.css
| | | |-- Auth/
| | | | |-- AuthForm.css
| | |-- tailwind.css
| | |-- index.css
| | |-- index.jsx
| | |-- App.jsx
| | |-- tailwind.config.js
| |-- .gitignore
| |-- package.json
|-- backend/
| |-- controllers/
| | |-- MovieController.js
| | |-- UserController.js
| |-- routes/
| | |-- movieRoutes.js
| | |-- userRoutes.js
| |-- models/
| | |-- MovieModel.js
| | |-- UserModel.js
| |-- utils/
| | |-- hashPassword.js // Nuevo archivo para hashear contraseñas
| |-- .gitignore
| |-- package.json
| |-- server.js
|-- database/
| |-- scripts/
| |-- .gitignore
|-- tests/
| |-- backend/
| | |-- MovieController.test.js
| | |-- UserController.test.js
| |-- frontend/
| | |-- Movie/
| | | |-- MovieCard.test.js
| | | |-- MovieList.test.js
|-- .gitignore
|-- docker-compose.yml
|-- Dockerfile
|-- README.md
