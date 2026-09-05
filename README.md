# Gestión de club náutico y API REST

Aplicación web académica para gestionar los socios, inscripciones,
embarcaciones, patrones, alquileres y actividades de un club náutico. Incluye
una interfaz web y una API REST desarrolladas con Java y Spring Boot.

## Funcionalidades

- Alta, consulta, modificación y eliminación de socios.
- Gestión de inscripciones individuales y familiares.
- Administración de embarcaciones y patrones.
- Vinculación de patrones con embarcaciones.
- Consulta de disponibilidad y alquiler de embarcaciones.
- Organización y modificación de reservas de actividades.
- Validación de restricciones del dominio y tratamiento de errores HTTP.
- Clientes Java de demostración para probar respuestas correctas y casos de
  error de la API.

## API REST

La API implementa operaciones mediante los métodos:

- `GET` para consultar recursos y disponibilidad.
- `POST` para crear socios, inscripciones, embarcaciones, alquileres y reservas.
- `PUT` y `PATCH` para modificaciones completas o parciales.
- `DELETE` para cancelaciones y eliminaciones sujetas a restricciones.

Los controladores REST están separados de los controladores de la interfaz web
y utilizan códigos de estado HTTP para comunicar el resultado de cada
operación.

## Tecnologías

- Java 17.
- Spring Boot y Spring Web.
- Thymeleaf.
- JDBC.
- MySQL.
- Maven.
- HTML y CSS.
- Git y GitHub.

## Estructura

```text
src/main/java/es/uco/pw/pw2526/
├── api/          Controladores de la API REST
├── client/       Clientes Java de demostración
├── controller/   Controladores de la interfaz web
└── model/
    ├── domain/   Entidades del dominio
    └── repository/ Acceso a datos mediante JDBC

src/main/resources/
├── db/           Esquema de la base de datos
├── static/       Estilos e imágenes
└── templates/    Vistas Thymeleaf
```

## Configuración

1. Crea una base de datos MySQL.
2. Ejecuta `src/main/resources/db/create_db.sql`.
3. Define las variables de entorno:

```dotenv
DB_URL=jdbc:mysql://localhost:3306/club_nautico
DB_USERNAME=usuario
DB_PASSWORD=contraseña
```

No publiques credenciales reales en `application.properties`.

## Ejecución

Con Java 17 y Maven instalados:

```bash
mvn spring-boot:run
```

La aplicación se inicia por defecto en `http://localhost:8080`.

## Desarrollo en equipo

Proyecto realizado en la asignatura Programación Web del Grado en Ingeniería
Informática de la Universidad de Córdoba durante el curso 2025/2026.

Autores:

- Carlos Raigón Serrano.
- Ángel Rodríguez Tarancón.
- Alejandro González López.
- Rafael Martín Victorio.
