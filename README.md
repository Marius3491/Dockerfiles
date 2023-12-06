# Dockerfiles
## Ficheros Dockers

1. Dentro de la carpeta `/srv`, debes crear la carpeta `wordpress` y dentro de esta, las carpetas `db` y `statics`.

```bash
mkdir -p /srv/wordpress/db
mkdir -p /srv/wordpress/statics
```

2. Edita los ficheros `/etc/hosts` tanto en Windows como en Debian para agregar la dirección IP de la instancia EC2 de AWS y el nombre que aparece en el `docker-compose.yml`.

   - En Windows, puedes encontrar el archivo en `C:\Windows\System32\drivers\etc\hosts`.
   - En Debian, el archivo se encuentra en `/etc/hosts`.

   Agrega la siguiente línea al final del archivo:

   ```
   <IP_de_la_instancia_EC2> <nombre_en_docker-compose.yml>
   ```

   Reemplaza `<IP_de_la_instancia_EC2>` con la dirección IP de tu instancia EC2 y `<nombre_en_docker-compose.yml>` con el nombre especificado en tu archivo `docker-compose.yml`.

Recuerda reiniciar los servicios de red o reiniciar la máquina después de realizar estos cambios.

Este proceso permitirá que la instancia EC2 y el contenedor Docker se comuniquen correctamente.
