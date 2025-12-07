# AeroGalaxy – Sistema de Gestión de Misiones y Reserva Espacial


## Taller Opcional #1 – Curso 750006-C Bases de Datos
Universidad / Desarrollo de Software By Sebastian Orejuela Albronoz
 Descripción del Proyecto

AeroGalaxy es una empresa dedicada al turismo espacial y misiones científicas interplanetarias. Debido a su crecimiento acelerado, necesita un sistema de gestión que permita administrar:

Vuelos y misiones espaciales

Tripulaciones

Pasajeros

Cargas científicas y comerciales

Reservas y asignación de naves

Notificaciones automáticas a los usuarios

Cada usuario debe registrarse y especificar condiciones especiales espaciales, tales como:

Traje presurizado avanzado

Sensibilidad gravitacional

Entrenamiento EVA limitado

Requerimientos físicos especiales

El sistema debe permitir reservar vuelos, registrar cargas, gestionar naves asignadas y manejar la comunicación con los usuarios mediante un sistema de notificaciones.

 Objetivos del Taller

Este repositorio demuestra la capacidad para:

✔️ Desplegar servicios utilizando Docker
✔️ Configurar un motor de base de datos PostgreSQL v14
✔️ Administrar la base de datos mediante pgAdmin 4
✔️ Crear una base de datos llamada aerogalaxy
✔️ Construir tablas utilizando instrucciones DDL
✔️ Insertar registros utilizando instrucciones DML
✔️ Documentar el proceso en un README profesional (este documento)



 1. Levantar contenedor PostgreSQL v14
docker run -d \
  --name aeropostgres \
  --network aero_net \
  -e POSTGRES_USER=aerogalaxy \
  -e POSTGRES_PASSWORD=aerogalaxy_db \
  -e POSTGRES_DB=aerogalaxy \
  -p 5432:5432 \
  postgres:14

 2. Levantar contenedor pgAdmin 4
docker run -d \
  --name aeropgadmin \
  --network aero_net \
  -e PGADMIN_DEFAULT_EMAIL=usuario@aerogalaxy.com \
  -e PGADMIN_DEFAULT_PASSWORD=galaxy#445 \
  -p 5050:80 \
  dpage/pgadmin4

 Configuración Inicial en pgAdmin

Acceder a pgAdmin desde el navegador:
 http://localhost:5050

Iniciar sesión con:

Usuario: usuario@aerogalaxy.com

Contraseña: galaxy#445

Crear un nuevo servidor:

Name: aeropostgres

Host: aeropostgres

User: aerogalaxy

Password: aerogalaxy_db

Verificar conexión y visualizar la base de datos aerogalaxy.

## Modelo de Datos (Basado en las Dependencias Funcionales)

Dependencias funcionales consideradas:

planeta_residencia → nombre_planeta, codigo_interplanetario

mision_id → nave_id, fecha_lanzamiento, duracion_horas, estado, destino

carga_id → tipo_carga, descripcion, peso_kg, mision_id



 Contenido del Video Entregado

El video incluye:

 Instrucciones utilizadas para ejecutar los contenedores en Docker

 Acceso exitoso a pgAdmin

 Conexión al servidor PostgreSQL

 Creación de la BD aerogalaxy

 Creación de dos tablas

 Inserción de registros

(Opcional) Publicación del repositorio

(Opcional) Explicación del README

 Repositorio en GitHub

(Puedes colocar aquí tu enlace cuando lo subas)
https://github.com/tu-usuario/aerogalaxy

 Conclusión

Este proyecto demuestra habilidades fundamentales en:

Administración de bases de datos

Uso de Docker

Modelado relacional

DDL y DML

Documentación profesional
