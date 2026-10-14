# Página de Sebastián Carvallo Campos

Landing de marca personal para las asesorías de empleabilidad. Es una sola
página, en un solo archivo: `index.html` tiene el texto, los estilos y todo lo
demás. No hay que compilar nada ni instalar nada.

## Dónde está publicado

| Dónde | Enlace |
|---|---|
| Sitio | https://marcasc.vercel.app |
| Código | https://github.com/Flaquillo0/marca-personal |
| LinkedIn | pendiente |
| Instagram | pendiente |

La dirección anterior, `subir-a-vercel-ashen.vercel.app`, sigue funcionando:
Vercel conserva los dominios viejos como alias al renombrar un proyecto. No
hace falta hacer nada con ella, pero la que va escrita en las metaetiquetas y
la que conviene compartir es `marcasc.vercel.app`.

Conviene revisar esta tabla cada cierto tiempo para que no queden enlaces
muertos apuntando a la página.

## Si cambia el dominio

Los cuatro lugares que lo tienen escrito son `og:url`, `og:image`,
`twitter:image` y `canonical`, entre las líneas 14 y 21 del `index.html`. Son
los que hacen que, al compartir el enlace por WhatsApp, aparezca la miniatura
con la foto y el nombre. Se reemplazan los cuatro, con `https://` y sin barra
al final.

Después de cambiarlos, manda el enlace por WhatsApp a alguien una vez para
comprobar que la miniatura aparece. WhatsApp cachea las miniaturas, así que si
el enlace ya se compartió antes puede seguir mostrando la vieja un rato.

## Cómo se cambia el número de WhatsApp

El número está escrito varias veces en `index.html` (en cada botón de WhatsApp
y en el script del final), siempre con el mismo formato: `56936108624` (código
de país, sin el signo + y sin espacios). Busca esa cadena y reemplázala en todas.

El enlace lleva un mensaje ya escrito, para que quien te escriba llegue
diciendo de dónde viene. Si quieres cambiar ese texto, está en la misma línea,
después de `?text=`, con los espacios escritos como `%20` y los acentos en
código (`á` es `%C3%A1`).

## Cómo se cambia el correo

Aparece varias veces como `sebastian.carvallo@outlook.com` (botones de correo,
datos estructurados y pie). Busca esa cadena y reemplázala en todas.

## Cómo se cambia la foto

La foto de la portada es `fotos/sebastian.jpg`, cuadrada, de 900 × 900 píxeles.
Si la reemplazas, mantén el formato cuadrado y el mismo nombre de archivo.

`fotos/og-image.jpg` es la miniatura que se ve al compartir el enlace: 1200 ×
630, con la foto a la derecha y tu nombre a la izquierda. Si cambias la foto de
portada, hay que rehacer también esta.

El original sin comprimir está en `originales/`, que **no se publica** (está en
el `.gitignore`). Todo lo que pongas en esa carpeta queda fuera del sitio.

## Dónde están los textos

Todos dentro de `index.html`, en orden de aparición. El diseño sigue el de
somosempleables.com (portada centrada con pregunta, bloque "sobre mí" con foto,
servicios en tarjetas, bloque oscuro de cifras, cierre en degradado y pie
oscuro), con contenido propio.

**Pestaña "Para candidatos"**

1. Portada: etiqueta, la pregunta grande, párrafo de entrada y dos botones.
2. "Sobre mí" (`#nosotros`): foto, trayectoria y enlace a LinkedIn.
3. Servicios (`#servicios`): cuatro tarjetas (los tres packs y la
   autoevaluación gratis), cada una con su lista corta.
4. La autoevaluación destacada, con la imagen del informe.
5. "Empezamos con quince minutos" (`#como-funciona`): los cuatro pasos.
6. Testimonios en video: comentado (ver "Qué falta").
7. Bloque oscuro de cifras (`#trayectoria`). Sólo datos que se pueden
   respaldar; no agregar números de clientes o seguidores que no estén medidos.
8. Preguntas frecuentes, incluida la de por qué no hay precios.
9. Base de candidatos y el llamado final en degradado.

**Pestaña "Para empresas"**: portada, bloque oscuro del problema, autoprueba,
cómo trabajo, por qué a mí y contacto.

## Decisiones que conviene no "arreglar"

**No hay precios en la página, y es a propósito.** La estrategia es evaluar al
cliente en la llamada de diagnóstico y recién ahí cotizar, distinto según esté
en Chile o fuera. Publicar las cifras rompe eso: el visitante compara en frío y
no llama. La sección "Tres formas de trabajar juntos" explica el motivo en voz
propia, que es lo que evita que la ausencia de precio se lea como algo turbio.

**Lo que queda en desplegables, y por qué.** Las tarjetas de servicios
muestran una lista corta, de una línea por punto, como en el sitio de
referencia. Lo largo (por qué no hay precios, qué es un ATS, etc.) vive en las
preguntas frecuentes, dentro de `<details>`. El texto que da credibilidad es
el mismo que hace que el visitante se vaya antes de escribir: si hay que sumar
contenido, va a una pregunta frecuente, no a la vista.

**El favicon es un monograma, no un logo.** No hay identidad visual todavía, así
que `fotos/favicon.png` es un cuadrado azul marino con las iniciales. Cuando
exista un logo de verdad, se reemplaza ese archivo manteniendo el nombre.

**LinkedIn va antes que el currículum en "Ganando al algoritmo", y es a propósito.**
En Google Trends (Chile, cinco años) las búsquedas de "curriculum" cayeron de 33
a 20 y las de "linkedin" subieron de 36 a 69. El activo que la gente está
trabajando hoy es el perfil, no el documento. Si algún día se reordena esa
lista, que sea porque los datos cambiaron, no por costumbre.

**La sigla ATS está escrita en el texto, no sólo los nombres de los sistemas.**
"cv ats" no registraba búsquedas en Chile durante 2025 y en 2026 aparece todos
los meses; "curriculum ats" sube 70 % en doce meses, y 60 % en España. Es la
palabra con la que la gente está empezando a nombrar el problema, y es
exactamente la credencial más fuerte de la página. Conviene que aparezca.

**El servicio de entrevista parte por "debilidades", no por "STAR".**
En el grupo de búsquedas de "entrevista de trabajo", cuatro de las seis primeras
son sobre debilidades. "Entrevista por competencias" y "metodología STAR" no
registran búsquedas: son el vocabulario del que evalúa, no el del que postula.
STAR sigue en la página como respaldo metodológico, después del gancho.

**El título dice "CV para ATS, LinkedIn y entrevistas", no "asesorías de
empleabilidad".** Nadie busca lo segundo: "asesoría laboral" y "coach laboral"
están bajo el umbral de medición de Google en Chile, doce meses casi enteros en
cero. Además, "currículum" a secas compite en Chile con el currículo escolar
("curriculum nacional", "curriculum mineduc"), así que en los textos de posicionamiento
conviene usar "CV" con calificador.

**Colores y tipografía.** Fondo blanco, azul `#1A5CFF` con degradado a
morado `#7C3AED` y azul casi negro `#0F172A` para los bloques oscuros y el pie,
tomados del sitio de referencia. La tipografía es Outfit (Google Fonts). Todos
los colores están como variables al inicio del `<style>`, con su versión para
modo oscuro.

## Qué falta

- **Testimonios.** En `index.html`, después de "Empezamos con quince minutos",
  hay una sección de cuatro videos dentro de un comentario HTML (el comentario
  explica dónde dejar los archivos). Está
  comentado a propósito: así no se ve mientras no haya testimonios de verdad.
  Cuando tengas dos o tres, con nombre, cargo y resultado concreto, sácalos del
  comentario. No los inventes: en una página de asesoría profesional un
  testimonio falso destruye exactamente la confianza que construye el resto del
  texto.
- **Dominio propio.** Mientras no lo haya, la miniatura al compartir no va a
  funcionar.

## La base de candidatos

La página `/base` (archivo `base.html`) tiene un formulario propio —no es un
formulario de Google incrustado— que escribe en la planilla **"Base de
candidatos — Sebastián Carvallo"** en Google Drive.

La cadena es: formulario en `base.html` → aplicación web de Apps Script →
planilla. El código del script está en `notas/formulario-apps-script.js`, que no
se publica. Si alguna vez hay que reimplementarlo, la dirección nueva se pega en
la variable `ENDPOINT`, al final de `base.html`.

**Dos cosas que hay que mantener así**, porque ya fallaron una vez:

- En Apps Script, la implementación debe tener "quién tiene acceso" en
  **Cualquier usuario**. Si pide iniciar sesión, el formulario dice "quedaste
  registrado" y no guarda nada: falla en silencio, que es lo peor que puede
  pasar acá. Para comprobarlo, abre la dirección del script en el navegador:
  tiene que responder "El formulario está activo."
- En la planilla, las **columnas B a N** tienen que estar en formato *texto sin
  formato*. Si no, un teléfono escrito como `+56 9 ...` se guarda como `#ERROR!`
  porque Sheets lo toma por una fórmula.

Las dos casillas de consentimiento del formulario son preguntas separadas a
propósito, y la segunda —presentar el perfil a empresas— es opcional y va
desmarcada. Eso no es un detalle de diseño: es lo que hace que la base sea
usable legalmente. No las juntes en una sola.

La planilla no se comparte con nadie, ni en modo lectura. Cuando una empresa
pide candidatos, se le mandan los perfiles que correspondan, nunca el acceso.

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
