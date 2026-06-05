# PRODUCT STRORE LAUNCHER (Git Submodules & Dockerize Microservices)

## Setup

Pasos para levantar el Product Store Launcher: `product-store-luncher`

1. Clonar el repositorio.
2. Crear y agregar las variables de entorno en `.env` basado en `.env.example`.
3. Ejecutar la app `docker compose up --build` o `docker compose up`.

## Git Submodules

Git Submodules son una características de Git que permite incluir un repositorio Git dentro de otro repositorio, manteniendo historiales separados.

Es como tener una biblioteca principal con una estantería independiente dentro. La biblioteca grande sabe qué edición exacta de esa estantería debe usar, pero la estantería sigue siendo un proyecto aparte.

Lo importante es que el repositorio principal no guarda todos los archivos del submódulo directamente, sino una referencia a un commit especifico.

## Docker

Docker es una plataforma que permite empaquetar una aplicación junto con todo los que necesita para ejecutarse: código, librerías, dependencias y configuraciones. Ese paquete se llama contenedor.

Conceptos rápidos:

- _Imagen_ - plantilla o receta.
- _Contenedor_ - instancia ejecutándose de esa image.
- _Dockerfile_ - instrucciones para construir la image.
- _Docker Compose_ - coordina varios servicios.
