# arreglos-asociativos
Realice un programa en PHP que permita la entrada de nombre, apellido y cedula de 3 empleados al igual que sus respectivos sueldos, departamento y lugar de trabajo. utilice arreglos asociativos.

<?php 
	$nombre2=$_POST['name2'];
	$apellido2=$_POST['lastname2'];
	$ci2=$_POST['ci2'];
	$sueldo2=$_POST['salary2'];
	$direccion2=$_POST['direction2'];
	$oficina2=$_POST['office2'];

	$datos2 = array("Nombre"=>$nombre2,"Apellido"=>$apellido2,"CI"=>$ci2,"Sueldo"=>$sueldo2,"Dirección"=>$direccion2,"Oficina"=>$oficina2);
	
	foreach ($datos2 as $key => $value) {
		echo "$key: $value <br>";
	}
?>
