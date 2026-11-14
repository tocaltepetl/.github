# Cómo contribuir

¡Gracias por tu interés! Los proyectos de tocaltepetl son cívicos y
voluntarios. Cualquier aporte es bienvenido: reportar errores, proponer
ideas, mejorar el diseño o el código, o corregir la documentación.

Estas reglas aplican a todos los repos. Cada uno explica en su README (o en su
propio `CONTRIBUTING.md`) cómo correrlo y sus reglas específicas.

## Privacidad
Sigue la [política de privacidad común](docs/privacidad.md). En resumen:
- La ubicación y los datos de quien usa una página **nunca** salen del
  navegador. No se aceptan rastreadores ni llamadas a terceros con datos del
  usuario.
- La única analítica permitida es el conteo de visitas con Cloudflare Web
  Analytics (sin cookies ni datos personales), y cada proyecto lo avisa en la
  página, el README y `docs/decisiones.md`.
- No incluyas coordenadas, direcciones ni datos personales de nadie en el
  código, issues o capturas.

## Identidad
Los proyectos **no son oficiales**. No uses logos, nombres ni imágenes de
dependencias de gobierno ni de sus apps, ni textos que hagan parecer que lo
son. Para la marca de tocaltepetl usa [`brand/`](brand/).

## Proceso
1. Para cambios grandes, abre primero un issue y platiquemos la idea.
2. Haz un fork y una rama con un nombre descriptivo.
3. Prueba en celular (o la vista móvil del navegador), en modo claro y oscuro.
4. Abre el PR llenando la plantilla. El título sigue
   [Conventional Commits](https://www.conventionalcommits.org/es/v1.0.0/):
   `tipo: descripción`, en español, minúscula y sin punto final.

| Tipo | Para qué | Versión |
|---|---|---|
| `feat` | Algo nuevo para quien usa la página | 0.**X**.0 |
| `fix` | Corrige un error | 0.0.**X** |
| `perf` | Mejora el rendimiento | 0.0.**X** |
| `docs` | Solo documentación | no publica |
| `refactor`, `style`, `test`, `build`, `ci`, `chore` | Mantenimiento | no publica |

Un cambio incompatible lleva `!` (`feat!: …`). Se integra con *squash merge*.

Las decisiones de diseño de cada proyecto están en su `docs/decisiones.md`;
léelas antes de proponer cambios de fondo.

## Idioma
- **Español** para la interfaz, la documentación, los comentarios, los commits,
  los issues y los PRs. En issues y PRs también se vale inglés.
- **Inglés** para los nombres en el código (variables, funciones).

## Conducta
Ver el [código de conducta](CODE_OF_CONDUCT.md).
