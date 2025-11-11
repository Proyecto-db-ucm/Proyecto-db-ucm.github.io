<!-- Shields -->
[![Java](https://img.shields.io/badge/Java-17%2B-ED8B00?logo=openjdk&logoColor=white)](https://openjdk.org/)
[![Spring Boot](https://img.shields.io/badge/Spring%20Boot-3.3%2B-6DB33F?logo=springboot&logoColor=white)](https://spring.io/projects/spring-boot)
[![React](https://img.shields.io/badge/React-18.3%2B-61DAFB?logo=react&logoColor=white)](https://react.dev/)
[![Oracle DB](https://img.shields.io/badge/Oracle%20DB-19c%2B-F80000?logo=oracle&logoColor=white)](https://www.oracle.com/database/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker&logoColor=white)](https://www.docker.com/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Status](https://img.shields.io/badge/Status-En%20Desarrollo-28a745)](https://github.com/tu-usuario/residencial-del-maule-crud)

<p align="center">
  <img src="https://github.com/Proyecto-db-ucm/Proyecto/blob/main/notfound.png" alt="Residencial del Maule - Linares, Chile" width="800"/>
  <br>
  <em>Hostal Residencial del Maule - Linares, Región del Maule, Chile</em>
</p>

<h1 align="center">Residencial del Maule - Sistema CRUD</h1>

<p align="center">
  <strong>Sistema de gestión integral para hostal en Linares, Chile</strong>
</p>

<p align="center">
  <a href="#-tecnologías">Tecnologías</a> •
  <a href="#-inicio-rápido">Inicio Rápido</a> •
  <a href="#-docker">Docker</a> •
  <a href="#-estructura">Estructura</a> •
  <a href="#-contribuir">Contribuir</a>
</p>

---

## Descripción del Proyecto

Sistema **full-stack CRUD** desarrollado para el **Hostal Residencial del Maule**, ubicado en **Linares, Región del Maule, Chile**.  
Diseñado para pequeñas residenciales y hostales, con enfoque en **robustez, escalabilidad y soporte nativo para Oracle Database**.

Funcionalidades clave:
- Gestión de huéspedes
- Reservas con check-in/check-out
- Administración de habitaciones
- Control de pagos
- Reportes y estadísticas

> **Ideal para empresas chilenas que usan Oracle en producción.**

---

## Tecnologías Utilizadas

| Capa         | Tecnología                        | Versión         |
|--------------|-----------------------------------|-----------------|
| **Backend**  | **Java + Spring Boot 3**          | `17+` / `3.3+`  |
| **Frontend** | React + Vite + Tailwind CSS       | `^18.3.0`       |
| **DB**       | **Oracle Database (XE / 19c+)**   | `19c+`          |
| **ORM**      | Spring Data JPA + Hibernate       | `^3.3`          |
| **Build**    | Maven                             | `3.9+`          |
| **Despliegue**| Docker + Docker Compose           | `latest`        |

---

## Características Principales

- Registro completo de **huéspedes** (RUT, pasaporte, contacto)
- **Habitaciones** por tipo: individual, doble, suite
- **Reservas** con calendario y disponibilidad en tiempo real
- Check-in / Check-out con notificaciones
- **Pagos**: efectivo, transferencia, tarjeta (próximamente SII)
- Panel admin con **reportes PDF**
- Diseño **100% responsive**
- Integración nativa con **Oracle Database** (JDBC + ojdbc11)

---

## Inicio Rápido

### Prerrequisitos

```bash
- Java 17 (JDK) → Descarga: https://adoptium.net/
- Node.js 18+ (incluye npm) → Descarga: https://nodejs.org/
- Oracle Database XE (Express Edition) → Descarga: https://www.oracle.com/database/technologies/appdev/xe.html
- Maven 3.9+ → (Opcional: usa `./mvnw` si no lo tienes instalado)
- Git → Descarga: https://git-scm.com/
- Docker + Docker Compose → (Solo si usas el modo Docker) → https://www.docker.com/
```

### Arranque
```bash
# 1. Clonar el repositorio
git clone https://github.com/tu-usuario/residencial-del-maule-crud.git
# → Este comando descarga una copia completa del repositorio desde GitHub a tu máquina local,
#    creando una carpeta con el nombre del proyecto. Útil para obtener el código fuente inicial.

cd residencial-del-maule-crud
# → Cambia el directorio actual a la carpeta del proyecto recién clonado, para que todos los
#    comandos posteriores se ejecuten dentro de él.

# SI ES QUE YA TIENE LA COPIA ACTUAL DEL REPOSITORIO IGNORE ESTE COMANDO!!!
```
---
### TERMINAL 1: Backend (Spring Boot + Maven)
```bash
cd FOLDER-BACKEND
# direccion en donde guarda el folder del backend
./mvnw spring-boot:run
# → Ejecuta Maven Wrapper (./mvnw) para compilar el código Java, resolver dependencias (como ojdbc para Oracle),
#     y levantar el servidor Spring Boot. Esto inicia la API REST en el puerto 8080, permitiendo que el frontend
#     se conecte a ella. Si hay errores, verifica las dependencias en pom.xml.

# → API REST en http://localhost:8080 → Aquí puedes probar endpoints como /api/habitaciones directamente.

# → Swagger UI en http://localhost:8080/swagger-ui.html → Interfaz gráfica para documentar y probar la API automáticamente.
```
---
### TERMINAL 2: Frontend (React + Vite)
```bash
cd FOLDER-FRONT
# → NOMBRE DE LA CARPETA DONDE SE ALOGA EL PROYECTO FRONT-END

npm install
# → Instala todas las dependencias del frontend definidas en package.json (como React, Tailwind CSS,
#      Axios para llamadas API). Esto crea la carpeta node_modules. Ejecuta solo la primera vez
#      o si cambian dependencias; puede tardar unos minutos dependiendo de tu conexión.


npm run dev
# → Inicia el servidor de desarrollo de Vite, que compila el código React en tiempo real, habilita
#     hot reload (cambios se ven inmediatamente), y sirve la aplicación en el puerto 5173. Ideal para
#     desarrollo; usa 'npm run build' para producción.
# → App en http://localhost:5173 → Abre esta URL en tu navegador para ver la interfaz del sistema
#    (conecta automáticamente al backend en 8080).

# ESTO PERMITE ARRANCAR EL FRONT
```
---
### Con Docker (Recomendado – 1 solo comando)
```bash
git clone https://github.com/tu-usuario/residencial-del-maule-crud.git
cd residencial-del-maule-crud

docker-compose up --build
# → Construye y levanta contenedores para frontend, backend y Oracle DB. '--build' recompila
#     imágenes si hay cambios. Ejecuta en una terminal; presiona Ctrl+C para detener.
```
