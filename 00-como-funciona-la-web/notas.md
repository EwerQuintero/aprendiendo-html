# Cómo funciona la web

## Mi analogía
Es como pedir una pizza a domicilio: yo hago el pedido, alguien busca
la dirección de la pizzería, y la pizzería me manda la comida.

## Conceptos
- **Navegador:** el programa (Chrome) que pide las páginas y las dibuja en mi pantalla.
- **Dominio:** el nombre fácil de recordar de una web, como `amazon.com`.
- **DNS:** una especie de agenda que convierte el dominio en la dirección real (IP) del servidor.
- **Hosting:** el computador siempre encendido donde viven los archivos de una web.
- **HTTP/HTTPS:** el idioma con el que el navegador y el servidor se hablan. HTTPS es la versión segura (el candadito).
- **SEO:** trucos para que Google entienda mi página y la muestre en los resultados.

## El recorrido
1. Escribo un dominio en Chrome.
2. Chrome le pregunta al DNS cuál es la IP.
3. Chrome le manda una petición HTTP al servidor.
4. El servidor responde con el HTML, CSS, JS e imágenes.
5. Chrome lo dibuja en pantalla.

## Experimento con DevTools (Amazon)
Abrí Amazon, presioné F12, entré a la pestaña Network y recargué con F5.
- Peticiones totales: 114
- Peso transferido: 1.1 MB (10.4 MB de recursos en total)
- Tiempo en terminar de cargar: 7.14 segundos
- Primer archivo: el HTML, con Status 200 (todo bien).
- Lo que más me sorprendió: que una sola página haga 114 peticiones, y que muchas sean imágenes y "pings" que ni se ven.

## Reto bonus: nslookup
Ejecuté `nslookup google.com` y el DNS (8.8.8.8) me devolvió varias
direcciones: varias IPv6 y una IPv4 (142.251.132.174). Google tiene muchos
servidores, y el DNS me da varias direcciones para repartir la carga y
tener respaldo si una falla.