# Creación del repositorio y primeros pasos

En este apartado se documenta la creación y configuración inicial del repositorio en GitHub, así como la estructura de carpetas y archivos necesarios.

## Pasos realizados

1. Creación del repositorio en GitHub con el nombre `PPS-Unidad0-Tarea-Raul-Rodriguez`.
2. Clonación del repositorio en local.
3. Generación de la estructura recomendada de carpetas y archivos para la documentación y el código.
4. Primer commit y push de la estructura al repositorio remoto.
5. Añadir al profesor como colaborador desde Settings > Collaborators.

### Comandos utilizados

```bash
git clone git@github.com:vjp-raulRF1/PPS-Unidad0-Tarea-Raul-Rodriguez.git
git clone git@github.com:vjp-raulRF1/CalculadoraPython-Raul-Rodriguez.git
mkdir PPS-Unidad0-Tarea-Raul-Rodriguez
cd PPS-Unidad0-Tarea-Raul-Rodriguez
cp CalculadoraPython-Raul-Rodriguez .
mkdir -p  .github/workflows
touch  docs/git.md docs/gitActions.md docs/gitPages.md docs/docker.md docs/conclusiones.md
git add .
git commit -m "Estructura inicial del repositorio"
git push origin main

```

![Vista del comando tree una vez acabado el ejercicio](images/tree.png)
