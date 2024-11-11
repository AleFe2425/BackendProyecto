# Proyecto de Gestión de Producción de Muebles

Este proyecto es un sistema de gestión de producción de muebles desarrollado con un backend en Java y un frontend en Svelte.

## Tabla de Contenidos

1. [Características](#características)
2. [Tecnologías Utilizadas](#tecnologías-utilizadas)
3. [Requisitos Previos](#requisitos-previos)
4. [Instalación](#instalación)
5. [Configuración](#configuración)
6. [Ejecución](#ejecución)
7. [Endpoints del Backend](#endpoints-del-backend)
8. [Frontend](#frontend)
9. [Despliegue](#despliegue)
10. [Contribuciones](#contribuciones)
11. [Licencia](#licencia)

---

### Características

- Gestión de clientes, pedidos, materiales, muebles y empleados.
- Control de producción y estimación de tiempos de fabricación en función de los materiales.
- Autenticación de administrador y permisos de acceso.

### Tecnologías Utilizadas

- **Backend**: Java (Spring Boot)
- **Frontend**: Svelte
- **Base de Datos**: MySQL
- **Despliegue**: Railway para el backend y Vercel para el frontend

### Requisitos Previos

- Node.js y npm instalados
- Java Development Kit (JDK) versión 11 o superior
- MySQL
- Git

### Instalación

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tuusuario/BackendProyecto.git
2. Navega a la carpeta del proyecto backend:
   ```bash
   cd BackendProyecto
3. Instala las dependencias necesarias para el backend
4. Configura la base de datos MySQL y asegúrate de tener las credenciales para la conexión.

### Configuración
Backend
1. Configura las credenciales de la base de datos en el archivo application.properties del backend:
   ```bash
   spring.datasource.url=jdbc:mysql://localhost:3306/nombre_base_datos
   spring.datasource.username=usuario
   spring.datasource.password=contraseña
   
2. Realiza la migración de la base de datos, si es necesario, para que todas las tablas estén actualizadas.

Frontend
1. En el archivo svelte.config.js, asegura la configuración del adaptador para Vercel.
2. En el archivo axiosConfig.js, modifica la baseURL para que apunte a la URL de tu backend en producción:
     ```bash  
      const axiosInstance = axios.create({
    baseURL: 'https://refreshing-expression-production.up.railway.app',
    timeout: 10000,
    });
    export default axiosInstance;

Ejecucion    

Backend
1. Navega a la carpeta del backend y ejecuta el servidor
   ```bash
   ./mvnw spring-boot:run
El backend debería estar disponible en http://localhost:8080.

Frontend
1. Navega a la carpeta del frontend y ejecuta el proyecto:
   ```bash
   npm install
   npm run dev
El frontend debería estar disponible en http://localhost:5173.

### Endpoints del Backend
Algunos de los endpoints disponibles son:

POST /administrador/login: Autenticación de administradores.
GET /pedido: Obtiene todos los pedidos.
POST /pedido: Crea un nuevo pedido.
PUT /pedido/{id}: Actualiza un pedido existente.
DELETE /pedido/{id}: Elimina un pedido.
Otros endpoints para clientes, muebles, materiales, y empleados.

Frontend
El frontend se despliega en Vercel:
1. En el archivo svelte.config.js, asegura la configuración del adaptador para Vercel.
2. Conéctalo a tu repositorio de GitHub y sigue las instrucciones de despliegue en Vercel.

### Proyecto Desplegado
Enlace al proyecto en Vercel: https://frontend-proyecto-umber.vercel.app/

### Video de YouTube
Link a YouTube: https://youtu.be/Ipp_Ikucs1Q
