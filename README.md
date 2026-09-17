# Página de Sebastián Carvallo Campos

Landing de marca personal para las asesorías de empleabilidad. Es una sola
página, en un solo archivo: `index.html` tiene el texto, los estilos y todo lo
demás. No hay que compilar nada ni instalar nada.

## Dónde está publicado

Todavía no está en línea. Cuando se publique, hay que anotar la dirección acá
y reemplazarla también dentro de `index.html` (ver "Antes de publicar").

| Dónde | Enlace |
|---|---|
| Sitio | pendiente |
| LinkedIn | pendiente |
| Instagram | pendiente |

Conviene revisar esta tabla cada cierto tiempo para que no queden enlaces
muertos apuntando a la página.

## Antes de publicar: reemplazar el dominio

Dentro de `index.html` hay cuatro lugares que dicen `DOMINIO-PENDIENTE`. Son
los que hacen que, al compartir el enlace por WhatsApp, aparezca la miniatura
con la foto y el nombre. Búscalo con Ctrl+F y reemplaza las cuatro apariciones
por la dirección real, con `https://` y sin barra al final:

- `og:url`
- `og:image`
- `twitter:image`
- `canonical`

Después de reemplazarlas, manda el enlace por WhatsApp a alguien una vez, para
comprobar que la miniatura aparece.

## Cómo se cambia el número de WhatsApp

El número está escrito tres veces en `index.html`, siempre con el mismo
formato: `56936108624` (código de país, sin el signo + y sin espacios). Busca
esa cadena y reemplázala en las tres.

El enlace lleva un mensaje ya escrito, para que quien te escriba llegue
diciendo de dónde viene. Si quieres cambiar ese texto, está en la misma línea,
después de `?text=`, con los espacios escritos como `%20` y los acentos en
código (`á` es `%C3%A1`).

## Cómo se cambia el correo

Aparece cuatro veces como `sebastian.carvallo@outlook.com`: dos en el botón de
contacto (el enlace y el texto visible) y dos en el pie. Reemplázalas todas.

## Cómo se cambia la foto

La foto de la portada es `fotos/sebastian.jpg`, cuadrada, de 900 × 900 píxeles.
Si la reemplazas, mantén el formato cuadrado y el mismo nombre de archivo.

`fotos/og-image.jpg` es la miniatura que se ve al compartir el enlace: 1200 ×
630, con la foto a la derecha y tu nombre a la izquierda. Si cambias la foto de
portada, hay que rehacer también esta.

El original sin comprimir está en `originales/`, que **no se publica** (está en
el `.gitignore`). Todo lo que pongas en esa carpeta queda fuera del sitio.

## Dónde están los textos

Todos dentro de `index.html`, en orden de aparición:

1. Portada: el titular y el párrafo de entrada.
2. "Quién te va a asesorar": tu trayectoria y las cuatro credenciales.
3. La banda azul: los dos lugares donde se cae una postulación.
4. "Tres formas de trabajar juntos": los tres servicios y lo que incluye cada uno.
5. "Qué pasa en esos quince minutos": el desarrollo de la llamada.
6. "Agenda tu diagnóstico": contacto.

## Decisiones que conviene no "arreglar"

**No hay precios en la página, y es a propósito.** La estrategia es evaluar al
cliente en la llamada de diagnóstico y recién ahí cotizar, distinto según esté
en Chile o fuera. Publicar las cifras rompe eso: el visitante compara en frío y
no llama. La sección "Tres formas de trabajar juntos" explica el motivo en voz
propia, que es lo que evita que la ausencia de precio se lea como algo turbio.

**El favicon es un monograma, no un logo.** No hay identidad visual todavía, así
que `fotos/favicon.png` es un cuadrado azul marino con las iniciales. Cuando
exista un logo de verdad, se reemplaza ese archivo manteniendo el nombre.

**Los colores salen de la foto.** El azul marino (`#1D3557`) es el del muro de
la oficina en el retrato, y el fondo es un papel cálido en vez de blanco puro.
Si cambias la foto por una con otro ambiente, revisa que la paleta siga
teniendo sentido.

**El ocre tiene dos tonos.** `--ocre` es para líneas y detalles; `--ocre-texto`
es más oscuro y es el único que se usa sobre texto, porque el otro no alcanza
el contraste mínimo legible.

## Qué falta

- **Testimonios.** En `index.html`, al final de la sección "Qué pasa en esos
  quince minutos", hay un bloque de ejemplo dentro de un comentario HTML. Está
  comentado a propósito: así no se ve mientras no haya testimonios de verdad.
  Cuando tengas dos o tres, con nombre, cargo y resultado concreto, sácalos del
  comentario. No los inventes: en una página de asesoría profesional un
  testimonio falso destruye exactamente la confianza que construye el resto del
  texto.
- **Dominio propio.** Mientras no lo haya, la miniatura al compartir no va a
  funcionar.

## Acceso directo en el teléfono

La página trae `manifest.json` y los iconos `fotos/icono-*.png`, que son los que
hacen que al agregarla a la pantalla de inicio quede con el cuadrado azul y las
iniciales, y con el nombre corto "Sebastián Carvallo" en vez del título largo.

- **Android (Chrome):** menú de tres puntos > Agregar a pantalla principal.
- **iPhone (Safari):** botón de compartir > Añadir a pantalla de inicio.

En iPhone sólo funciona desde Safari, no desde Chrome.

## Cómo se publica un cambio

Hay dos caminos, según cómo se haya publicado la primera vez.

**Si se publicó arrastrando la carpeta a Vercel:** hay que volver a arrastrarla
cada vez. La carpeta lista para arrastrar es `Escritorio\subir-a-vercel`, que es
una copia sin `originales/` — importante, porque al arrastrar se sube todo lo que
haya dentro, incluidas las carpetas que git ignora. Si editas `index.html` en la
carpeta del proyecto, cópialo a `subir-a-vercel` antes de arrastrar.

**Si se conectó un repositorio de GitHub:** cada cambio que se sube se publica
solo:

```bash
git add -A
git commit -m "Describe el cambio"
git push
```

La analítica de Vercel ya está enlazada en la página, pero hay que activarla una
vez en el panel del proyecto (Analytics > Enable). Mientras no esté activada, el
script no carga y la página funciona igual. No usa cookies ni datos personales,
así que no necesita aviso de consentimiento.
