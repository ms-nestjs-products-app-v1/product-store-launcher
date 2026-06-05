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
        + Reconstruir los modules de los submodules
            $ npm install

        + ¡¡¡NOTA IMPORTANTE!!!: 
            - Si trabajamos en el repositorio que tiene submodules, PRIMERO ACTUALIZAR Y HACER PUSH en el submodule y DESPUES en el repositorio principal.
            - Si se hace al revés, se perderán las referencias de los submodules en el repositorio principal y tendremos que resolver conflictos.

* VSCode
    - Shortcuts
        + Vista Previa de Markdown (CTRL + SHIFT + P > Search: ... 'Markdown: Open Preview')
        + Intefaz visual para Git (CTRL + SHIFT + P > Seaarch: ... "Source Control: Focus on Changes View") 