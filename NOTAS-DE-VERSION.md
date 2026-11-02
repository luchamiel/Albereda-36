# Notas de versión — Gestión de fichas (Asesoría Albereda 36)

La más reciente, arriba. Cada una llega sola a los programas instalados la próxima vez que se abren.

## 1.1.5 — 2026-11-02

Revisión completa de la 1.1.4. Funciona en cualquier ordenador: archivo en la raíz de una unidad de red (Z:\), primer arranque sin datos, guardado aunque el antivirus u OneDrive tengan la base de datos abierta, aviso si otro equipo tiene el programa abierto en la misma carpeta, .env en ANSI, Node antiguo y OCR en español explicados. Lectura: varias facturas del mismo día en un PDF salen una por fila, las facturas seguidas de un escaneo ya no se juntan, recargo de equivalencia, abonos con el menos detrás o entre paréntesis. Importar y Revisar: «1.500» se lee como mil quinientos, los abonos se confirman, las facturas con varios tipos de IVA conservan su desglose y las sumas coinciden con el Excel. Los abonos importados antes de la 1.1.4 en positivo pasan una vez a Revisar «¿Abono?».

## 1.1.4 — 2026-10-31

Abonos en negativo (los dudosos van a Revisar «¿Abono?»), varios tipos de IVA en la misma fila, albaranes y justificantes en su carpeta, formatos de factura que se aprenden de las correcciones y fotos con varios tickets. Los PDF con varias facturas se leen hoja a hoja: en Importar salen en un bloque, una fila por factura, con un resumen y la suma debajo y el total de todo al final; los escaneos de varias hojas también se leen hoja a hoja.

## 1.1.3 — 2026-10-03

Facturas repetidas, emitida o recibida según el cliente de la factura, separar PDFs con varias facturas, filtro por periodo, empresa/CIF/código postal, exportar a Excel, ZIP o un solo PDF, plantillas de Hacienda y «Descartar» en Revisar. Nuevo: «Actualizar desde un fichero…» instala actualizaciones firmadas (.actualizacion) sin internet. «Quitarlo del programa» ya no mueve nunca el original del cliente.

## 1.1.2 — 2026-09-29

Ordenar una carpeta nueva: el programa lee una carpeta sin ordenar, reconoce los clientes y coloca cada factura en su cliente, año, trimestre y tipo (antes guarda una copia de todo y se puede recuperar). Lee los escaneos y las fotos de tickets con el OCR de Windows, sin que nada salga del ordenador. Al importar se puede indicar que toda la carpeta es de un cliente, decidir de golpe las facturas del mismo proveedor y repasar las dudosas con «Revisión rápida» desde el teclado.

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
