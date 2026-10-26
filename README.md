# Temario Técnico TIC UIB

Web estática con los 60 temas de la oposición a la **Escala de tècnics mitjans en TIC (subgrupo A2)** de la Universitat de les Illes Balears, según el anexo III de la convocatoria de 2024 (BOIB núm. 156, de 30/11/2024).

Para cada tema incluye:

- qué estudiar, con los artículos o subapartados clave;
- enlaces a la norma oficial (BOE, FOU de la UIB, EUR-Lex, RFC…) y a documentación técnica;
- notas sobre lo que suele preguntarse o puede cambiar;
- la normativa aplicable, en desplegables ordenados por rango (UE, ley orgánica, ley, real decreto, resoluciones, Illes Balears, UIB) y fecha, con qué mirar de cada norma y el enlace al texto consolidado.

También recoge el formato del examen, un simulador de méritos con el baremo del anexo IV, los resultados del proceso de 2024-2026 y exámenes de otras convocatorias para practicar.

Las normas estatales se comprobaron contra la API de legislación consolidada del BOE (todas vigentes a 26/10/2026) y los acuerdos de la UIB contra el FOU.

## Página de lectura

`lectura.html` muestra el temario como texto continuo para leer o imprimir: índice lateral, apuntes, texto literal de las normas y normativa de cada tema.

- `lectura.html`: los 60 temas.
- `lectura.html?parte=gen` o `?parte=tic`: solo una parte.
- `lectura.html?t=31`: un solo tema, con enlaces al anterior y al siguiente.

## Tests

`test.html` genera tests con preguntas de los temas que se elijan (707 preguntas de los 60 temas, con su explicación y la norma de referencia):

- **Práctica**: corrige cada pregunta al momento con la explicación.
- **Examen**: se corrige al final como en la oposición (cada error resta un tercio), con cronómetro opcional y paleta para revisar.
- Filtros: todas las preguntas, solo las no respondidas o solo las falladas; selección rápida de la parte general, la TIC, los temas marcados como estudiados o los puntos débiles.
- `test.html?t=5` o `test.html?temas=1,2,3` preseleccionan temas.
- Las estadísticas se guardan en el navegador.

## Estructura

- `index.html`: la web principal (temario, simulador de méritos, exámenes).
- `lectura.html`: la página de lectura.
- `data/datos.js`: datos compartidos (temas, normativa y su relación).
- `data/ley/tNN.json`: artículos literales de cada tema (BOE y FOU).
- `data/apuntes/tNN.html`: apuntes de los temas 19-60.
- `data/preguntas.json`: banco de preguntas tipo test (la opción correcta es siempre la primera; la página las baraja).

## Uso

No necesita compilación. Para verlo en local hay que servir la carpeta (por ejemplo `python3 -m http.server`), porque los textos se cargan con `fetch`.

Las marcas de «estudiado» se guardan en el `localStorage` del navegador, así que no pasan de un dispositivo a otro.

## Publicación

Se publica con GitHub Pages desde la rama `main` (carpeta raíz). Cada `git push` a `main` actualiza la web en uno o dos minutos.

## Aviso

El temario corresponde a la convocatoria de 2024. Cuando se publique la nueva convocatoria hay que comprobar si cambian los temas o la normativa.
