# Temario Técnico TIC UIB

Este repositorio contiene una web protegida. Todo su contenido está cifrado (AES-256-GCM) y solo se
muestra tras introducir la contraseña de acceso en el navegador.

- `index.html`, `lectura.html` y `test.html`: pantalla de acceso que descifra y muestra cada página.
- `e/`: ficheros cifrados.

El código en claro no está en este repositorio. Para regenerar la versión cifrada se usa el script
`xifra.py`, que pide la contraseña al ejecutarse y no la guarda en ningún sitio.
