# Copias de NCGEP

Criticidad: alta. La cadena todavía no está lista para copiarse.

## Ahora

Se copia solo la configuración de `cored`: `/srv/ncgep/main-v04/config` en eu-es-ion-01 y en eu-es-ion-02. Ahí están `config.toml`, `app.toml`, `client.toml` y las identidades del nodo. No entra `data/` ni `.ncgep/data`. El cron que paraba el nodo para exportar la cadena está retirado.

La política se llama `ncgep config`. El destino es el repositorio REST01 de cada VPS. rmm la ejecuta a las 05:40 UTC.

## Más adelante

Cuando la cadena esté lista, la copia será una exportación periódica del tipo instantánea. La primera versión será completa. La incremental vendrá después. El procedimiento, todavía sin activar:

1. Parar solo `ncgep-cored`.
2. Exportar a un fichero nuevo bajo `/var/backups/ncgep`.
3. Arrancar el nodo y comprobar que vuelve a `running`. Si no vuelve, no se da por buena la copia.
4. Dejar el fichero para que restic lo recoja. No copiar `data/` en caliente.
5. Conservar el nodo en marcha al terminar.

Hasta que ese procedimiento se active, la exportación no forma parte de la copia.
