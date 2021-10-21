# arreglos-asociativos
Realice un programa en PHP que permita la entrada de nombre, apellido y cedula de 3 empleados al igual que sus respectivos sueldos, departamento y lugar de trabajo. utilice arreglos asociativos.

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registro de empleados con arreglos asociativos</title>
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
</head>
<body>

    <div style="display: flex;">
        <br><br>
        <form id="formulario" method="POST" style="display: flex; flex-direction:column; margin-right: 3rem;">
            <label for="nombre">
                <span>Nombre:</span>
                <input type="text" id="nombre" placeholder="Nombre" name="nombre">
            </label>

            <label for="apellido">
                <span>Apellido:</span>
                <input type="text" id="apellido" placeholder="Apellido" name="apellido">
            </label>

            <label for="ci">
                <span>C.I:</span>
                <input type="text" id="ci" placeholder="C.I" name="ci">
            </label>

            <label for="sueldo">
                <span>Sueldo:</span>
                <input type="text" id="sueldo" placeholder="Sueldo" name="sueldo">
            </label>

            <label for="direccion">
                <span>Dirección:</span>
                <input type="text" id="direccion" placeholder="Dirección" name="direccion">
            </label>

            <label for="oficina">
                <span>Oficina:</span>
                <input type="text" id="oficina" placeholder="Oficina">
            </label>

            <button type="button" id="enviar">Enviar</button>
        </form>
        <br><br>

        <form id="formulario2" method="POST" style="display: flex; flex-direction:column; margin-right: 3rem;">
            <label for="nombre2">
                <span>Nombre:</span>
                <input type="text" id="nombre2" placeholder="Nombre">
            </label>

            <label for="apellido2">
                <span>Apellido:</span>
                <input type="text" id="apellido2" placeholder="Apellido">
            </label>
            
            <label for="ci2">
                <span>C.I:</span>
                <input type="text" id="ci2" placeholder="C.I">
            </label>

            <label for="sueldo2">
                <span>Sueldo:</span>
                <input type="text" id="sueldo2" placeholder="Sueldo">
            </label>

            <label for="direccion2">
                <span>Dirección:</span>
                <input type="text" id="direccion2" placeholder="Dirección">
            </label>

            <label for="oficina2">
                <span>Oficina:</span>
                <input type="text" id="oficina2" placeholder="Oficina">
            </label>

            <button type="button" id="enviar2">Enviar</button>
        </form>

        <br><br>

        <form id="formulario3" method="POST" style="display: flex; flex-direction:column; margin-right: 3rem;">
            <label for="nombre3">
                <span>Nombre:</span>
                <input type="text" id="nombre3" placeholder="Nombre">
            </label>

            <label for="apellido3">
                <span>Apellido:</span>
                <input type="text" id="apellido3" placeholder="Apellido">
            </label>
        
            <label for="ci3">
                <span>C.I:</span>
                <input type="text" id="ci3" placeholder="C.I">
            </label>

            <label for="sueldo3">
                <span>Sueldo:</span>
                <input type="text" id="sueldo3" placeholder="Sueldo">
            </label>

            <label for="direccion3">
                <span>Dirección:</span>
                <input type="text" id="direccion3" placeholder="Dirección">
            </label>

            <label for="oficina3">
                <span>Oficina:</span>
                <input type="text" id="oficina3" placeholder="Oficina">
            </label>

            <button type="button" id="enviar3">Enviar</button>
        </form>

    </div>

    <br><br>

    <div id="respuesta"></div>
    <br>
    <div id="respuesta2"></div>
    <br>
    <div id="respuesta3"></div>
    
</body>

<script>

    $('#enviar').click(function() {
        var nombre = document.getElementById('nombre').value,
            apellido = document.getElementById('apellido').value,
            ci = document.getElementById('ci').value,
            sueldo = document.getElementById('sueldo').value,
            direccion = document.getElementById('direccion').value,
            oficina = document.getElementById('oficina').value;

        var parametros = {
                "name": nombre,
                "lastname": apellido,
                "ci": ci,
                "salary": sueldo,
                "direction": direccion,
                "office": oficina
            };

        $.ajax({
            url:'data1.php',
            type: 'POST',
            data: parametros
        })
        .done(function(res) {
            $('#respuesta').html(res)
        })
        .fail(function() {
        console.log("error");
        });
    });

        $('#enviar2').click(function() {
        var nombre = document.getElementById('nombre2').value,
            apellido = document.getElementById('apellido2').value,
            ci = document.getElementById('ci2').value,
            sueldo = document.getElementById('sueldo2').value,
            direccion = document.getElementById('direccion2').value,
            oficina = document.getElementById('oficina2').value;

        var parametros2 = {
                "name2": nombre,
                "lastname2": apellido,
                "ci2": ci,
                "salary2": sueldo,
                "direction2": direccion,
                "office2": oficina
            };
            
        $.ajax({
            url:'data2.php',
            type: 'POST',
            data: parametros2,
        })
        .done(function(res) {
            $('#respuesta2').html(res)
        })
        .fail(function() {
        console.log("error");
        });
    });

        $('#enviar3').click(function() {
        var nombre = document.getElementById('nombre3').value,
            apellido = document.getElementById('apellido3').value,
            ci = document.getElementById('ci3').value,
            sueldo = document.getElementById('sueldo3').value,
            direccion = document.getElementById('direccion3').value,
            oficina = document.getElementById('oficina3').value;

        var parametros3 = {
            "name3": nombre,
            "lastname3": apellido,
            "ci3": ci,
            "salary3": sueldo,
            "direction3": direccion,
            "office3": oficina
        };

        $.ajax({
            url:'data3.php',
            type: 'POST',
            data: parametros3,
        })
        .done(function(res) {
            $('#respuesta3').html(res)
        })
        .fail(function() {
        console.log("error");
        });
    });

</script>
</html>
