# arreglos-asociativos
Realice un programa en PHP que permita la entrada de nombre, apellido y cedula de 3 empleados al igual que sus respectivos sueldos, departamento y lugar de trabajo. utilice arreglos asociativos.

<?php 
	$nombre3=$_POST['name3'];
	$apellido3=$_POST['lastname3'];
	$ci3=$_POST['ci3'];
	$sueldo3=$_POST['salary3'];
	$direccion3=$_POST['direction3'];
	$oficina3=$_POST['office3'];

	$datos3 = array("Nombre"=>$nombre3,"Apellido"=>$apellido3,"CI"=>$ci3,"Sueldo"=>$sueldo3,"Dirección"=>$direccion3,"Oficina"=>$oficina3);
	
	foreach ($datos3 as $key => $value) {
		echo "$key: $value <br>";
	}
?>
