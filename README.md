
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
**Tablas**
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
+indicando las direcciones asociadas a cada usuario.
+ _Atributos_: id_usuario, id_direccion.


`TARJETAS`  
+ Guarda la información de las tarjetas de crédito de los usuarios.
+ _Atributos_:id_tarjeta, num_tarjeta, nombre_titular, fecha_caducidad, CVV.




<div aling="center">
    <img src="/img/logo.png">
</div>