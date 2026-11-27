# Verificación de la primera publicación

Fecha: 2026-11-27.

- Sitio efectivo: https://gb-films.github.io/kaza-comercial/
- Repositorio nuevo y separado: https://github.com/GB-Films/kaza-comercial
- Versión desplegada: `e8028b6f8eb86e999a5423c08cedad856f9b36c0`.
- Ejecución manual exitosa: https://github.com/GB-Films/kaza-comercial/actions/runs/46029942617
- Los trabajos `build` y `deploy` finalizaron correctamente. El registro de deploy devolvió la URL anterior y `Reported success!`.

## Pruebas desde el enlace público

Realizadas en Chrome, abriendo la URL efectiva de GitHub Pages:

- Carga de la portada, textos con acentos, ilustración y estilos.
- Navegación desde “Ver demo” hasta la demo ficticia.
- Asistencia: “No puedo ir” devuelve “Respuesta de prueba: No puedo ir. No se guardó.”.
- Mesas: “Sofía de ejemplo” devuelve “Mesa 3 · Jardín”.
- Regalos: muestra ejemplos y “No hay pagos habilitados en esta demo”.
- Consulta: con “Pareja de prueba KAZA”, fecha vacía y funciones predeterminadas, genera el texto con “Fecha estimada: por definir” e “Invitación digital, Confirmaciones”.
- Copiar consulta: el sitio devuelve “Consulta copiada.” en HTTPS.
- Vista móvil emulada a 400 × 824: portada, navegación y tarjeta de asistencia legibles, en una columna y sin recortes horizontales visibles.

## Comprobaciones del paquete

- `node --check dist/app.js` correcto.
- Los tres archivos del frontend remoto coinciden con la base comercial original. Se conservan las rutas relativas de CSS y JavaScript.
- Revisión estática: sin endpoints externos, contactos inventados, llamadas de red, almacenamiento del navegador ni cobros.
- El árbol remoto contiene exclusivamente el frontend ficticio, su workflow y documentación comercial; no contiene `.openai/` ni archivos de hosting anteriores.
- El workflow solo se ejecuta manualmente en `main` y solo publica `dist/`. Separar `build` y `deploy` resolvió el error de descubrimiento del artefacto de la primera ejecución.

## Límites y acceso para futuros cambios

No se probó en un teléfono físico, Safari o Firefox; la comprobación móvil fue emulación de Chrome. No hay backend ni pruebas de envío o cobro: esas funciones no están habilitadas.

La carga y configuración iniciales se hicieron con la sesión de GB-Films del titular en el navegador. Git devolvió 403 a `guidoboetsch` al intentar subir `main` a este repositorio; el conector conectado también tiene solo lectura. No se modificaron credenciales ni permisos. Antes de próximos pushes/PR se debe verificar un canal de escritura autorizado para este repo. No reintentar el push rechazado sin verificar ese acceso.

El proyecto del casamiento real quedó fuera del alcance y no fue accedido ni modificado. Los cambios futuros se entregan en borrador/PR y no se fusionan ni publican sin dirección explícita.
