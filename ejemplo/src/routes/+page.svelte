<script>
    // Creamos una variable para guardar el texto que escribimos en el input
    // $state() -> con esta runa le decimos a Svelte que este dato puede cambiar con el tiempo
    let nuevaTarea = $state("");

    // Creamos un array donde meteremos todas las tareas
    // $state() -> permite que Svelte detecte los cambios y actualice la página
    let arrayTareas = $state([]);

    // Creamos la función que agrega la tarea
    function agregarTarea() {

        // Solo añadimos la tarea si el texto no está vacío
        if (nuevaTarea !== "") {

            // Añadimos la tarea al array de tareas
            arrayTareas.push(nuevaTarea);

            // Vaciamos el input después de añadir la tarea
            nuevaTarea = "";
        }
    }
</script>

<!-- Escribimos el título de la aplicación -->
<h1>Lista de tareas</h1>

<!-- Ponemos un campo para escribir la tarea a realizar -->
<!-- bind:value={nuevaTarea} -> esto enlaza el valor del input con el de la variable 'nuevaTarea' -->
<input type="text" bind:value={nuevaTarea} placeholder="Escribe una tarea">

<!-- Ponemos un botón para añadir esa tarea -->
<!-- onclick={agregarTarea} -> al darle click al boton ejecutamos la función que crea la nueva tarea -->
<button onclick={agregarTarea}>Añadir</button>

<!-- Creamos una lista con todas las tareas que tenemos en el array -->
<ul>
    <!--  Recorremos todas las tareas del array -->
    <!--  Este es el equivalente a un bucle 'for of' en JavaScript -->
    {#each arrayTareas as tarea}

        <!-- Mostramos la tarea -->
        <!-- {} -> nos permite decirle a Svelte que lo que hay dentro es una variable con un valor -->
        <!-- tarea -> contiene el valor actual del array de tareas -->
        <li>{tarea}</li>
        
    {/each}
</ul>