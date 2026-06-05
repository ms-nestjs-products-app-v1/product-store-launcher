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


* VSCode
    - Shortcuts
        + Vista Previa de Markdown (CTRL + SHIFT + P > Search: ... 'Markdown: Open Preview')