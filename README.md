# Canal de actualizaciones — Gestión de fichas (Asesoría Albereda 36)

Repositorio **privado**. Los programas instalados leen de aquí `actualizaciones/ultima.json`
y el paquete que indica; nada más. Qué trae cada versión: [NOTAS-DE-VERSION.md](NOTAS-DE-VERSION.md).

```
instalacion/
  Gestion-de-fichas-Albereda36.zip   el programa (con INICIAR.bat), vacío y sin la clave
  Guia-de-uso-Albereda36.html        guía de uso
actualizaciones/
  ultima.json                  la última versión publicada (firmada)
  gestion-fichas-X.Y.Z.gfpaq   el programa de esa versión, empaquetado y firmado
en-fichero/
  gestion-fichas-X.Y.Z.actualizacion   la última, para instalarla sin internet
NOTAS-DE-VERSION.md            historial de cambios, lo más nuevo arriba
```

## Instalar (solo la primera vez)

El programa está en [`instalacion/Gestion-de-fichas-Albereda36.zip`](instalacion/Gestion-de-fichas-Albereda36.zip).
Va **vacío** (sin clientes, facturas ni datos de nadie) y **sin la clave de las
actualizaciones**, que se entrega aparte.

1. Descarga `instalacion/Gestion-de-fichas-Albereda36.zip` y descomprímelo.
2. Para que se actualice solo: abre `gestion-fichas\.env` con el Bloc de notas, busca la línea
   `# GF_ACTUALIZACIONES_TOKEN=`, quítale el `# ` del principio y pega la clave detrás del `=`.
   Guarda. (Sin este paso el programa funciona igual, pero no se actualiza solo.)
3. Doble clic en `INICIAR.bat`. Si falta Node.js, se abre la guía para instalarlo.
4. La primera vez, si avisa de que falta la carpeta de las facturas, pulsa **«Buscarla por mí»**.

A partir de ahí el programa se actualiza solo cada vez que se abre: no hay que volver a descargar nada.

El ZIP lo genera quien mantiene el programa, siempre sin la clave:
`node herramientas/entrega.js --canal https://api.github.com/repos/luchamiel/Albereda-36/contents/actualizaciones`
(sin `--token-desde`), y se copia a `instalacion/`.

## Cómo funciona

- Los ficheros del programa **no van sueltos**: van dentro de cada `.gfpaq`, firmado con la
  clave privada de `%USERPROFILE%\.gestion-fichas\`. El programa rechaza lo que no esté
  firmado con ella.
- El repositorio es **privado**: los programas lo leen con una clave de solo lectura.
  Aquí no hay datos de la asesoría: las actualizaciones (`actualizaciones/`) solo llevan
  código y nunca tocan los datos de un programa ya instalado.
- Nunca van aquí `.env` sueltos, registros ni documentos internos.
- **No se sube nada desde la web de GitHub.** Todo se publica desde el proyecto:

```
cd gestion-fichas
node herramientas/publicar.js 1.1.1 "Qué cambia, en una frase" --subir
```

El publicador sube la versión, firma, añade la entrada a las notas y lo sube. El programa
del cliente la instala la próxima vez que se abra.
