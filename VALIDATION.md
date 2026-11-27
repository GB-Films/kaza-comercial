# Verificación

Fecha: 2026-11-27.
Repositorio creado: https://github.com/GB-Films/kaza-comercial (público, nuevo y separado).

- JavaScript válido: `node --check dist/app.js`.
- Los tres archivos de frontend son idénticos a la base comercial de origen.
- Las rutas de CSS y JavaScript son relativas, compatibles con una subruta de Pages.
- Revisión estática: sin endpoints externos, enlaces de contacto, llamadas de red, almacenamiento del navegador ni cobros.
- El workflow publica solo `dist` por ejecución manual en `main`.
- Pendiente: ejecutar el workflow y verificar su URL efectiva desde el navegador, incluyendo formularios y vista móvil.

El conector GitHub ve el nuevo repositorio con permisos de lectura, sin escritura; la carga inicial usa la sesión del titular en el navegador. No se accedió al proyecto del casamiento real.
