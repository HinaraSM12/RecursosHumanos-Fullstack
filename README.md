# Recursos Humanos - Fullstack

## Descripción

Este proyecto es una aplicación de gestión de empleados desarrollada con una arquitectura full-stack utilizando Spring Boot para el backend y MySQL como base de datos. El objetivo principal de esta aplicación es proporcionar una interfaz sencilla y eficiente para administrar empleados dentro de una organización, permitiendo operaciones CRUD (Crear, Leer, Actualizar, Eliminar) sobre los datos de los empleados.

## Tecnologías Utilizadas

### Backend
- **Java 21**
- **Spring Boot**
- **Spring Data JPA**
- **Hibernate**
- **MySQL**
- **SLF4J** (para logging)
- **Tomcat** (servidor embebido)

### Frontend
- **React** (puerto 3000)
- **HTML**
- **CSS**
- **JavaScript**

## Estructura del Proyecto

### Backend
La estructura del backend sigue el modelo típico de capas:
- **Controladores**: Manejan las solicitudes HTTP y las respuestas.
- **Servicios**: Contienen la lógica de negocio.
- **Repositorios**: Interactúan con la base de datos.

### Frontend
El frontend está diseñado para interactuar con la API del backend a través de solicitudes HTTP y proporcionar una interfaz de usuario amigable.

## Endpoints

### Empleados

- **Obtener todos los empleados**
  - **URL**: `/rh-app/empleados`
  - **Método**: GET
  - **Descripción**: Devuelve una lista de todos los empleados.
  
- **Agregar un nuevo empleado**
  - **URL**: `/rh-app/empleados`
  - **Método**: POST
  - **Descripción**: Agrega un nuevo empleado.
  - **Cuerpo de la Solicitud**: JSON con los detalles del empleado.

- **Obtener empleado por ID**
  - **URL**: `/rh-app/empleados/{id}`
  - **Método**: GET
  - **Descripción**: Devuelve los detalles de un empleado específico por ID.

- **Actualizar un empleado**
  - **URL**: `/rh-app/empleados/{id}`
  - **Método**: PUT
  - **Descripción**: Actualiza la información de un empleado existente.
  - **Cuerpo de la Solicitud**: JSON con los nuevos detalles del empleado.

- **Eliminar un empleado**
  - **URL**: `/rh-app/empleados/{id}`
  - **Método**: DELETE
  - **Descripción**: Elimina un empleado por ID.
  - **Respuesta**: JSON con confirmación de eliminación.

## Instalación y Ejecución

### Prerrequisitos

- **Java 21**
- **Maven**
- **MySQL**

### Configuración de la Base de Datos

1. Crear una base de datos en MySQL:
   ```sql
   CREATE DATABASE recursos_humanos;
   ```

2. Configurar las credenciales de la base de datos en `application.properties`:
   ```properties
   spring.datasource.url=jdbc:mysql://localhost:3306/recursos_humanos
   spring.datasource.username=tu_usuario
   spring.datasource.password=tu_contraseña
   spring.jpa.hibernate.ddl-auto=update
   ```

### Construir y Ejecutar el Proyecto

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/HinaraSM12/RecursosHumanos-Fullstack.git
   cd recursos-humanos-spring
   ```

2. Construir el proyecto con Maven:
   ```bash
   mvn clean install
   ```

3. Ejecutar la aplicación:
   ```bash
   mvn run
   ```

4. El servidor estará corriendo en `http://localhost:8080`.

### Frontend

1. Navegar al directorio del frontend:
   ```bash
   cd recursos-humanos-app
   ```

2. Instalar dependencias:
   ```bash
   npm install
   ```

3. Ejecutar la aplicación de React:
   ```bash
   npm start
   ```

4. La aplicación frontend estará corriendo en `http://localhost:3000`.

## Contribuir

Si deseas contribuir al proyecto, por favor sigue los siguientes pasos:

1. Haz un fork del repositorio.
2. Crea una nueva rama (`git checkout -b feature/nueva-funcionalidad`).
3. Realiza tus cambios y haz commits (`git commit -am 'Añadir nueva funcionalidad'`).
4. Haz push a la rama (`git push origin feature/nueva-funcionalidad`).
5. Abre un Pull Request.

## Contacto

Para más información, puedes contactarme en [hinarasm01212@gmail.com](mailto:hinarasm01212@gmail.com).

## Licencia

Este proyecto está licenciado bajo la Licencia MIT. Consulta el archivo `LICENSE` para más detalles.