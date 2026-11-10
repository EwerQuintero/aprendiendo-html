# Módulo 01: Primeros pasos

## Etiquetas (tags)
HTML funciona con etiquetas que abren y cierran:

```html
<p>Hola, soy un párrafo</p>
```

- `<p>` abre y `</p>` cierra (lleva `/`).
- Lo de en medio es el **contenido**.
- Todo el conjunto se llama **elemento**.

## Atributos
Información extra dentro de la etiqueta de apertura:

```html
<a href="https://google.com">Ir a Google</a>
```

`href` es el atributo y lo que va entre comillas es su valor.

## Comentarios
Notas para mí que el navegador ignora:

```html
<!-- Esto no se ve en la página -->
```

## Espacios en blanco
El navegador junta varios espacios y saltos de línea en uno solo.
Para un salto real se usa la etiqueta `<br>`.

## Mayúsculas
HTML no distingue entre `<P>` y `<p>`, pero se escribe en minúscula
por costumbre y estándar.

## Esqueleto de toda página

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8">
    <title>Título de la pestaña</title>
  </head>
  <body>
    <!-- Aquí va lo que se ve -->
  </body>
</html>
```

- `<!DOCTYPE html>`: le dice al navegador que es HTML moderno.
- `<html>`: envuelve todo el documento.
- `<head>`: información invisible (título de pestaña, codificación).
- `<meta charset="UTF-8">`: hace que las tildes y la ñ se vean bien.
- `<body>`: todo lo que se ve en la página.

## Experimentos (rompiendo cosas)
- **Borrar el `</h1>`:** todo lo que venía después se convirtió en título
  (grande y en negrita), porque el navegador nunca encontró dónde terminaba.
  HTML no avisa con errores, así que hay que cerrar siempre las etiquetas.
- **Quitar `meta charset`:** las tildes y la ñ se vieron bien igual, porque
  Live Server/el navegador adivina UTF-8, pero no hay que depender de eso.
  `lang="es"` solo indica el idioma, no la codificación.
- **Muchos saltos de línea en un `<p>`:** el navegador los junta en uno solo.
  Para un salto real se usa la etiqueta `<br>`, no un atributo.
- **Escribir `<H1>` en mayúscula:** funciona igual; se escribe en minúscula
  por estándar y legibilidad.

## Lo que aprendí
- HTML no marca errores: el navegador intenta adivinar, por eso hay que
  escribir el código con cuidado.
- Siempre cerrar las etiquetas y poner `DOCTYPE` y `meta charset`.