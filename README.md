# arreglos-asociativos
Realice un programa en PHP que permita la entrada de nombre, apellido y cedula de 3 empleados al igual que sus respectivos sueldos, departamento y lugar de trabajo. utilice arreglos asociativos.

<?php
	$nombre1=$_POST['name'];
	$apellido1=$_POST['lastname'];
	$ci1=$_POST['ci'];
	$sueldo1=$_POST['salary'];
	$direccion1=$_POST['direction'];
	$oficina1=$_POST['office'];
	
	$datos1 = array("Nombre"=>$nombre1,"Apellido"=>$apellido1,"CI"=>$ci1,"Sueldo"=>$sueldo1,"Dirección"=>$direccion1,"Oficina"=>$oficina1);
	
	foreach ($datos1 as $key => $value) {
		echo "$key: $value <br>";
	}
?>
