## Actividades
Solo se cuenta con 2 actividades en este proyecto:
- **Actividad de Login:** Pantalla inicial en la que solo se muestra el botón de login con Google.
- **Actividad Principal:** Pantalla principal sobre la que se ejecuta la totalidad de la aplicación, sobre esta se servirán todos los fragments a emplear.
## Fragment 
Nuestra aplicación se va componer mayoritariamente de fragments ya que tenemos tanto una toolbar con un NavDrawer, como un BottomNavigation que nos permitirán navegar entre ellos. 
En el NavDrawer se mostrará un header con la información de usuario y diversas opciones:
- **Home Fragment:** Nos lleva de vuelta a la pantalla principal cerrando el menú.
- **Settings Fragment:** Nos lleva al fragment de los ajustes de la app.
- **Botón de Share:** Botón de compartir la app.
- **About Us:** Boton que redirecciona al Github del proyecto.
- **Log out:** Botón que cerra la sesión de la cuenta abierta en la primera actividad.
Por su parte el BottomNav cuenta con tres opciones:
- **Ranking Fragment:** Fragment que muestra el ranking de los jugadores.
- **Home Fragment:** Nos lleva de vuelta a la pantalla principal del mapa.
- **Calendario Fragment:** Fragment que muestra la lista de torneos en activo.

A continuación se enumeran todos los fragments y su utilidad:
- **Home Fragment**: Fragment principal que cuenta mostrará el mapa y todos los eventos en el. Clickando en estos eventos se puede acceder a su información o formulario de inscripción. Además esta pantalla cuenta un botón en la parte inferior para crear un nuevo evento. En caso de querer ver los eventos en forma de lista, el usuario solo tendrá que arrastrar la pestaña de la sección inferior para acceder al fragment de lista de eventos.
- **Crear Evento:** Fragment que nos muestra un formulario para crear nuestro evento, indicando nombre formato, fecha o capacidad máxima. Se puede acceder o bien desde el botón en el HomeFragment o en el botón del fragment de Lista de Eventos. Se podrá acceder a el desde el mapa al crear mantener presionado y crear un evento en el.
- **Lista de Eventos:** Fragment que muestra la lista de eventos disponibles visibles en el mapa pero mediante un RecyclerView. Solo se puede acceder a el arrastrando la pestaña que se muestra en el HomeFragment, por ahora este es un botón que se cambiará en el futuro.
- **Fragment Inscribirse en Evento Casual:** Fragment accesible desde o bien la lista de eventos o bien el mapa. Este Fragment permite al usuario ver la información del evento junto con los comentarios del administrador. Cuenta con una sección que muestra el tiempo que se espera en ese lugar a la hora del evento. Además cuenta con un botón de como llegar que permite acceder a otro fragment que guie al usuario. 
- **Fragment Inscribirse en Torneo:** Fragment accesible desde o bien la lista de eventos o bien el mapa. La principal diferencia con el fragment anterior es que a la hora de inscribirse no existe un botón que lo haga directamente. En los torneos el administrador ha creado unos equipos en los cuales cada uno de los usuarios se debe inscribir.
- **Fragment Direcciones:** Fragment unicamente accesible con el botón __Como Llegar__ de los fragments de inscripción. Este muestra una ruta desde la ubicación actual del usuario a la localización del torneo
- **Ranking Fragment:** Fragment que muestra el ranking de los jugadores con un RecyclerView. Se accede a el mediante el bottomNavigation. Si se presiona sobre cualquiera de los jugadores del ranking nos lleva a su perfil.
- **Profile Fragment:** Fragment que muestra la información de un usuario. Existen dos maneras de acceder a el o bien por el paso del ranking anterior o bien mediante el botón de perfil de la ToolBar. En caso de acceder desde el botón de la Toolbar la app también muestra un TabLayout superior donde el usuario puede moverse entre este fragment y el de historial de partidos.
- **Fragment Historial:** Fragment que muestra los resultados de los partidos en los que usuario ha participado. Accesible unicamente desde el TabLayout del perfil del usuario de la propia aplicación.
- **Calendario Fragment:** Fragment que muestra la lista de torneos en activo con un RecyclerView solo se puede acceder desde el bottomNavigation. En caso de clickar en cualquiera de los eventos nos lleva al fragment de su información.
- **Fragment Partidos**: Desde el Fragment de calendario si se accede a uno de los eventos este será el fragment que se muestre por defecto. En el se puede ver los partidos de este evento y sus resultados, en caso de ser dueño del evento puede modificar los resultados. Cuenta con un TabLayout en la parte superior para cambiar entre este fragment y el de clasificiación de equipos.
- **Fragment Clasificiación**: Fragment accesible desde el TabLayout anteriormente explicado. Muestra una clasificación de los equipos dentro del torneo, con datos como Partidos Juagos, Victorias, Empates, Derrotas y Diferencia de Goles.

