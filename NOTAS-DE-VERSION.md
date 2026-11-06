# Notas de versión — Gestión de fichas (Asesoría Albereda 36)

La más reciente, arriba. Cada una llega sola a los programas instalados la próxima vez que se abren.

## 1.1.8 — 2026-11-06

Los PDF con varias facturas se guardan ENTEROS: un solo fichero en la carpeta, con una factura por grupo de páginas (cada una en su trimestre en el IVA y el Excel). Las páginas se agrupan por número de factura con doble revisión (otro número en una hoja, «Página X de Y», dos totales, sin total): lo dudoso se guarda y sale en Revisar. Debajo del PDF, en todos los visores, la tabla de sus facturas con la base y el IVA de cada tipo (0, 4, 10, 21 %) y si cuadra; pulsar una fila lleva a su página. Se lee el recuadro resumen del pie (Base imponible · Tipo · Cuota · Total), con varios tipos, recargo e IRPF, mirando las otras hojas si hace falta. Revisar: «Revisión rápida» emitida o gasto con teclas (G, I, O, Intro) y decidir por proveedor; decidir el tipo ya no borra otros avisos. La descarga nueva viene vacía.

## 1.1.7 — 2026-11-03

Deja de ser una demostración: un programa recién instalado empieza vacío, sin clientes, facturas ni grupos de ejemplo, y los que ya están instalados pierden solo los grupos, el servidor, el periodo y la nota de ejemplo (sus clientes, facturas y documentos no se tocan). Nuevo «Historial»: cada cosa que se hace en el programa (importar, ordenar, revisar, exportar, clientes, facturas, configuración, actualizaciones y cada vez que se abre) queda apuntada con su fecha y equipo, aparte de los datos, así que ni ordenar una carpeta nueva ni recuperar una copia la borran; se puede filtrar y descargar en CSV. Al crear un informe se propone el trimestre que toca presentar.

## 1.1.6 — 2026-11-03

Mejor lectura de escaneos. El OCR rehace las filas como en la hoja (etiqueta a la izquierda, valor a la derecha) y endereza los escaneos torcidos: más escaneos analizados y muchos menos «Sin número de factura». Se reconocen números como «FACTURA 079-0003-353470» (Leroy Merlin, Bricomart) y «Número de la factura» (Amazon). Arreglado: al separar un PDF por hojas, el número de página del nombre ya no sale como número de factura. Los detalles de llamadas siguen con su factura aunque el OCR lea mal el número, y la primera hoja de la factura siguiente o dos facturas seguidas del mismo día ya no se juntan. Aviso si la fecha leída es posterior a hoy.

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
