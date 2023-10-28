
E-commerce COCOSHOP

En el js lo primero que hice es crear un array de productos.
Abri un objeto y le puse un "id" a cada producto y las caracteristicas como titulo,img,categoria,precio,etc.
IMPORTANTE (A las categorias le puse un "id").
Las imagenes en vez de subirla a una carpeta le genere un link de cada imagen a traves de esta pagina https://postimg.cc/.

Cree una constante con el nombre contenedorProductos y (lo traje a traves de un id).
luego cree una funcion cuyo nombre le puse cargarProductos y alli dentro cree un foreach para recorrer todos los arrays.
Cree un div contenedor que le puse de nombre (producto) y aplique un innerhtml para darle la estructura dentro.
luego hice un append al div (contenedorProductos), despues llamo a una funcion con el nombre cargar productos.

BOTONES

Le puse un id a los botones en el html ( genere una contante en el js y le puse botonesCategoria
Y le agregue un foreach y un addevelintenner para poder filtar por categorias los productos.
(use filter para filtrar las categorias)
Para agregar los productos al carrito...

cree un let que diga botones agregar(para agregar al carrito)
luego cree una funcion (actualizarBotonesAgregar)
creo un foreach de botonesAgregar y dentro un evento addevenlistenner y 
que como funcion sea "agregar al carrito"

creo una cont de productosEnCarrito que sea igual a un array vacio

Entonces creo la funcion agregarAlCarrito 
busco el array de productos con el metodo FindIndex.
Ademas use some (para que me devuelva true o false)
le agregue la propiedad (cantidad)
despues use el metodo push para agregar pruductos al carrito

NUMERITO

Para el numerito cree una variable let numerito
y tambien una funcion para actualizar el numerito lo hice con el metodo (reduce)
al que le agregue un acumulador para que sume toda la cantidad de los productos que agregue al carrito y cuya cuenta arranque en cero.

Para llevar todo al localStorage hago un localStorage.setitem(productoencarrito) 
y como valor le pase un JSON.stringfy de (productosencarrito)

Cree un carrito.html y un carrito.js lo traigo y parseo el JSON 
traigo algunos elementos del html como 
contenedorCarritoVacio 
contenedorProductos,
contenedorCarritoAcciones,
contenedorCarritoComprado.

CARRITO

Creo un foreach para productos en carrito 
por cada producto creo un div con la clase (carrito-producto)
creo una funcion botonesEliminar (para eliminar productos en el carrito)

















