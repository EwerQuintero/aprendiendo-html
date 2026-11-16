# Módulo 03: Agrupar y listar

> Estado: en progreso.

## Agrupar contenido: div y span

### div (bloque)
Es una caja que agrupa varios elementos. No tiene significado ni aspecto propio: sirve para organizar y, más adelante, para darle estilo con CSS.

```html
<div>
  <h2>Título</h2>
  <p>Párrafo dentro de la caja.</p>
</div>
```

- Es un elemento **de bloque**: ocupa todo el ancho y empieza en una línea nueva.

### span (en línea)
Agrupa una parte de un texto, sin romper la línea.

```html
<p>Mi color favorito es <span>el azul</span>.</p>
```

- Es un elemento **en línea**: solo ocupa el espacio de su contenido.
- Solo es útil cuando le das estilo o un `class`/`id`. Solo, no cambia nada visualmente.

| | `div` | `span` |
|---|-------|--------|
| Tipo | Bloque | En línea |
| Se usa para | Agrupar secciones | Marcar un trozo de texto |
| Salta de línea | Sí | No |

## Atributos globales

Son atributos que se pueden poner en casi cualquier etiqueta.

```html
<p id="intro" class="destacado" style="color: blue;" title="Un párrafo">Hola</p>
```

- **`id`**: nombre **único** en la página. No se repite.
- **`class`**: nombre que **se puede repetir** en varios elementos. Un elemento puede tener varias clases separadas por espacio (`class="destacado grande"`).
- **`style`**: estilos CSS directos en el elemento (se ve a fondo en el módulo 04).
- **`title`**: texto que aparece al pasar el mouse.
- **`data-*`**: atributos propios para guardar datos (`data-nivel="3"`).

Regla simple: `id` es como la cédula (única), `class` es como un equipo (muchos pueden pertenecer).

## Listas

### Lista desordenada (ul)
Con viñetas. El orden no importa.

```html
<ul>
  <li>Manzana</li>
  <li>Pera</li>
</ul>
```

### Lista ordenada (ol)
Con números. El orden sí importa (pasos, rankings).

```html
<ol>
  <li>Primer paso</li>
  <li>Segundo paso</li>
</ol>
```

Atributos útiles de `ol`:

```html
<ol start="5">...</ol>       <!-- empieza en 5 -->
<ol reversed>...</ol>        <!-- cuenta hacia atrás -->
<ol type="A">...</ol>        <!-- A, B, C -->
```

### Listas anidadas
Una lista dentro de un `<li>`, nunca directamente dentro del `<ul>`.

```html
<ul>
  <li>Frutas
    <ul>
      <li>Manzana</li>
      <li>Pera</li>
    </ul>
  </li>
  <li>Verduras</li>
</ul>
```

### Lista de definiciones (dl)
Pares de término y descripción.

```html
<dl>
  <dt>HTML</dt>
  <dd>Lenguaje que da estructura a las páginas.</dd>
  <dt>CSS</dt>
  <dd>Lenguaje que les da estilo.</dd>
</dl>
```

- `dl`: la lista, `dt`: el término, `dd`: la descripción.

### Reglas importantes
- Dentro de `ul` y `ol` **solo van `li`**.
- Las listas **no van dentro de un `<p>`** (ya lo vimos con Prettier).
- Para anidar, la lista va dentro del `li`, no al lado.

## Citas y fuentes

```html
<blockquote cite="https://ejemplo.com">
  <p>Una cita larga, en su propio bloque.</p>
</blockquote>

<p>Como dijo alguien: <q>una cita corta en línea</q>.</p>

<p><cite>El nombre de una obra</cite> es un buen ejemplo.</p>
```

- `blockquote`: cita larga, en bloque (se ve con sangría).
- `q`: cita corta, en línea (el navegador agrega comillas).
- `cite`: el título de una obra o la fuente.

## Definiciones, abreviaturas y contacto

```html
<p><dfn>HTML</dfn> es un lenguaje de marcado.</p>

<p><abbr title="HyperText Markup Language">HTML</abbr></p>

<address>
  Escrito por Ewer<br>
  <a href="mailto:ejemplo@correo.com">ejemplo@correo.com</a>
</address>
```

- `dfn`: la palabra que estás definiendo.
- `abbr`: abreviatura; el `title` muestra su significado al pasar el mouse.
- `address`: datos de contacto de quien escribió la página.

## Cambios en el texto

```html
<p>Precio: <del>$50</del> <ins>$40</ins></p>
<p><s>Agotado</s></p>
```

- `del`: texto eliminado (tachado), indica un cambio.
- `ins`: texto añadido (subrayado).
- `s`: algo que ya no es correcto o relevante.

## Experimentos
- **div vs span:** los `div` se apilan uno debajo del otro (bloque). El
  `span` se queda dentro de la línea y por sí solo no cambia nada visual;
  sirve para marcar un trozo de texto y darle estilo con CSS después.
- **id repetido vs class repetida:** a la vista no cambian nada. El
  navegador no avisa si repito un `id`, pero es un error: el `id` debe ser
  único. La `class` sí se puede repetir.
- **div dentro de un `p`:** el `div` es de bloque y rompe la línea, partiendo
  la frase. Para marcar un trozo dentro de un texto se usa `span`.
- **div sin cerrar:** cada `</div>` cierra el `div` abierto más reciente,
  así que otro `div` no lo cierra. El navegador lo cierra solo al final y
  no avisa. Con CSS puede romper el diseño, así que siempre hay que cerrar.
- **ul vs ol:** ___
- **Lista dentro de un `p`:** ___
- **Lista anidada mal puesta:** ___
- **blockquote vs q:** ___
- **abbr con title:** ___
- **del e ins:** ___

## Lo que aprendí
- `div` es de bloque y `span` es en línea.
- `id` es único y `class` se puede repetir; el navegador no avisa si me
  equivoco.
- ___

## Pendiente
- [x] Ejercicio: div, span, id y class
- [ ] Ejercicio: listas
- [ ] Ejercicio: citas y cambios en el texto
- [ ] Proyecto: receta o top 10
- [ ] Completar "Lo que aprendí"