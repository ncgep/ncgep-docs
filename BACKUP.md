# Copias de NCGEP

Criticidad: alta. El historial de bloques no se regenera desde git.

## Método

No se copia `/srv/ncgep` en caliente. En eu-es-ion-01, `/etc/cron.d/ncgep-export` (domingo 05:10 UTC) para `ncgep-cored`, exporta y lo vuelve a arrancar. El JSON queda en `/var/backups/ncgep`. El script ya no llama a restic.

La política `ncgep cored export` copia ese directorio cada día a las 05:40 UTC hacia el repositorio REST01 de ion-01.

eu-es-ion-02 tiene el mismo nodo y no tiene exportación. Su directorio de unos 7,5 GB no se copia en bruto. Si hace falta una exportación propia, es el mismo procedimiento y hay que dejar el nodo en marcha al terminar.

## Verificación el 2026-10-19

Exportación `ncgep-main-20261019T074649Z.json`, 31394 bytes. El nodo volvió a `running`. Instantánea rmm `6cb473534c1c`. La restauración del directorio coincidió con el fichero vivo.
