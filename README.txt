PRODUCT STRORE LAUNCHER (Git Submodules & Dockerize Microservices)

* Git
    - Crear un nuevo repositorio dentro de la 'Microservice Organization' (Click "New Repository")
        > Owner:                  Repository name:
          {{ORGANIZATION_NAME}} / product-store-launcher
        > Description: Product Store Launcher (Git Submodules & Dockerize Microservices)
        > Public
        Click 'Create repository'
    - Submodules (Repositorio añadido dentor de otro repositorio principal)
        + Agregar repositorios extenos al repositorio principal
            * Cliente Gateway
                $ git submodule add {{REPOSITORY_URL}} client-gateway
            * Products Microservice
                $ git submodule add {{REPOSITORY_URL}} products-ms
            * Orders Microservice
                $ git submodule add {{REPOSITORY_URL}} orders-ms
            * Payments Microservice
                $ git submodule add {{REPOSITORY_URL}} payments-ms
            * Auth Microservice
                $ git submodule add {{REPOSITORY_URL}} auth-ms
        + Actualizar las referencias de los submodules
            $ git submodule update --remote
        + Descargar, inicializar y sincronizar el contenido de todos los submodules (repositorio externos anidados)
            $ git submodule --init --recursive
        + Reconstruir los modules de los submodules
            $ npm install

        + ¡¡¡NOTA IMPORTANTE!!!: 
            - Si trabajamos en el repositorio que tiene submodules, PRIMERO ACTUALIZAR Y HACER PUSH en el submodule y DESPUES en el repositorio principal.
            - Si se hace al revés, se perderán las referencias de los submodules en el repositorio principal y tendremos que resolver conflictos.

        + Recrear la DB de un submodule (Optional: solo con Prisma SQLite pero con otras DBs no será necesario)
            - Ingresar al submodule, crear el archivo `.env` y generar manualmente la DB
                $ npx prisma migrate dev        // Recontruye la DB en el submodule local

* Docker
    - Configuraciones de los repositories
        + Product Store Launcher
            * Crear el archivo `docker-compose.yml`.
        + Client Gateway
            * Crear el archivo `dockerfile`.
        + Products Microservice
            * Crear el archivo `dockerfile`.
    + Comandos (Terminal)
        + Compilar (reconstruir) las imágenes y levantar los contenedores
            $ docker compose up --build
            $ docker compose up --build d           // Modo detach o segundo plano
        + Levantar los contenedores (Sin reconstruir)
            $ docker compose up 
        + Detener y eliminar los contenedores e imágenes
            $ docker compose down

* VSCode
    - Shortcuts
        + Vista Previa de Markdown (CTRL + SHIFT + P > Search: ... 'Markdown: Open Preview')
        + Intefaz visual para Git (CTRL + SHIFT + P > Seaarch: ... "Source Control: Focus on Changes View") 