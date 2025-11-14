# WorkFlow de GitHub Actions y MkDocs

En este apartado se describe la creación del workflow para automatizar la generación y el despliegue de la documentación web utilizando MkDocs mediante GitHub Actions.

## Pasos realizados

1. Creación del archivo `.github/workflows/CreacionDocumentacion.yml` con los pasos necesarios.
2. Configuración para ejecutar el workflow cada vez que se haga push en la rama principal.
3. Instalación de las dependencias requeridas para MkDocs.
4. Publicación automática en GitHub Pages tras cada actualización.

### Ejemplo de archivo CreacionDocumentacion.yml

```bash

name: Deploy MkDocs

on:
  push:
    branches:
      - main

jobs:
  deploy:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Repo
        uses: actions/checkout@v3

      - name: Set up Python
        uses: actions/setup-python@v4
        with:
          python-version: '3.x'

      - name: Upgrade pip & Install dependencies
        run: |
          python -m pip install --upgrade pip
          pip install mkdocs mkdocs-material

      - name: Deploy docs
        run: mkdocs gh-deploy --force
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

```

Incluye capturas de la pestaña Actions mostrando el workflow y su ejecución correcta.
