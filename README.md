# App de Ecommerce de Ropa

Proyecto web de comercio electronico para una tienda de ropa, construido con **HTML5 + CSS3 vanilla** (sin frameworks ni librerias JS).

Incluye:
- Home con buscador, categorias, tarjetas de producto y navbar responsive.
- Paginas de detalle por producto con selector de cantidad/talla/color y modal de descripcion.
- Checkout con carrito, control de cantidades, metodos de pago, resumen de compra y modal de confirmacion.

## Tecnologias
- HTML5
- CSS3 (responsive con media queries)
- Navegacion y modales sin JavaScript (usando `:target` y `input:checked`)

## Estructura del proyecto
```text
Proyectos HTML/
├── CSS/
│   ├── variables.css
│   ├── style.css
│   ├── detail.css
│   └── checkout.css
├── storage/
│   ├── font/
│   │   └── encode_sans/
│   └── img/
│       ├── Botón_Carro.png
│       ├── Botón_Pago.png
│       ├── Dav.png
│       ├── Estilo_Clasico.png
│       ├── Estilo_Gorrito.png
│       ├── Estilo_Negro.png
│       ├── Estilo_Urbano.png
│       └── Screen 1.png, Screen 2.png, Screen 3.png
├── views/
│   ├── detail.html
│   ├── detail-urban.html
│   ├── detail-black.html
│   ├── detail-relaxed.html
│   └── checkout.html
└── index.html
```

## Paginas y funcionalidades

### 1) Home (`index.html`)
- Navbar superior fija (desktop + hamburguesa en mobile).
- Opciones del navbar: Home, About, Category, Menu, Testimonial, Contact.
- Contact abre un modal con numeros de contacto y se cierra al hacer click fuera o en `Cerrar`.
- Bienvenida personalizada con nombre y foto de perfil (`storage/img/Dav.png`).
- Buscador visual de productos.
- Filtro visual de categorias.
- Grid de productos con:
  - Imagen
  - Boton de favorito
  - Titulo
  - Categoria
  - Precio
  - Rating
  - Enlace a pagina de detalle
- Bottom nav mobile: Home, Cart, Favorites, Profile.

### 2) Detalle de producto (`views/detail*.html`)
Paginas incluidas:
- `detail.html` (Classic Linen Set)
- `detail-urban.html` (Urban Hat Combo)
- `detail-black.html` (Black Street Style)
- `detail-relaxed.html` (Relaxed City Fit)

Cada pagina tiene:
- Boton `Atras`.
- Boton/estado `Anadir a favoritos`.
- Imagen principal del producto.
- Informacion:
  - Titulo
  - Calificacion
  - Numero de vistas
  - Selector de cantidad (por defecto 1)
- Boton `Ver mas` que abre modal de descripcion completa.
- Personalizacion:
  - Talla (S, M, L)
  - Color
- Boton `Comprar` con icono (`Botón_Carro.png`) enlazado a `views/checkout.html`.
- Total dinamico segun cantidad seleccionada (solo HTML/CSS).

### 3) Checkout (`views/checkout.html`)
- Header con `Back`, titulo `Checkout` y boton de menu.
- Tarjetas de carrito con:
  - Imagen
  - Titulo
  - Categoria
  - Precio
  - Control de cantidad con `-` y `+`
- Seccion `Informacion de Envio y Pago`:
  - Metodo de pago (Tarjeta de Credito / Tarjeta de Debito)
  - Direccion de envio
- Seccion `Resumen de Compra`:
  - Total de productos seleccionados
  - Precio total de productos
  - Costo de envio
  - Descuentos
  - Subtotal
- Boton `Pagar` con icono (`Botón_Pago.png`) que abre modal de confirmacion.

## Sistema de estilos

### `CSS/variables.css`
Contiene variables globales de:
- Colores
- Tipografia
- Radios
- Sombras
- Breakpoints

### `CSS/style.css`
Estilos globales:
- Layout base
- Navbar
- Home
- Tarjetas de producto
- Bottom nav mobile
- Modal de contacto

### `CSS/detail.css`
Estilos especificos de las paginas de detalle:
- Hero de producto
- Bloques de informacion
- Selectores (cantidad, talla, color)
- Boton de compra
- Modal de descripcion

### `CSS/checkout.css`
Estilos especificos de checkout:
- Cart items
- Control de cantidades
- Panel de envio/pago
- Resumen
- Modal de confirmacion

## Como ejecutar el proyecto
Como es un proyecto estatico, puedes abrir `index.html` directamente en tu navegador.

Opcionalmente, puedes usar una extension como **Live Server** en VS Code para desarrollo.

## Flujo recomendado de navegacion
1. Abrir `index.html`.
2. Elegir un producto y entrar con `View detail`.
3. Ajustar cantidad/talla/color y hacer click en `Comprar`.
4. Revisar carrito en `checkout.html` y completar con `Pagar`.

## Publicacion en GitHub
Comandos basicos:

```bash
git init
git add .
git commit -m "Proyecto ecommerce ropa"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
git push -u origin main
```

Si te rechaza el push porque el remoto tiene cambios:

```bash
git pull --rebase origin main
git push -u origin main
```

## Autor
Proyecto desarrollado por David (configurado en la interfaz como `David Fabian`).
