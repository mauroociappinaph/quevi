# Proyecto de Desarrollo Full Stack: Registro de Películas

## Paso 1: Configuración de la Base de Datos

### 1.1 Base de Datos MongoDB

1. Accede a [MongoDB Atlas](https://www.mongodb.com/cloud/atlas) e inicia sesión o crea una nueva cuenta si aún no la tienes.
2. En el panel de control, haz clic en "Build a Cluster" para configurar tu clúster de base de datos.
3. Selecciona un proveedor de nube y una región para alojar tu clúster (AWS, Google Cloud, o Azure).
4. Configura las opciones adicionales según tus necesidades.
5. Haz clic en "Create Cluster" para iniciar la creación del clúster. Este proceso puede llevar algún tiempo.
6. Mientras se crea el clúster, en el panel lateral, selecciona la pestaña "Database Access". Aquí crearás un usuario para acceder a tu base de datos.
7. Haz clic en "Add a Database User" y proporciona un nombre de usuario y una contraseña segura. Asegúrate de recordar estos detalles, ya que los necesitarás para conectarte a la base de datos desde tu aplicación.
8. Volviendo al panel lateral, selecciona la pestaña "Network Access". Aquí, añadirás la dirección IP desde la cual te conectarás a la base de datos.
9. Haz clic en "Add IP Address" y elige "Allow Access from Anywhere" por simplicidad. En un entorno de producción, sería recomendable limitar el acceso a direcciones IP específicas.
10. Una vez que se complete la creación del clúster, vuelve a la pestaña "Clusters" y selecciona tu clúster recién creado.
11. En el clúster, haz clic en el botón "Connect" y elige "Connect your application". Esto te proporcionará la cadena de conexión URI que necesitas para conectarte desde tu aplicación.
12. Copia la cadena de conexión y guárdala de forma segura. Contendrá la información necesaria para que tu aplicación se conecte a la base de datos MongoDB Atlas.

## Paso 2: Desarrollo del Backend (Node.js con Express)

### 2.1 Configuración Inicial

### 1. **Crear la Estructura del Proyecto:**

- Antes de comenzar, asegúrate de tener Node.js instalado en tu máquina. Puedes descargarlo desde [nodejs.org](https://nodejs.org/).

- Abre tu terminal y ejecuta los siguientes comandos:

  ```bash
  # 📁 Crea una nueva carpeta para el backend
  mkdir backend

  # 📂 Ingresa a la carpeta del backend
  cd backend

  # 🚀 Inicializa tu proyecto Node.js
  npm init -y
  ```

- Este comando generará un archivo `package.json` con la configuración predeterminada. Asegúrate de revisar y modificar este archivo según sea necesario.

- Ahora, puedes continuar instalando las dependencias necesarias para tu proyecto. Ejecuta el siguiente comando:

  ```bash
  # ⚙️ Instala las dependencias necesarias
  npm install express@^4.18.1 mongoose@^6.2.15 passport@^0.5.0 passport-jwt@^4.5.0 bcrypt@^5.0.2 dotenv@^16.0.1 cors@^2.8.5
  ```

- Estas dependencias son fundamentales para el desarrollo del backend, proporcionando herramientas como Express para el manejo de rutas, Mongoose para interactuar con MongoDB, Passport para la autenticación, y otras utilidades.

- Con esto, has configurado la estructura básica del proyecto backend y has instalado las dependencias necesarias.

2. **Instalar Dependencias del Backend:**
   - Instala las dependencias necesarias:
     ```bash
     npm install express@^4.18.1 mongoose@^6.2.15 passport@^0.5.0 passport-jwt@^4.5.0 bcrypt@^5.0.2 dotenv@^16.0.1 cors@^2.8.5
     ```

### 2.2 Estructura de Carpetas y Archivos

<details>
  <summary><strong style="color:#3498db;">3. Crear Estructura del Proyecto:</strong></summary>

- 📁 Crea la siguiente estructura de carpetas y archivos en la carpeta del backend:

  ```
  /backend
  ├── 📁 /controllers
  │   ├── 📄 MovieController.js
  │   ├── 📄 UserController.js
  ├── 📁 /routes
  │   ├── 📄 movieRoutes.js
  │   ├── 📄 userRoutes.js
  ├── 📁 /models
  │   ├── 📄 MovieModel.js
  │   ├── 📄 UserModel.js
  ├── 📁 /utils
  │   ├── 📄 hashPassword.js
  ├── 📄 .gitignore
  ├── 📄 package.json
  ├── 📄 server.js
  ```

- Esta estructura proporciona una organización clara para tu proyecto backend. Los controladores manejan la lógica, las rutas gestionan las solicitudes HTTP, los modelos definen la estructura de la base de datos, y los archivos de utilidad contienen funciones reutilizables.

- El archivo `.gitignore` asegura que ciertos archivos y carpetas no se incluyan en el control de versiones. `package.json` contiene la configuración del proyecto, y `server.js` es el punto de entrada de tu aplicación.

</details>

### 2.3 Modelos y Base de Datos

<details>
  <summary><strong style="color:#3498db;">4. Definir Modelos y Conexión con MongoDB:</strong></summary>

- **Paso 1: Definir Modelo de Película (`MovieModel.js`):**

  - Crea el archivo `MovieModel.js` en la carpeta `/models` del backend.
  - Define la estructura del modelo utilizando Mongoose para representar los datos de las películas.

- **Paso 2: Definir Modelo de Usuario (`UserModel.js`):**

  - Crea el archivo `UserModel.js` en la carpeta `/models` del backend.
  - Define la estructura del modelo utilizando Mongoose para representar los datos de los usuarios.

- **Paso 3: Conectar el Backend a MongoDB:**

  - Abre el archivo `server.js` en la raíz del backend.
  - Utiliza la conexión URI obtenida en la configuración de la base de datos para conectar el backend a MongoDB.

- Con estos pasos, has definido los modelos de datos para películas y usuarios, y has establecido la conexión del backend con la base de datos MongoDB.

</details>

### 2.4 Controladores y Rutas

5. **Implementar Controladores y Rutas:**
   - Implementa controladores (`MovieController.js` y `UserController.js`) para manejar la lógica de películas y usuarios.
   - Define rutas en `movieRoutes.js` y `userRoutes.js` para gestionar las solicitudes HTTP.

### 2.5 Autenticación y Seguridad

6. **Implementar Autenticación y Seguridad:**
   - Implementa la autenticación de usuarios con Passport.js y JWT.
   - Mejora la seguridad del servidor Express utilizando Helmet.
   - Implementa el hash seguro de contraseñas con Bcrypt.

### 2.6 Pruebas

7. **Realizar Pruebas Unitarias e Integración:**
   - Implementa pruebas unitarias y de integración con Jest, Enzyme y Supertest.
   - Asegúrate de que las pruebas sean exhaustivas y corrige cualquier error encontrado.

### 2.7 Conexión con la Base de Datos

8. **Conectar el Backend con la Base de Datos:**
   - Conecta el backend con la base de datos MongoDB.
   - Configura CORS para manejar las solicitudes del frontend.

### 2.8 Flujo de la Aplicación

9. **Definir Flujo Básico de la Aplicación:**
   - Define el flujo básico de la aplicación desde la solicitud hasta la respuesta, considerando la autenticación y autorización cuando sea necesario.

## Paso 3: Desarrollo del Frontend (React)

### 3.1 Configuración Inicial

10. **Crear la Estructura del Proyecto de React:**

- Crea un nuevo proyecto de React en la carpeta frontend.
- Dentro, ejecuta `npm init -y` para inicializar tu proyecto React.

11. **Instalar Dependencias del Frontend:**

- Instala las dependencias necesarias:
  ```bash
  npm install react@^18.0.0 react-dom@^18.0.0 react-redux@^7.3.0 react-router-dom@^6.2.2 axios@^0.26.0 tailwindcss@^2.3.0
  ```

### 3.2 Estructura de Carpetas y Archivos

12. **Crear Estructura del Proyecto de React:**

- Crea la siguiente estructura de carpetas y archivos en la carpeta del frontend:
  ```
  /frontend
  ├── /public
  ├── /src
  │   ├── /components
  │   │   ├── /Movie
  │   │   │   ├── MovieCard.jsx
  │   │   │   ├── MovieList.jsx
  │   │   ├── /Search
  │   │   │   ├── SearchBar.jsx
  │   │   ├── /Auth
  │   │   │   ├── AuthForm.jsx
  │   ├── /pages
  │   │   ├── /Home
  │   │   │   ├── HomePage.jsx
  │   │   ├── /Auth
  │   │   │   ├── LoginPage.jsx
  │   │   │   ├── RegisterPage.jsx
  │   │   ├── /User
  │   │   │   ├── UserProfilePage.jsx
  │   ├── /features
  │   │   ├── /movies
  │   │   │   ├── moviesSlice.js
  │   │   ├── /user
  │   │   │   ├── userSlice.js
  │   ├── /redux
  │   │   ├── store.js
  │   ├── /services
  │   │   ├── api.jsx
  │   ├── /styles
  │   │   ├── App.css
  │   │   ├── /Movie
  │   │   │   ├── MovieCard.css
  ```

### 3.3 Desarrollo de Componentes

13. **Desarrollar Componentes:**

- Desarrolla los componentes según la estructura mencionada.
- Implementa la lógica para agregar películas, buscar, etc.

### 3.4 Configuración de Redux y React Router

14. **Configurar Redux y React Router:**

- Configura Redux Toolkit para gestionar el estado global.
- Define slices para manejar el estado de películas y usuarios.
- Configura React Router para manejar la navegación entre páginas.

### 3.5 Estilos y Diseño

15. **Aplicar Estilos y Diseño:**

- Utiliza Tailwind CSS para dar estilo a los componentes.
- Implementa el modo oscuro y asegúrate de que la interfaz sea atractiva.

### 3.6 Integración con el Backend

16. **Integración con el Backend:**

- Implementa servicios para realizar solicitudes HTTP al backend.

### 3.7 Pruebas y Correcciones

17. **Realizar Pruebas Exhaustivas:**

- Realiza pruebas exhaustivas en el frontend.
- Ejecuta las pruebas y corrige cualquier error encontrado.

## Paso 4: Integración Frontend y Backend

### 4.1 Conexión Frontend y Backend

- Conecta el frontend y el backend para que se comuniquen adecuadamente.

## Paso 5: Despliegue

### 5.1 Elección de Plataforma de Alojamiento

- Decide entre Heroku o AWS para el despliegue.

### 5.2 Configuración de Despliegue

- Configura la aplicación para el despliegue en la plataforma elegida.

### 5.3 Despliegue en Producción

- Despliega la aplicación en producción.

## Paso 6: Mantenimiento Continuo

### 6.1 Monitoreo y Correcciones

- Monitorea el rendimiento de la aplicación.

- Implementa correcciones de errores y nuevas características.

- Realiza auditorías de seguridad periódicas.

## Paso 7: Documentación y Comentarios

### 7.1 Documentación del Código

- Documenta tu código, especialmente si planeas compartirlo.

### 7.2 Comentarios en el Código

- Agrega comentarios en partes críticas o complejas del código.

## Paso 8: Pruebas Finales y Lanzamiento

### 8.1 Pruebas Finales

- Realiza pruebas finales para garantizar que la aplicación funcione correctamente.

### 8.2 Lanzamiento

- Anuncia y lanza tu aplicación.
