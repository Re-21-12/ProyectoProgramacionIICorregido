# Diagrama
![proyecto_progra](https://github.com/Re-21-12/ProyectoProgramacionIICorregido/assets/104967229/f383222e-b7bf-4ce3-a597-85cadb50d388)

# Documentacion Externa
Este proyecto consta de el control de una fabrica de sillas, utilizando el lenguaje Java aplicando conceptos de POO y los principios SOLID.

## Que contiene el control de fabrica?

- Clase _Control_Fabrica_de_sillas_: En ella encontraremos ArrayList como manera de almacenamiento de los datos, tendremos tales de tipo: 'distribuidores, proveedores y clientes' Donde en cada operacion de querer se podra ir almacenando el proveedor, distribuidor o cliente que haya efectuado alguna accion en cada debido proceso. 
  * Ademas tendremos una clase Inventario dentro de la misma, que contendra ArrayList de material y silla.

- Clase _Entidad_: La clase Entidad es una representacion de una clase padre con los siguientes atributos: 'Id, nombre, numero_telefono, direccion y correo'. Cabe recordar que _Entidad_ Implementa una interfaz llamada 'IGenerar_Factura'.
  * IGenerar_Factura: Implementando esta interfaz debe de generar un objeto 'Factura' que correspondera al Cliente. Este metodo se hereda de la clase padre Entidad a las clases: 'Proveedor y Disitribuidor'. 

- Clase _Cliente_: La clase cliente contiene los siguientes atributos: 'Id, nombre, numero_telefono, Factura' Como parte del proceso de venta de una silla o sillas.

- Clase _Proceso_Fabrica_Sillas_: En ella se puede encontrar todo el proceso de produccion que se obtiene desde la compra del material hasta la venta de las sillas como producto final.
  1. revisarInventario: En este metodo podemos encontrar una revision a los materiales y sillas que se encuentran en el inventario. Inicialmente se encontrara vacio.
  2. realizarCompraMaterial: Como bien describe el nombre este metodo se encarga de comprar material, este material se comprara a un proveedor.
  3. corteDeMateriales: Una vez hecha la compra de materiales procederemos a cortarlos para asi empezar a planear el proceso de ensamblaje.
  4. ensamblaje: A partir del corte de los materiales o de un arreglo de materiales, asignaremos segun los materiales obtenidos la insntancia de un nuevo o nuevos objetos de la clase silla.
  5. empaque: Posteriormente del ensamblaje de las sillas instanciadas estas desde su creacion poseeran una clase estado, en ella se definira en que fase de produccion se encuentra la silla o sillas.
  6. envioParaAlmacenar: Aqui una vez las sillas ya empacadas procederemos a mandar a almacenar, para ello cambiaremos el estado en su clase.
  7. realizarVentaSillas: Por ultimo tendremos la venta, revisaremos nuestro inventario para saber cuantas sillas podremos vender, de encontrarnos con sillas podremos distribuir estas a travez de un distribuidor para un cliente o clientes.

-  Clase _Inventario_ : En ella como se menciona anteriormente podremos encontrar ArrayList de Material 'materiales' y Silla 'sillas' donde se ira almacenando los debidos datos, cabe recordar que estas son herencia de una clase padre llamada 'Producto' que contiene: 'Id, nombre y costo'.
