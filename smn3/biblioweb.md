# Prompt base de BiblioWeb

Este fue el prompt inicial usado para definir el prototipo estático. La paleta visual y las funciones se refinaron después en iteraciones con otras herramientas.

En el prompt original, `[paleta elegida]` era un marcador pendiente de definir. La propuesta visual se trabajó después y la paleta final fue café, roble y almendra.

```text
Actúa como un desarrollador web front-end. Antes de generar código,
hazme las preguntas que necesites para entender mejor el proyecto.

Proyecto: BiblioWeb, un sitio para una biblioteca con una parte pública
y un panel de administración.

Tecnologías obligatorias: HTML5, CSS, Bootstrap 5.3 (por CDN) y
JavaScript puro. No uses React, Tailwind, backend ni base de datos.

Páginas:
1. index.html: landing con carrusel de imágenes, servicios, horarios
   ficticios, y enlaces al catálogo y al login.
2. catalogo.html: cuadrícula de 6 tarjetas de libros (categorías
   Narrativa, Tecnología y Ciencia, con badge), cada una con portada y
   alt, título, autor, descripción y botón "Solicitar préstamo" que abre
   un modal con: nombre, correo, comentario opcional y checkbox de
   términos.
3. login.html: título "Acceso de administrador", correo, contraseña y
   botón "Ingresar". Cuenta de prueba: admin@biblioweb.test / Admin123.
   Si es incorrecta, mostrar "Correo o contraseña incorrectos".
4. admin.html: formulario (título, autor, portada URL, descripción,
   categoría en select, botones Guardar y Cancelar), tabla estática de
   libros con botones Editar y Eliminar visuales, y tabla de "Solicitudes
   recibidas" (ID, libro, solicitante, correo, comentario, estado
   Pendiente).

JavaScript solo para:
- Login con sessionStorage y redirección a admin.html.
- Protección de admin.html (si no hay sesión, redirige a login.html).
- Botón "Cerrar sesión" que borra la sesión y lleva a index.html.
- Selector de tema claro/oscuro con data-bs-theme de Bootstrap 5.3,
  presente en la navbar de todas las páginas.

Todo lo demás (libros, solicitudes, botones de editar/eliminar) debe ser
HTML estático, sin arreglos de JS ni localStorage.

Diseño: responsivo, limpio, con esta paleta: [paleta elegida].
Estructura de archivos: index.html, catalogo.html, login.html,
admin.html, css/base.css, js/auth.js, js/tema.js.
```
