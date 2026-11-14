# Solicitudes de acceso a la información

Forma común de preparar, enviar, seguir y publicar solicitudes de
transparencia en todos los proyectos de
[tocaltepetl](https://github.com/tocaltepetl). El objetivo es que el gobierno
publique como **datos abiertos** la información que ya tiene, para que llegue
a la ciudadanía sin depender de plataformas privadas.

## Dónde vive cada cosa
| Qué | Dónde |
|---|---|
| Esta guía y la [plantilla](plantilla.md) | `.github/docs/solicitudes/` (común) |
| Cada solicitud de un proyecto | `docs/solicitudes/AAAA-MM-DD-sujeto-tema.md` en el repo del proyecto |
| Respuestas recibidas (PDF, archivos) | `docs/solicitudes/respuestas/` del proyecto, sin datos personales |
| Página o ficha pública para que la gente también pregunte | opcional; muestra el texto del `.md`, no lo duplica (ver abajo) |

Un archivo por solicitud (por sujeto obligado). Si el mismo texto se manda a
dos dependencias, son dos archivos.

## Cómo se escribe una solicitud
Usa la [plantilla](plantilla.md). Reglas:

1. **Fundamento corto:** artículo 6.º constitucional y la ley de transparencia
   que aplique (en Jalisco: Ley de Transparencia y Acceso a la Información
   Pública del Estado de Jalisco y sus Municipios). No cites artículos ni plazos
   que no hayas verificado.
2. **Puntos numerados, uno por dato.** Cada punto dice qué documento o dato se
   pide, de qué periodo, con qué nivel de detalle y **con qué campos** (p. ej.
   «id del camión, ruta, fecha y hora, lat, lng»). Así una respuesta parcial
   se puede evaluar punto por punto.
3. **Pide documentos que existen**, no opiniones ni explicaciones: archivos,
   contratos, convenios, bases de datos, manuales técnicos, direcciones de
   servicios. En vez de «¿por qué no funciona?», pide «reportes de incidencia,
   órdenes de servicio y el plan o cronograma para restablecerlo». Si hay pruebas de que existen (p. ej. el gobierno ya los dio a
   una empresa), menciónalo.
4. **Formato abierto y legible por máquina** (CSV, JSON, GTFS, SHP…), no PDF
   escaneado. Modalidad electrónica, sin costo.
5. **Versión pública:** si algo es reservado o confidencial, pide la versión
   pública del resto y la prueba de daño.
6. **Propiedad y licencia de los datos:** cuando hay un proveedor privado,
   pide las cláusulas sobre quién es dueño de los datos y cómo pueden usarse.
7. **Publicación permanente:** cierra pidiendo que la información se publique
   de forma permanente como datos abiertos, documentados, actualizados y con
   licencia de libre uso; y pregunta si se prevé y en qué fecha.
8. Lenguaje llano, sin adjetivos ni acusaciones: pedir no requiere justificar.

## Quién la envía
- La envía una **persona** desde su cuenta de la
  [Plataforma Nacional de Transparencia](https://www.plataformadetransparencia.org.mx).
  Ni los proyectos ni Claude envían solicitudes a nombre de nadie.
- Se puede usar seudónimo; la plataforma no exige identificarse.
- Que muchas personas manden la misma solicitud es válido y suma presión: por
  eso cada proyecto puede tener una guía pública con el texto listo para copiar.

## Página para que la ciudadanía pregunte (opcional)
Lo mínimo, en la página del proyecto:
- Por qué importa, en dos o tres frases.
- Botón «Copiar solicitud» con el texto de la sección «Texto para pegar» del
  `.md`. Si la página no puede leer el `.md` (sitio estático, `file://`), se
  copia el texto en la página con un comentario
  `<!-- fuente: docs/solicitudes/<archivo>.md -->`, y el PR que cambie uno
  debe cambiar el otro (opcional: un paso de CI que compare ambos textos).
- Enlace a la PNT y pasos: elegir ámbito y sujeto obligado, pegar, modalidad
  electrónica, **guardar el folio**.
- Aviso de que existe el recurso de revisión si no responden o la respuesta no
  convence (sin inventar plazos).
- Invitación a mandar la respuesta como issue (`transparencia`) para
  publicarla.

Opcional, a criterio de cada proyecto:
- Mensajes para compartir en redes (verifica las cuentas oficiales que
  menciones).
- **Registro anónimo de folios** con contador y estados (modelo:
  [rutas-gdl](https://github.com/tocaltepetl/rutas-gdl), `/api/solicitudes`).
  Agrega backend y datos; si un proyecto lo adopta, debe decirlo en su aviso de
  privacidad y en `docs/decisiones.md`. camiones-basura-gdl decidió no tenerlo:
  lo que pesa es la solicitud formal.

## Seguimiento
El encabezado del archivo registra la **solicitud de referencia** del
proyecto. Las que envíen otras personas con el mismo texto se juntan en el
issue `transparencia` (folio, estado y respuesta, sin nombres) o en el
registro anónimo, si el proyecto lo tiene.

Al enviarla, llena el encabezado del archivo (ver plantilla): folio, fecha de
envío y fecha límite que muestra la plataforma. Estados posibles:

`borrador` · `enviada` · `prorroga` · `respondida` · `parcial` · `negada` ·
`sin-respuesta` · `en-recurso` · `cerrada`

- El folio de una solicitud de transparencia **es público** (cualquiera lo
  consulta en la plataforma), así que se puede publicar. No publiques el
  nombre de quien la envió, su correo ni el acuse con datos personales.
- Si vence el plazo sin respuesta, o la respuesta niega o no entrega lo pedido,
  procede el **recurso de revisión** ante el órgano garante (verifica cuál es
  el vigente y su plazo en la plataforma). Registra el folio del recurso en el
  mismo archivo.
- Abre un issue con la etiqueta `transparencia` por solicitud enviada y
  ciérralo cuando quede `cerrada`, para que el seguimiento sea visible.

## Publicar la respuesta
- Sube la respuesta a `docs/solicitudes/respuestas/` quitando datos personales
  de servidores públicos que no sean de su función y de particulares. El PDF
  de respuesta y el acuse suelen traer el nombre o seudónimo y el correo de
  quien solicitó: quítalos antes de subirlos.
- Resume en el archivo de la solicitud qué se entregó punto por punto
  (✅ entregado · ◐ parcial · ❌ negado · — sin respuesta).
- Si entregaron datos útiles, súbelos al proyecto como datos abiertos y
  anótalo en su `docs/decisiones.md`.
- Si se negaron, eso también se publica: es información.

## Revisión antes de enviar
- [ ] Usa la plantilla y cada punto pide un documento o dato concreto
- [ ] Fundamento y plazos verificados (nada inventado)
- [ ] Formato abierto, modalidad electrónica, versión pública
- [ ] Sin datos personales en el archivo del repo
- [ ] Revisada en un PR (`docs:`) antes de enviarla
