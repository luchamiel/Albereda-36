# Notas de versión — Gestión de fichas (Asesoría Albereda 36)

La más reciente, arriba. Cada una llega sola a los programas instalados la próxima vez que se abren.

## 1.1.1 — 2026-09-26

Importar una carpeta entera: se miran todas sus subcarpetas y cada factura se coloca sola en su cliente, año, trimestre y tipo cuando no hay duda (lo dudoso queda para revisar). Los importes leídos del PDF quedan por confirmar. «Buscarla por mí» ya no confunde el archivo con una copia parcial.

## 1.1.0 — 2026-09-23

Primera versión con actualizaciones automáticas.

- **Se actualiza solo.** Al abrir el programa con `INICIAR.bat` comprueba si hay versión nueva y la instala. Tus datos no se tocan nunca.
- **Si una versión nueva fallara al arrancar,** el programa vuelve solo a la anterior y no la vuelve a instalar.
- **Volver a la versión anterior** desde *Configuración → Versión del programa*, cuando quieras.
- **Carpeta de las facturas:** si el programa no la encuentra, lo avisa y la busca él solo en el equipo («Buscarla por mí»), o la compruebas tú antes de guardarla.
- **Visor al lado:** «Ver» abre el PDF junto a la tabla, para corregir importes con la factura delante (Esc para cerrarlo).
- **Clasificación por bloques y trazabilidad:** aprobar de una vez los cambios seguros (copias repetidas, documentos que no son factura) y ver o deshacer cada cambio.
- **Protección de los datos:** si la base de datos estuviera dañada, el programa se para sin tocarla y dice dónde están las copias.
