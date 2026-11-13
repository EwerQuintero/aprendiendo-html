# Módulo 02: Texto y enlaces

> Estado: en progreso.

## Títulos (h1 a h6)
Hay seis niveles, de `<h1>` (el más importante) a `<h6>` (el menos importante).

```html
<h1>Título principal</h1>
<h2>Sección</h2>
<h3>Subsección</h3>
```

- Normalmente se usa **un solo `<h1>`** por página.
- No se saltan niveles (de `h2` no se pasa a `h4`).
- Los títulos sirven para dar **estructura**, no para hacer el texto grande. Para eso está CSS.

## Párrafos
`<p>` es un bloque de texto. El navegador deja un espacio antes y después.

## Negrita y cursiva
```html
<strong>Importante</strong>   <!-- negrita, con significado de importancia -->
<b>Negrita</b>                <!-- negrita solo visual -->
<em>Énfasis</em>              <!-- cursiva, con significado de énfasis -->
<i>Cursiva</i>                <!-- cursiva solo visual (términos, pensamientos) -->
```

La diferencia: `strong` y `em` **dicen algo sobre el contenido** (importancia, énfasis), y los lectores de pantalla lo notan. `b` e `i` solo cambian el aspecto. Se prefiere `strong` y `em`.

## Resaltado
```html
<mark>texto resaltado</mark>
```

## Subíndices y superíndices
```html
H<sub>2</sub>O
x<sup>2</sup>
```

## Texto preformateado
`<pre>` respeta los espacios y saltos de línea tal como los escribo. Útil para código o poemas.

```html
<pre>
  Línea 1
      Línea 2 con sangría
</pre>
```

## Saltos y líneas divisorias
- `<br>`: salto de línea dentro de un texto (no se cierra).
- `<hr>`: línea horizontal que separa secciones (no se cierra).

## Enlaces
Se crean con la etiqueta `<a>` y el atributo `href`:

```html
<a href="https://www.google.com">Ir a Google</a>
```

**Tipos de enlace:**

```html
<!-- Externo: a otra web -->
<a href="https://es.wikipedia.org">Wikipedia</a>

<!-- Interno: a otra página de mi proyecto -->
<a href="otra-pagina.html">Otra página</a>

<!-- Correo -->
<a href="mailto:micorreo@ejemplo.com">Escríbeme</a>

<!-- Abrir en pestaña nueva -->
<a href="https://google.com" target="_blank" rel="noopener noreferrer">Google</a>
```

- `href` es la dirección a la que lleva el enlace.
- `target="_blank"` abre en una pestaña nueva.
- `rel="noopener noreferrer"` se agrega junto a `_blank` por seguridad.
- Para ir a otra web hay que escribir la dirección completa, con `https://`.

## Experimentos
- **Tamaño de los títulos:** van decreciendo de `h1` (el más grande) a `h6`
  (el más pequeño).
- **`<strong>` vs `<b>` y `<em>` vs `<i>`:** se ven exactamente iguales.
  `strong` y `b` dan negrita; `em` e `i` dan cursiva. La diferencia es el
  significado: `strong` y `em` indican importancia o énfasis, y los lectores
  de pantalla lo notan.
- **`<pre>` vs `<p>`:** `pre` respeta los espacios y los saltos de línea tal
  como los escribo; `p` los junta en uno solo.
- **`<sub>` y `<sup>`:** `sub` pone el texto abajo (H₂O) y `sup` arriba (x²).
- **Borrar la etiqueta de apertura de un título:** el texto pierde el tamaño
  y la negrita propios del título y se ve como texto normal.
- **Saltar de `h1` a `h4`:** cada título se ve según su propio nivel y el
  navegador no avisa de nada. Saltarse niveles es mala práctica porque
  desordena la estructura (afecta a los lectores de pantalla).
- **Título sin cerrar:** si después viene otro título, el navegador cierra
  el anterior solo. Pero si viene un `<p>`, el texto sigue siendo título.
  Por eso hay que cerrar siempre las etiquetas.
- **Enlace sin `https://`:** el navegador lo toma como una ruta dentro de
  mi proyecto y sale "Cannot GET". Para ir a otra web hay que poner la
  dirección completa.
- **Enlace con y sin `target="_blank"`:** sin `target`, el enlace se abre
  en la misma pestaña (se vuelve con la flecha atrás). Con
  `target="_blank"` se abre en una pestaña nueva y mi página queda abierta.
- **Enlace interno:** `href="archivo.html"` busca el archivo en la misma
  carpeta de la página actual. Funciona porque el archivo existe en mi
  proyecto.
- **Enlace `mailto:`:** abre el programa de correo del computador (Outlook,
  etc.) con el destinatario ya escrito.

## Lo que aprendí (hasta ahora)
- Los títulos dan estructura y van de `h1` a `h6`, sin saltarse niveles.
- `strong` y `em` se ven igual que `b` e `i`, pero significan más.
- `pre` respeta los espacios; `p` no.
- `sub` baja el texto y `sup` lo sube.
- El navegador no avisa de errores: a veces adivina bien (un título sin
  cerrar seguido de otro título) y a veces no (seguido de un `<p>`).
- Un enlace externo necesita `https://`, si no, se busca dentro de mi proyecto.
- Hay enlaces externos, internos y de correo, y `target="_blank"` controla
  si se abren en otra pestaña.

## Pendiente
- [x] Probar `target="_blank"` (ejercicio de enlaces)
- [ ] Ejercicio `04-poema.html` (`pre`, `br`, `hr`)
- [ ] Proyecto: artículo sobre Hollow Knight
- [ ] Completar "Lo que aprendí" al terminar el módulo