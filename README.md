![# The Original Kingdom](./logoLetters.png)

## 🏰 Descripción general del proyecto:

"The Original Kingdom" es un juego de simulación de toma de decisiones en el que los jugadores asumen el papel de un rey medieval. El objetivo del juego es tomar decisiones estratégicas para mantener el equilibrio y la prosperidad en el reino durante el mayor tiempo posible.

# Video explicación del proyecto
[![Video explicatorio](https://img.youtube.com/vi/D_qBSxVPbq0/0.jpg)](https://www.youtube.com/watch?v=D_qBSxVPbq0)

# Árbol de decisiones
![Árbol de decisiones](./ArbolDeDecisiones.png)


## 📂 Arquitectura y estructura del proyecto:

El proyecto se divide en dos partes principales:

### 🤖 Backend:
- Se encarga de manejar los controladores, las rutas de las peticiones y los esquemas de los modelos de datos.
- Utiliza Node.js con Express para gestionar las rutas y las solicitudes HTTP.

### 🙍‍♂️ Frontend:
- Utiliza Node.js con React para la creación del frontend del juego.
- El directorio "public" almacena el archivo index.html y otros recursos como imágenes y videos.
- Se hace uso de los estados de React (UseState) para el manejo de la lógica del juego.

Protopito de frontend: [FIGMA](https://www.figma.com/community/file/1382300407944413432/the-original-kingdom-figma)


## ⚙ Funcionalidades principales:

El juego incluye las siguientes características principales:
- Sistema de registro e inicio de sesión utilizando **hash** para almacenar de forma segura las contraseñas de los usuarios.
- Sistema de manejo de volumen para controlar el sonido del juego.
- Toma de decisiones estratégicas que afectan a diferentes facciones del reino, como la economía, la protección, la población, etc.
- Sistema de puntos en el cual se actualizara el *maxscore* en la base de datos si el usuario supero su mayor puntuacion.

## 📚 Documentación técnica:

El proyecto fue desarrollado utilizando las siguientes tecnologías:
- Backend: Node.js con Express para el servidor, MongoDB Atlas como base de datos.
- Frontend: React para la interfaz de usuario.
- HTML, JavaScript para el desarrollo web.
- Se utiliza la función UseState de React para el manejo de estados en el frontend.

## 🌐 Endpoints de la API:

Se proporcionan las siguientes rutas de API para las peticiones al backend:

Aqui la colecion **YAML**: [SWAGGER](https://app.swaggerhub.com/apis/DVAZALM/The-Original-Kingdom/1.0.0-oas3)

Aqui la coleccion en **PostMan**: [PostMan](https://drive.google.com/file/d/1SKR8so5Dn2SXcmQN9iy9gaZ8wq_jgGWg/view?usp=sharing)


### 👥 Usuarios:
- POST /api/user/register -> Registro de nuevos usuarios.
- GET /api/user/data/:email -> Obtener datos de un usuario específico.
- PATCH /api/user/update/:email -> Actualizar datos de un usuario.
- DELETE /api/user/delete/:email -> Eliminar un usuario.

### ⚖ Decisiones:
- POST /api/decision/create -> Crear una nueva decisión.
- GET /api/decision/randomDecision -> Obtener una decisión aleatoria.
- GET /api/decision/data -> Obtener detalles de una ID específica.

## 📑 Instrucciones de instalación, configuración e instrucciones de uso:

Para instalar y ejecutar el proyecto:

Primero debemos ir al backend con `cd backend`, a continuación:

    1. Ejecutar `npm install` para instalar las dependencias.

    2. Crea un archivo llamado `.env` y rellena en el la plantilal que se encuantra en ".env-Template"

    3. Lanzar el proyecto:
    - Opción 1: Ejecutar `docker-compose up` para utilizar Docker.
    - Opción 2: Ejecutar `npm start`.

    4. Asegurarse de que el backend se inicie primero para ocupar el puerto 3000.

Despues debemos abrir una nueva terminal e ir al frontend con `cd frontend`, a continuación:

    1. Ejecutar `npm install` para instalar las dependencias.

    2. Lanzar el proyecto ejecutando `npm start`.

    3. Asegurarse de que el frontend se inicia en un puerto diferente al del backend.
