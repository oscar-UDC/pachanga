# Almacenamiento en la nube
Para nuestra aplicación, como queremos que la información tanto de eventos como de rankings sea accesible para todos los usuarios, es necesario guardar estos elementos en la nube. Para ello hemos escogido emplear la base de datos _Real Time Database_, que nos proporciona Firebase.

En ella se guardarán 4 "ramas" principales. 
1. Eventos: Se guardarán en ellos toda la información relevante acerca de un torneo. Cada torneo, cuenta con una lista de jugadores que indica quien está inscrito.
2. Jugadores: Cuenta con toda la información que identifica a un usuario: nombre, posición, equipo...
3. Equipos: Todos los equipos presentes en la base de datos están bajo el control del torneo o evento al que pertenecen. Cada uno cuenta con datos como, nombre, maxplayers, lista de participantes...
4. Resultados: Para cada uno de los torneos se muestra los partidos ocurridos y sus resultados.

# Almacenamiento en local
En cuanto a almacenamiento en local se ha empleado SharedPreferences. Aunque en clases teóricas se ha recomendado migrar a Jetpack DataStore, no hemos conseguido que su funcionamiento sea el correcto por lo cual se ha optado por la opción más antigua.

Para su uso se han planteado varias ideas:
1. Almacenar las credenciales del usuario una vez logeado para cuando se acceda al fragment del perfil, este solo haga la petición de la información directamente por este identificador.
2. Guardar User Settings como el tema, el idioma.
3. Se ha planteado la opción de guardar la información de si el usuario ya está loggeado, para así evitar que de cada vez se comprueba el auth con Firebase.

