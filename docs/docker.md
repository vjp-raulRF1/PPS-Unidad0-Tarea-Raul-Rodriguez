# Publicación con Docker y NGinx

En este apartado se documenta la creación y puesta en marcha de un servicio NGinx en Docker para mostrar la documentación generada en el repositorio.

## Pasos realizados

1. Cambio a la rama `gh-pages` para obtener los archivos estáticos generados por MkDocs.
2. Ejecución del contenedor NGinx publicando la web en el puerto 8085 y montando el directorio de la rama como volumen.
3. Verificación del funcionamiento accediendo a la web vía navegador en `http://localhost:8085/`.
4. Inspección y obtención de información del contenedor con Docker.

### Comandos utilizados

```bash
git checkout gh-pages
docker run --name PPSUnidad0-Tarea_Tu_nombre \
  -p 8085:80 \
  -v $(pwd):/usr/share/nginx/html:ro \
  -d nginx

docker ps
docker inspect PPSUnidad0-Tarea_Tu_nombre
```

![Vista del despliegue con docker completamente funcional](images/contdocker.png)
