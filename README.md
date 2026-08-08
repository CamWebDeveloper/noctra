# BLACK TITAN — Performance Club / E-commerce de Moda Urbana

Proyecto de portafolio: e-commerce premium de moda urbana, construido con **HTML, CSS y JavaScript puro** (sin frameworks ni dependencias de build). Diseño minimalista, lujoso y urbano — negro, blanco, gris y detalles plateados.

> ⚠️ Proyecto ficticio creado con fines de portafolio. Todos los pagos, productos y datos de usuario son simulados.

---

## 🚀 Cómo verlo

No requiere instalación ni compilación. Dos opciones:

1. **Directo:** abre `index.html` en cualquier navegador moderno.
2. **Con servidor local** (recomendado, evita restricciones de `fetch`/rutas en algunos navegadores):
   ```bash
   npx serve .
   # o
   python3 -m http.server 8000
   ```
   Luego visita `http://localhost:8000`.

---

## 🗂️ Estructura del proyecto

```
├── index.html          Portada principal
├── tienda.html          Catálogo con filtros, orden y búsqueda
├── producto.html         Detalle de producto (galería, zoom, reseñas)
├── carrito.html            Carrito + checkout (4 métodos de pago)
├── cuenta.html               Login / registro / pedidos / favoritos / direcciones
├── coleccion.html              Vista de una colección específica
├── promociones.html              Promociones activas
├── lista-espera.html               Contador regresivo + reserva de lanzamiento
├── blog.html                        Blog + panel de publicación
├── admin.html                        Panel de administración del dueño
├── 404.html                          Página de error personalizada
├── favicon.svg
├── css/
│   └── style.css        Sistema de diseño global (variables, componentes)
└── js/
    ├── data.js          Base de datos simulada (productos, blog, cupones...)
    ├── main.js          Header, carrito, favoritos, drawers, utilidades UI
    ├── tienda.js / producto.js / carrito.js / cuenta.js / ...
```

Cada página HTML carga `data.js` → `main.js` → su script específico, en ese orden.

---

## ✨ Funcionalidades implementadas

- **Catálogo:** filtros por categoría/talla/color, orden, búsqueda en vivo.
- **Producto:** galería con swipe táctil y zoom, selección de talla/color, reseñas (lectura + escritura), productos relacionados, notificación de reposición para agotados.
- **Carrito y checkout:** cupones, envío gratis automático, 4 métodos de pago simulados (Tarjeta, PayPal, Mercado Pago, Transferencia), historial de pedidos.
- **Cuenta:** login/registro simulado, pedidos, favoritos, direcciones.
- **Blog:** filtro por categoría, artículo en modal, formulario de publicación funcional.
- **Panel admin:** CRUD de productos (precio, stock, fotos, tallas, colores), control de promociones, vista de pedidos — todo se refleja en vivo en la tienda.
- **Persistencia:** todo el estado (carrito, favoritos, sesión, pedidos, contenido del admin) vive en `localStorage`, por lo que el sitio es completamente funcional sin backend.

---

## 🛠️ Decisiones técnicas

- **Sin frameworks:** HTML/CSS/JS puro, ideal para demostrar fundamentos sólidos.
- **Estado compartido vía `localStorage`:** simula una base de datos real sin necesidad de servidor.
- **`main.js` como capa común:** header, drawers de carrito/perfil y utilidades de UI se comparten entre todas las páginas para evitar duplicación.
- **Datos centralizados en `data.js`:** productos, colecciones, cupones, blog, testimonios, etc. en un único archivo fácil de editar.

---

## 📌 Roadmap (v2 — mejoras futuras, no bloqueantes)

- Lightbox de pantalla completa para el zoom de producto.
- Lógica real de promoción "2x1" aplicada en el carrito.
- Edición/eliminación de posts ya publicados desde el blog.
- Validación de tarjeta con algoritmo de Luhn.
- Backend real (o Supabase/Firebase) para reemplazar `localStorage`.
- Multi-usuario real en el panel de cuenta.

---

## 👤 Autor

Proyecto desarrollado como pieza de portafolio front-end.
