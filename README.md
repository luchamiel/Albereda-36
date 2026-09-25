# Canal de actualizaciones — Gestión de fichas (Asesoría Albereda 36)

Repositorio **privado**. Los programas instalados leen de aquí `actualizaciones/ultima.json`
y el paquete que indica; nada más. Qué trae cada versión: [NOTAS-DE-VERSION.md](NOTAS-DE-VERSION.md).

```
instalacion/
  Gestion-de-fichas-Albereda36.zip   instalación completa para el equipo de la asesoría
  Guia-de-uso-Albereda36.html        guía de uso
actualizaciones/
  ultima.json                  la última versión publicada (firmada)
  gestion-fichas-X.Y.Z.gfpaq   el programa de esa versión, empaquetado y firmado
NOTAS-DE-VERSION.md            historial de cambios, lo más nuevo arriba
```

## Instalar (solo la primera vez)

1. Descarga `instalacion/Gestion-de-fichas-Albereda36.zip` (botón *Download raw file*) y descomprímelo.
2. Doble clic en `INICIAR.bat`. Si falta Node.js, se abre la guía para instalarlo.
3. La primera vez, si avisa de que falta la carpeta de las facturas, pulsa **«Buscarla por mí»**.

A partir de ahí el programa se actualiza solo cada vez que se abre: no hay que volver a descargar nada.

## Cómo funciona

- Los ficheros del programa **no van sueltos**: van dentro de cada `.gfpaq`, firmado con la
  clave privada de `%USERPROFILE%\.gestion-fichas\`. El programa rechaza lo que no esté
  firmado con ella.
- El ZIP de `instalacion/` lleva los datos de la asesoría y la clave de lectura de este
  repositorio: por eso el repositorio es **privado** y solo se comparte con la asesoría.
  Las actualizaciones (`actualizaciones/`) nunca llevan datos: el publicador solo empaqueta código.
- Nunca van aquí `.env` sueltos, registros ni documentos internos.
- **No se sube nada desde la web de GitHub.** Todo se publica desde el proyecto:

```
cd gestion-fichas
node herramientas/publicar.js 1.1.1 "Qué cambia, en una frase" --subir
```

El publicador sube la versión, firma, añade la entrada a las notas y lo sube. El programa
del cliente la instala la próxima vez que se abra.
