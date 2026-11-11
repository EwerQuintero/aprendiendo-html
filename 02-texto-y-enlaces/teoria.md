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
- **Saltar de `h1` a `h4`:** pendiente de probar.
- **Enlace con y sin `target="_blank"`:** pendiente de probar.
- **Enlace sin `https://`:** pendiente de probar.

## Lo que aprendí (hasta ahora)
- Los títulos dan estructura y van de `h1` a `h6`, sin saltarse niveles.
- `strong` y `em` se ven igual que `b` e `i`, pero significan más.
- `pre` respeta los espacios; `p` no.
- `sub` baja el texto y `sup` lo sube.

## Pendiente
- [ ] Cerrar experimentos (h1 a h4, enlace sin https, target="_blank")
- [ ] Ejercicio 2: enlaces
- [ ] Proyecto: artículo sobre Hollow Knight
- [ ] Completar "Lo que aprendí"