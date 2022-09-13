# consultas1

#  EJERCICIOS CONSULTAS SQL

## Tabla usuario

![tabla usuario](img/tabla_usuario.png "Tabla usuario")

## COMANDO SELECT

1. Para visualisar toda la informacion que contiene la tabla `usuario` se puede incluir con la instruccion SELECT el caracter '*' o cada uno de los campos de la tabla
`select * from usuario` 

![Consulta1](img/Consulta1.png "Consulta1")

2. Visualizar solamente la identificacion del usuario.

`select identificacion from usuario`

![Consulta2](img/Consulta2.png "Consulta2")

3. Se desea obtener los registros cuya identificacion sean mayores o iguales a 150, se debe utilizar la clausula WHERE que especifica las condiciones que deben reunir los registros que se van a seleccionar.

`SELECT * FROM usuario WHERE Identificación >='150'`

![consulta3](img/consulta3.png)

4. Si desea obteer los registros cuyo sus apelidos sean Vanegas o Cetina, se ddebe utilizar el operador IN que especifica los registros que se quieren visualizar de una tabla

`SELECT apellidos FROM usuario WHERE apellidos IN ('Vanegas','Cetina')`

![consulta4](img/consulta4.png)

O se puede utilizar el operador OR.

`SELECT apellidos FROM usuario WHERE apellidos='Vanegas'OR apellidos='Cetina'`

![consulta4.1](img/consulta4.1.png)

5. Si se desea obtener los registros cuya identificacion sea menor de '110' y la ciudad sea 'Cali' se debe utilizar el operadodr AND

`SELECT * FROM usuario WHERE Identificaicon<'110' AND ciudad='Cali'`

![Consulta5](img/Consulta5.png "Consulta5")

6. Si se desea obtener los registros cuyos nombres  empiencen por la letra A , se debe utlizar el operador LIKE que utliza los patrones '%'(Todos) '_'(caracter).

`SELECT * FROM ususario WHERE nombre LIKE 'A%'`

![Consulta6](img/Consulta6.png "Consulta6")

7. Si desea obtener los registros de los nombres contengan la letra 'a'

`SELECT * FROM ususario WHERE nombre LIKE '%a%'`

![Consulta7](img/Consulta7.png "Consulta7")

8. Si se desea tener los registros donde la 4 letra del nombre sea una 'a' 

`SELECT * FROM ususario WHERE nombre LIKE '___a%`

![Consulta8](img/Consulta8.png "Consulta8")

9. Si se desea obtener los registros cuya identificacion este entre el intervalo 110 y 150, se debe utilizar la clausula BETWEN, que sirve para especificar un intervalo de valores 

`SELECT * FROM ususario WHERE identificacion BETWEEN '110' AND '150'`

![Consulta9](img/Consulta9.png "Consulta9")

## COMANDO DELET

10. Para eliminar solamente los registros cuya identificacion sea > de 130

`DELETE FROM usuario WHERE identificacion>'130'`

![Consulta10](img/Consulta10.png "Consulta10")
![Consulta10.2](img/consulta10.2.png.png "Consulta10.2")

## COMANDO UPDATE 

11. Para actualizar la ciudad la ciudad de nacimiento de Cristian Vanegas, cuya identificacion es 114.

`UPDATE usario SET ciudad_nac = 'Manizales' WHERE Identificación='114'`

![Consulta11](img/Consulta11.png "Consulta11")
![Consulta11.2](img/consulta11.2.png.png "Consulta11.2")

## INNER JOIN 

permite obtener datos o mas tablas. cuando se realiza la concatenacion de las tablas, no necesariamente se deben mostrar todos los datos de las tablas.