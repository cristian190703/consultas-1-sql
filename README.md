#  EJERCICIOS CONSULTAS SQL

## Tabla usuario

## COMANDO SELECT
![tabla usuario](img/tabla_usuario.png "Tabla usuario")

1. Para visualisar toda la informacion que contiene la tabla `usuario` se puede incluir con la instruccion SELECT el caracter '*' o cada uno de los campos de la tabla
`select * from usuario` 

![Consulta1](img/consulta1.png "Consulta1")

2. Visualizar solamente la identificacion del usuario.

`select identificacion from usuario`

![Consulta2](img/consulta2.png "Consulta2")

3. Si se desea optener los registros cuya identificacion mayor o igual a 150 se debe utilizar la clausula WHERE que especifica las condiciones que debe reunir los registros que se van a seleccionar 

`SELECT * FROM usuario WHERE identificacion>=` '150'

![Consulta3](img/consulta3.png "Consulta3")

4. Si se desea obtener los regitros cuyo sus apellidos sean Vnegas o Cetina se debe utilizar el operador IN que especifica los registros que se quieren visualizar de una tabla

`SELECT apellidos FROM usuario WHERE apellidos IN ('Vanegas','Cetina')`

![Consulta4](img/consulta4.1.png "Consulta4")

O se puede utilizar el operador OR

`SELECT apellidos FROM usuario WHERE apellidos='Vanegas' OR apellidos='Cetina'`

![Consulta4](img/consulta4.png "Consulta4")

5. Si se desea obtener los registros cuya identificacion sea menor de '110' y la ciudad sea 'Cali' se debe utilizar el operador AND

![Consulta5](img/consulta5.png "Consulta5")

6. Si se desea obtener los registros cuyos nombres empiecen por la letra 'A' se debe utilizar el operador LIKE que utiliza los patrones'%' (todos) y '_' (caracter)

`SELECT * FROM usuario WHERE nombre LIKE'A%'`

![Consulta6](img/consulta6.png "Consulta6")

7. Si desea obtener los registros cuyos nombres contengan la letra 'a' 

`SELECT * FROM usuario WHERE nombre LIKE '%a%'`

![Consulta7](img/consulta7.png "Consulta7")

8. Si se desea obtener los registros donde la cuerta letra del nombre sea una 'a' 

`SELECT * FROM usuario WHERE nombre LIKE'   a%'`

![Consulta8](img/consulta8.png "Consulta8")

9. Si se desea obtener los registros cuya identificaicon este entre el intervalo 110 y 150 se debe utilizar la clausula BETWEEN que sirve para especificar un intervalo de valores

`SELECT * FROM usuario WHERE identificacion BETWEE '110' AND '150'`

![Consulta9](img/consulta9.png "Consulta9")

  


## COMANDO DELETE

10. Para eliminar solamente los registros cuya identificacion sea mayor de 130

`DELETE FROM usuario WHERE Identificacion>'130'`

![Consulta10](img/consulta10.png "Consulta10")
![Consulta10](img/consulta10.2.png "Consulta10")


## COMANDO UNDATE

11. Para actualizar la ciudad de nacimiento de Cristian Vanegas cuya Identificacion es 114

`UPDATE usuario SET ciudad_nac = 'Manizales' WHERE Identificacion='114'`

![Consulta11](img/consulta11.png "Consulta11")
## INNER JOIN

Permite obtener datos de dos o mas tablas cuando se realiza la concanetacion de las tablas no necesariamente se deben mostrar todos los datos de las tablas 

## TABLA PEDIDOS

![Tabla pedidos](img/tabla%20pedidos.png "Tabla pedidos")

12. Para visualizar los campos identificacion nombre apellidos de la tabla usuario y nrpedido fecha de compra decha de vencimiento y observacion de la tabla pedidos se debe realizar la sigueinte instruccion SQL

`SELECT usuario.Identificacion, usuario.nombre, usuario.apellidos, pedido.nropedido, pedidos.fechaCompra, pedidos.fechaVence, pedidos.observacion FROM usuario INNER JOIN pedidos ON usuario.Identificaicon = pedidos.Identificacion`

![Consulta12](img/Consulta12.png "Consulta12")

13. Para visualizar todos campos de las tablas usuarios y pedidos donde Indentificancion sea mayor que 100 se debe realizar la siguiente instruccion

`SELECT usuarios.*,pedidos.* FROM usuarios INNER JOIN pedidos ON usuarios.Identificacion = pedidos.Identificacion WHERE usuarios.Identificacion>100`

![Consulta13](img/Consulta13.png "Consulta12")


lta13.png "Consulta13")