
<div aling="center">
    <img src="/img/Logo_blackbg.png">
</div>

# Entrega Proyecto SQL Coderhouse

## Primera preentrega

Alumna:Dovis Yesica Lorena

Docente: Maximiliano Torreblanca

Comisión: 59405 SQL   

### Introducción: Descripción de la temática de la base de datos:

Crear una base de datos relacionar para gestionar una tienda on line especializada en cerveza llamada "La birra es Bella". 
La base de datos gestionara usuarios, roles (cliente & administrador), direcciones, tarjetas, productos y pedidos. Las relaciones entre las tablas permiten almacenar información detallada sobre los clientes, sus datos de contacto, métodos de pago, productos disponibles y pedidos realizados. 

### Diagrama de entidad relación
___
<div aling="center">
    <img src="/img/DiagramaDER.jpg">
</div>

___

Para implementar las relaciones descritas, se necesitarán varias tablas intermedias y claves foráneas para establecer las conexiones entre las entidades. A continuación, se detalla cómo se pueden crear estas relaciones en una base de datos relacional.
___

### Listado de Tablas (Entidad-Descripcion-Atributos)
`USUARIOS`  
+ Esta tabla almacena información básica sobre los usuarios del sistema.
+ _Atributos_: id_usuario / nombre / apellidos / fecha_nacimiento / email / password.

`ROLES`  
+ Esta tabla define los diferentes roles que pueden tener los usuarios en el sistema,de momento se proyectas solo 2  administrador & cliente.
+ _Atributos_: id_rol / nombre 

`USUARIO_ROLES`  
+ Esta tabla establece la relación entre usuarios y roles, indicando qué roles tiene asignados cada usuario.
+ _Atributos_:id_usuario / id_roles.


`DIRECCIONES`  
+ Esta tabla almacena información sobre las direcciones de los usuarios.
+ _Atributos_: id_direccion, codigo_postal, localidad, calle, numero, piso, letra.


`USUARIOS_DIRECCIONES`  
+ indicando las direcciones asociadas a cada usuario.
+ _Atributos_: id_usuario, id_direccion.


`TARJETAS`  
+ Guarda la información de las tarjetas de crédito de los usuarios.
+ _Atributos_:id_tarjeta, num_tarjeta, nombre_titular, fecha_caducidad, CVV.

`USUARIOS_TARJETAS`  
+ indica las tarjetas asociadas a cada usuario.
+ _Atributos_:id_usuario, id_tarjeta.

`PRODUCTOS`  
+ Representa los productos que se venden en la tienda.
+ _Atributos_:id_producto, nombre, descripcion, precio, stock.


`PEDIDOS`  
+ Almacena la información de los pedidos realizados.
+ _Atributos_:id_pedido, fecha, id_direccion, id_tarjeta.

`PEDIDOS_PRODUCTOS`  
+ Detalla los productos incluidos en cada pedido
+ _Atributos_:id_pedido, id_producto, unidades, precio_venta.
___

### Documentación de Tablas > CLAVES > INDICES > ATRIBUTOS > TIPO DE DATOS > DESCRIPCION Y 

<div aling="center">
    <img src="/img/PK.jpg">
</div>

<div aling="center">
    <img src="/img/FK.jpg">
</div>

___

### Análisis de las Relaciones

<div aling="center">
    <img src="/img/cardinalidad.jpg">
</div>
___

`Relaciones Muchos a Muchos`

Usuarios y Roles: Un usuario puede tener múltiples roles (por ejemplo, cliente y administrador) y un rol puede ser asignado a múltiples usuarios.
Usuarios y Direcciones: Un usuario puede tener múltiples direcciones (por ejemplo, domicilio y trabajo) y una dirección puede pertenecer a múltiples usuarios (si comparten vivienda, por ejemplo).
Usuarios y Tarjetas: Un usuario puede tener múltiples tarjetas de crédito y una tarjeta puede ser utilizada por múltiples usuarios (si comparten una cuenta).
Pedidos y Productos: Un pedido puede contener múltiples productos y un producto puede estar en múltiples pedidos.

`Relaciones Uno a Muchos`

Pedidos y Direcciones: Un pedido se realiza a una sola dirección.
Pedidos y Tarjetas: Un pedido se paga con una sola tarjeta.


___


<div aling="center">
    <img src="/img/logo.png">
</div>