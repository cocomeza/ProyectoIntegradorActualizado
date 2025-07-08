# 🛒 E-commerce COCOSHOP

Este es un proyecto de tienda virtual desarrollado con **HTML, CSS y JavaScript puro**, en el cual se pueden visualizar productos por categoría, agregarlos al carrito de compras, eliminarlos y realizar acciones básicas como guardar la información en `localStorage`.

---

## 🧱 Funcionalidades principales

- Mostrar productos en el DOM desde un array local.
- Filtrar productos por categorías.
- Agregar y eliminar productos del carrito.
- Calcular cantidad total de productos.
- Persistir el carrito en `localStorage`.
- Vista de carrito con acciones dinámicas.

---

## 🛠️ Lógica implementada

### 📦 Creación de productos

- Se definió un **array de productos**, donde cada producto es un objeto con propiedades:
  - `id`, `titulo`, `imagen`, `categoria` (con su propio `id`), `precio`, etc.
- Las **imágenes** fueron cargadas mediante links generados desde [postimg.cc](https://postimg.cc/) en lugar de alojarlas localmente.

---

### 🧩 Mostrar productos

- Se obtuvo el `div` contenedor de productos mediante `getElementById`.
- Se creó una función `cargarProductos` que recorre el array con `forEach`.
- Por cada producto se crea un `div` con la clase `producto` y se inserta el contenido con `innerHTML`.
- Luego se hace un `appendChild` al contenedor principal y se llama a la función para mostrar todo.

---

### 🧰 Botones de categorías

- Se definieron `botonesCategoria` con un `id` en el HTML.
- En JS se hizo un `forEach` con `addEventListener` para detectar clics y filtrar productos usando el método `filter` según la categoría seleccionada.

---

### 🛒 Agregar al carrito

- Se creó un `let botonesAgregar` y una función `actualizarBotonesAgregar`.
- Se agregó un `addEventListener` a cada botón con la función `agregarAlCarrito`.
- Se creó `productosEnCarrito` como array vacío para almacenar los productos agregados.
- En `agregarAlCarrito` se usa:
  - `findIndex` para buscar si ya existe,
  - `some` para verificar si está en el carrito,
  - y `push` para agregar si es nuevo.
- Se asigna y actualiza la propiedad `cantidad`.

---

### 🔢 Numerito del carrito

- Se definió una variable `numerito` para mostrar la cantidad total.
- Se usó `reduce` para acumular la cantidad de productos.
- Se actualiza automáticamente al agregar o quitar productos.

---

### 💾 Persistencia

- Se utilizó `localStorage.setItem('productosEnCarrito', JSON.stringify(productosEnCarrito))` para guardar los datos.
- En la página del carrito, se parsean los datos con `JSON.parse`.

---

## 🛍️ Página del carrito

- Archivo: `carrito.html` y `carrito.js`
- Se obtienen elementos como:
  - `contenedorCarritoVacio`
  - `contenedorProductos`
  - `contenedorCarritoAcciones`
  - `contenedorCarritoComprado`
- Se recorre `productosEnCarrito` con `forEach` para mostrar cada producto en el carrito.
- Se creó una función `botonesEliminar` para eliminar productos desde el carrito.

---

## 📁 Archivos importantes

```
COCOSHOP/
├── index.html
├── carrito.html
├── js/
│   ├── main.js
│   └── carrito.js
├── css/
│   └── estilos.css
└── README.md
```















