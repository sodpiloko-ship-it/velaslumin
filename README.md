# velaslumin.com — Lumin Candele (sitio estático)

Tienda estática de **Lumin Candele** (velas aromáticas artesanales, madre e hijo, inspiradas en Italia).
Un `index.html` **self-contained** (0 dependencias): Inicio, Tienda, Producto, Carrito, Pago, Colecciones,
Nuestra historia. Carrito en `localStorage`. Pensado para **GitHub → Hostinger**.

```
index.html · favicon.svg · robots.txt · sitemap.xml
img/   ← fotos reales (ver img/COMO-AGREGAR-FOTOS.md)
.github/workflows/deploy.yml   ← auto-deploy a Hostinger por FTP
```

## ⚠️ ANTES DE NADA — la tienda actual está VIVA y VENDIENDO
velaslumin.com hoy corre una **tienda WooCommerce (WordPress) real, con pedidos**. Pushear a este repo de
GitHub es **seguro** (no toca el sitio). Lo que **NO** debes hacer todavía:
- **No** conectes este repo al `public_html` de velaslumin.com, ni apuntes el dominio aquí —
  **sobreescribiría la tienda viva** (productos, carrito, pedidos, SEO).

**Migración segura (recomendada):**
1. Resolver **comercio** en el sitio nuevo: Stripe (Payment Links/Checkout) o cierre por WhatsApp (ya incluido).
2. Bajar el **inventario de URLs** de la tienda actual y preparar **301** origen→destino (no perder SEO).
3. Desplegar primero a un **subdominio/carpeta de PRUEBA** (ej. `nuevo.velaslumin.com`) y revisar.
4. **Cutover** (apuntar el dominio) solo cuando esté probado y con tu OK.

## Deploy (cuando toque el cutover)
- **A · Git nativo de Hostinger:** hPanel → Avanzado → GIT → URL del repo, rama `main`, directorio = el
  public_html destino. Webhook en GitHub para auto-deploy.
- **B · Actions por FTP:** agrega `FTP_SERVER`/`FTP_USERNAME`/`FTP_PASSWORD` (el workflow ya está listo).

## Pendiente
- **Fotos reales** de las velas (ver `img/COMO-AGREGAR-FOTOS.md`). Hoy: ilustración de respaldo.
- **Precio de Wax Melts** y nombres de **aromas** (hoy: el cliente escribe su aroma; se confirma por WhatsApp).
- **Stripe** para cobrar en línea.
