# Canal de actualizaciones — Gestión de fichas (Asesoría Albereda 36)

Repositorio **privado**. Los programas instalados leen de aquí `actualizaciones/ultima.json`
y el paquete que indica; nada más.

- Cada paquete va firmado con la clave privada de `%USERPROFILE%\.gestion-fichas\`.
  El programa rechaza lo que no esté firmado con ella, así que este repositorio no
  necesita ser secreto para ser seguro, pero sí **privado**: los paquetes llevan el
  código del programa.
- **Nunca** hay datos del cliente aquí: el publicador solo empaqueta código.
- No se toca a mano. Se publica desde el proyecto:

```
cd gestion-fichas
node herramientas/publicar.js 1.1.1 "Qué cambia" --subir
```

El programa del cliente la instala la próxima vez que se abra.
