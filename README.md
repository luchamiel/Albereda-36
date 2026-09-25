# Canal de actualizaciones — Gestión de fichas (Asesoría Albereda 36)

Repositorio **privado**. Los programas instalados leen de aquí `actualizaciones/ultima.json`
y el paquete que indica; nada más. Qué trae cada versión: [NOTAS-DE-VERSION.md](NOTAS-DE-VERSION.md).

```
actualizaciones/
  ultima.json                  la última versión publicada (firmada)
  gestion-fichas-X.Y.Z.gfpaq   el programa de esa versión, empaquetado y firmado
NOTAS-DE-VERSION.md            historial de cambios, lo más nuevo arriba
```

- Los ficheros del programa **no van sueltos**: van dentro de cada `.gfpaq`, firmado con la
  clave privada de `%USERPROFILE%\.gestion-fichas\`. El programa rechaza lo que no esté
  firmado con ella.
- **Nunca** hay aquí datos del cliente, `.env`, registros ni documentos internos: el
  publicador solo empaqueta código.
- **No se sube nada desde la web de GitHub.** Todo se publica desde el proyecto:

```
cd gestion-fichas
node herramientas/publicar.js 1.1.1 "Qué cambia, en una frase" --subir
```

El publicador sube la versión, firma, añade la entrada a las notas y lo sube. El programa
del cliente la instala la próxima vez que se abra.
