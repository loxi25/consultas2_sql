# consultas2_sql



1. ![departamento](img/departamento.jpg "departamento")

2. ![empleados](img/empleados.jpg "empleados")



## moodelo fisico
3. ![estructura](img/estructura.jpg "estructura")


1. Obtener la lista de los apellidos de todos los empleados.


SELECT apellidos_empleado AS empleado FROM empleado;


 ![consulta1](img/consulta1.jpg "consulta1")



2. Obtener los apellidos de todos los empleados sin repeticiones.

SELECT DISTINCT apellidos_empleado FROM empleado;


 ![consulta2](img/consulta2.jpg "consulta2")



3.  Obtener todos los datos de los empleados que se apellidan 'santana'.

SELECT * FROM empleado WHERE apellidos_empleado LIKE 'santana%';

 ![consulta3](img/consulta3.jpg "consulta3")



 4. Obtener todos los datos de los empleados que se apellidan "Diaz" y los que se apellidan "Rodriguez".  Usar OR o IN

 `SELECT * FROM empleado WHERE apellidos_empleado LIKE 'florez%' OR apellidos_empleado LIKE 'castillo%';

  ![consulta4](img/consulta4.jpg "consulta4")


5.  Obtener los nombres de los empleados que trabajan en el departamento 11


SELECT nombre_empleado FROM empleado WHERE id_departamento = 11;

  ![consulta5](img/consulta5.jpg "consulta5")

6. Obtener todos los datos de los empleados cuyo apellido empiece por 's


SELECT * FROM empleado WHERE apellidos_empleado LIKE 's%

  ![consulta6](img/consulta6.jpg "consulta6")

7. Obtener el presupuesto total de todos los departamentos

SELECT presupuesto_departamento FROM departamento;

  ![consulta7](img/consulta7.jpg "consulta7")



8. Obtener el número de empleados de cada departamento.

SELECT id_departamento, COUNT(*) AS cantidad_empleados FROM empleado GROUP BY id_departamento;

![consulta8](img/consulta8.jpg "consulta8")

9. Obtener un listado completo de empleados, incluyendo por cada empleado los datos del empleado y de su departamento.



SELECT * FROM Empleado, Departamento WHERE Empleado.id_departamento = Departamento.id_departamento;


  ![consulta9](img/consulta9.jpg "consulta9")


10. Obtener un listado completo de empleados, incluyendo el nombre y apellidos del empleado junto al nombre y presupuesto de su departamento.


SELECT nombre_empleado, apellidos_empleado, nombre_departamento, presupuesto_departamento FROM empleado , departamento WHERE empleado.id_departamento = departamento.id_departamento;


![consulta10](img/consulta10.jpg "consulta10")

11. Obtener los nombres y apellidos de los empleados que trabajen en departamentos cuyo presupuesto sea mayor a 100000000

SELECT nombre_empleado , apellidos_empleado FROM empleado , departamento WHERE empleado.id_departamento = departamento.id_departamento AND presupuesto_departamento > 100000000;


![consulta11](img/consulta11.jpg "consulta11")



# clausula iner join

![inerjoin](img/inerjoin.png "inerjoin")

![xd](img/xd.png "xd")
