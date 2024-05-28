## Integrantes y roles
- **(CEO) Julián Barcia Facal**
Encargado de coordinación, comunicación, documentación y gestión del proyecto. Gestionará la geolocalización, el uso de sensores y las API de terceros empleadas durante el proyecto.
- **(CTO) Ruben Tome Moure**
Realizará testing de integración, al igual que participará en la unificación y creación de módulos da arquitectura. Además, tendrá un papel importante a la hora de crear la base de datos externa en Firebase, definiendo su estructura y coordinando su correcto uso.
- **(COO) David Zambrana Seoane**
Encargado de la arquitectura, se coordinará principalmente con el CEO para realizar la integración de nuevas funcionalidades y componentes a la aplicación.
- **(CXO)Jerónimo José Pardo Rodríguez**
Centrará su foco en mantener una correcta UX durante todo el proyecto a medida que se añaden nuevas funcionalidades.

## Funcionalidades 
Este proyecto se centra en el desarrollo de una aplicación que facilite un método para la creación y organización de eventos deportivos. Todos estos eventos se concretarán en un entorno de mapa, donde los usuarios podrán confirmar su asistencia si así lo desean. Cada evento contará con un formato, una fecha, una localización y con su correspondiente número de jugadores.

### Críticas
- **Sistema de identificación o login. Permitirá identificar al usuario unívocamente. Este identificador es necesario, puesto que es el que marcará la estructura en la base de datos. Login con cuentas de Google** _Coordinación entre CEO y COO para crear un modelo simple y funcional_
- **Creación de cada uno de los eventos sobre un mapa, fijando la localización en este y guardando su referencia en la base de datos. Del mismo modo, en esta creación se deben poder fijar otras opciones como: horario, capacidad máxima, formato (casual o torneo) y el nombre y número de equipos se así se requiere. Una vez creado el evento, el resto de usuarios podrán visualizarlo, bien en el mapa si su proximidad es suficiente o en la lista global de eventos e inscribirse si lo desean.** _Funcionalidad crítica y amplia, por lo tanto, se comparte por todo el equipo, énfasis en geolocalización por el CEO y base de datos por el CTO_
- **Edición de formato del evento creado (casuales y torneo). Dependiendo del formato elegido, las opciones presentes al usuario cambian, puesto que el primero implica fijar un total de participantes a los que se suman jugadores. En el segundo caso, se deben crear primero equipos a los cuales se inscriben los jugadores** _Tarea coordinada entre todos los integrantes del grupo puesto se coordina las funcionalidad en la app con la base de datos._
- **Sistema de ranking de usuario y de equipos, mediante una variable de puntos totales** _Coordinación entre COO y CXO_
- **Geolocalización del usuario en tiempo real. Esta funcionalidad es crítica, puesto que el usuario solo podrá ver los eventos en el mapa si tiene la localización activada y si estos se encuentran dentro de su rango definido de alcance.** _Tarea principalmente a cargo del CEO_
- **
### No críticas_
- **Módulo de información sobre el clima en la localización del evento en tiempo real. Mediante el uso de una API externa en el evento se debe mostrar un indicador de la temperatura y tiempo en el lugar del evento** _Tarea del CEO_
- **Creación de indicador de como llegar a la localización del evento. Dentro de cada uno de los eventos mediante un botón de como llegar se podrá acceder a un fragment que muestra una ruta calculada de como llegar al evento y de su distancia y duración** _Tarea del CEO_

## Target
El usuario objetivo estaría en una franja de edad comprendida entre los 12 y los 30 años. Dado que se tratan de usuarios bastante jóvenes, el status económico no sería demasiado alto, por lo que la aplicación buscará adaptarse a estas condiciones y ser y proporcionar en su mayoría servicios de forma gratuita. La aplicación no realizará ningún otro sesgo respecto al target esperado, cuestiones como el género son intrascendentes, pues al final el usuario final se identificará únicamente por su gusto por el deporte, en especial deportes de equipo. Estas personas estarían buscando que la aplicación facilite poder organizar encuentros casuales con otras personas para practicar deporte sin necesidad previa de conocerse. 
Respecto al mercado, sería más bien de nicho. Debido a la franja de edad en la que la aplicación se desarrolla, no se espera una cantidad de usuarios masificada. Por lo tanto, el diseño de la aplicación no tiene que estar orientado a cubrir una amplia demanda, sino más bien en realizar correctamente lo que se propone. Nuestro cliente perfecto inicial, no se reduce a un único usuario, puesto que este no encontraría mucha utilidad en la aplicación, sino que más bien este cliente ideal se representa por un grupo de personas que quieren organizar un evento deportivo, conformando equipos, y que buscan ampliar la participación en este mediante el uso de la app.
## Estudio de mercado
Nuestra aplicación, a diferencia de la gran mayoría disponible actualmente, no se centra en organizar eventos de forma general, sino en posibilitar encuentros deportivos casuales entre grupos pequeños de personas, y permitir que estas compitan entre ellas en eventos tales como torneos. Para fidelizar a los usuarios, permitiremos crear equipos y formar parte de ellos, por lo tanto, si surge una aplicación similar, el usuario deberá crear de nuevo los equipos, lo cual puede ser tedioso y desmotivará al usuario a la hora de realizar este cambio. Además, se creará un sistema de puntos, que se incrementan si el usuario se inscribe en eventos. Estos puntos servirán para rankear al usuario respecto a la base de jugadores global, sirviendo como un incentivo para continuar usando la app y participando

En cuanto a aplicaciones similares en el mercado, no hemos encontrado ninguna semejante en España. Sin embargo, en Reino Unido, debido a la gran importancia que tiene el futbol amateur y la comúnmente conocida Sunday League existen una gran variedad de ejemplos sobre los que basarse. (La mayoría de capturas son recogidas directamente de la APP Store debido a las restricciones geográficas a la hora de descargarlas.) 
#### Are you in
![Imagen are you in](https://github.com/rubenTome/APM/blob/main/estudio_mercado/capturas/are_you_in/are_you_in.png)
Esta primer ejemplo muestra la aplicación de Are you In. Como se puede ver en las capturas esta aplicación se centra en la organización de eventos deportivos, a los cuales cualquier usuario se puede inscribir. Estos eventos se le muestran al usuario en forma de lista (tercera captura), pudiendo acceder a cada uno de ellos de forma individual (primera captura) para obtener información más pormenorizada. De esta aplicación, además del esquema de UX, se han extraído ideas como el uso de un sistema de "coins" o puntos que el usuario obtenga y pueda emplear en la aplicación como método de fidelización.

#### TSL
![Imagen TSL](https://github.com/rubenTome/APM/blob/main/estudio_mercado/capturas/TSL/Sin%20nombre.png)
Esta segunda aplicación llamada TSL, ya se centra mucho más en el mercado de _Sunday League_ que se mencionó anteriormente. Como se puede ver mantiene un esquema muy similar al anterior, con una listado de todos los eventos que ocurren o ocurrirán en un futuro. Esta aplicación además cuenta con una pestaña de "Photos" que permite la integración las redes sociales de forma natural. Además hace uso de un calendario, como posible modelo para mantener la usuario informado sobre los eventos.

#### Organizador torneo, crear liga
Esta última aplicación llamada __Organizador torneo, crear liga__ , se encuentra muy próxima en muchas de las funcionalidades que propone a las ideas de nuestro proyecto. Como se puede ver en esta primera captura, los eventos a crear pueden ser de todo tipo, modificando tanto el formato (liga,playoff) como la disciplina.
![Evento Organizador](https://github.com/rubenTome/APM/blob/main/estudio_mercado/capturas/Organizador/crearevento.png)

A la hora de incorporar equipos, esta aplicación incluye una nueva funcionalidad denominada importar. Esta permite "copiar" a un equipo entero a otro evento sin necesidad de tener que crearlo de nuevo. No obstante, en esta aplicación, la inscripción a estos eventos se hace de modo "local", los jugadores o usuarios serán inscritos por el creador del evento y su interacción no irá más allá que un texto. 
![Equipo Organizador](https://github.com/rubenTome/APM/blob/main/estudio_mercado/capturas/Organizador/equipos.png)

Como se puede ver en estas capturas, assets como el escudo se encuentra detrás de un modelo PRO de pago. Este trae otras funcionalidades como las que se muestran en esta captura. Como nuestro proyecto se centra en jóvenes con pocos o nulos ingresos, este modelo de negocio puede resultar contraproducente pero se apunta como posible consideración.
![Pro Organizador](https://github.com/rubenTome/APM/blob/main/estudio_mercado/capturas/Organizador/Pro.png)

##  Diseño de la arquitectura de comunicaciones.
![Diseño](https://github.com/rubenTome/APM/blob/main/dise%C3%B1o_arquitectura/Dise%C3%B1oArqComunicaciones.svg)

