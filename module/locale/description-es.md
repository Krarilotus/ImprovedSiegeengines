# Improved Siegeengines

**Versión**: 1.0.32

En el juego original las máquinas de asedio de la IA se desperdician solas: las catapultas avanzan hasta el muro al que podrían haber disparado desde lejos, las tiendas de asedio se alejan cada vez más en partidas largas hasta que los trabuquetes no llegan a nada, las torres de asedio esperan un muro que la IA considere válido y los escudos persiguen ciervos. Este módulo corrige cada uno de esos fallos.

Todo lo que sigue puede activarse o desactivarse por separado. Cambia las máquinas de asedio de la IA, además del acople y pasajeros de las torres de asedio y los ingenieros con aceite, que también benefician al jugador.

## Qué hace

**Catapultas y trabuquetes eligen objetivos.** Una catapulta o trabuquete de la IA mira alrededor en todo su alcance buscando el muro, torre o puerta enemigos más cercanos y dispara desde donde está. Los edificios civiles solo se atacan si no queda ninguna fortificación al alcance, y solo avanza si no hay nada al alcance. (El juego original miraba una dirección cada vez e ignoraba muros dañados.)

**Se detienen en camino para disparar.** El juego solo busca objetivos en parado, así que las catapultas en incursiones o marchas pasaban de largo ante todo. Ahora las catapultas y trabuquetes de la IA en movimiento miran alrededor con frecuencia y se detienen en cuanto un muro, torre, puerta o edificio enemigo entra en alcance.

**Paso al siguiente oponente.** Una catapulta o trabuquete solo apunta al jugador contra el que marchó su ejército. Al caer ese jugador (muerto su señor), dispara contra cualquier otro enemigo al alcance en lugar de quedar inactivo.

**Otros enemigos al alcance.** Si no hay objetivos del jugador asediado al alcance, dispara contra muros y edificios de otros enemigos en vez de pasar de largo. Los objetivos del jugador asediado conservan prioridad y nunca se apunta a edificios destruidos.

**Fin de disparos a ruinas.** Una máquina apuntando a un edificio (balista de fuego o catapulta) seguía disparando al solar vacío tras destruirlo porque el juego solo miraba el número del edificio. Ahora descarta objetivos destruidos y elige otro nuevo, incluidas las balistas de fuego.

**Mejor puntería.** El juego deja que una piedra de catapulta de la IA caiga hasta 12 casillas corta y 6 de lado. Ahora la dispersión se reduce a la mitad y se centra en el objetivo (configurable; 100 % mantiene el original). Tus máquinas no cambian.

**Reutilización de emplazamientos de tiendas.** Cuando la tropa se ha ido, el sitio está libre y no hay enemigos cerca para atacar, la IA puede volver a poner una tienda allí. En el juego original el sitio quedaba ocupado toda la partida.

**Tiendas a distancia según alcance.** Las tiendas de catapultas, trabuquetes y balistas de fuego se colocan a entre 0 y 10 casillas (configurable) dentro del alcance desde muros, torres y puertas enemigos, para alcanzar también el interior.

**Los ingenieros siempre llegan a su tienda.** Una entrada bloqueada se mueve a un lado libre y los ingenieros que desistieron o se atascaron vuelven a ser enviados junto con ingenieros inactivos cercanos. Una tienda rodeada de muros recibe ingenieros en cuanto se abre paso.

**Torres de asedio acoplan en más muros.** Cuando el juego no halla lugar, la torre acopla por una esquina contra un muro diagonal o hasta tres casillas más allá en el mismo muro.

**Las torres de asedio de la IA buscan su propio muro.** Una torre inactiva de la IA va al muro acoplable más cercano (en 100 casillas). Si no hay ninguno o no logra llegar, acompaña al ejército como gran escudo —patrullas, escolta de asedio, ejército principal, tiradores al azar o reservas— hasta encontrar muro.

**Soldados a pie viajan en torres de asedio.** Selecciona soldados a pie y haz clic en una de tus torres: hasta 9 suben arriba, pudiendo disparar mientras rueda con la protección de una torre acoplada. No son seleccionables en trayecto y mueren con la torre o quedan sobre ella al acoplar. Haz clic en la torre para desembarcar: el primer clic baja a los pasajeros y el segundo a los ingenieros. Las torres de la IA embarcan a sus tiradores en un radio de 3 casillas.

**Escudos con sus propias tropas.** Los escudos de la IA se reparten uniformemente entre rellenadores de fosos, máquinas a distancia del ejército atacante (nunca las defensivas) y tiradores; las reservas solo reciben escudos si no queda nadie más.

**Ingenieros con aceite solo en suelo.** Los ingenieros —incluidos los tuyos— solo vierten aceite en suelo despejado donde pueda arder, nunca en muros, escaleras o torres. Por sí solos solo atacan enemigos en ese suelo; si les indicas un lugar inválido, buscan suelo cercano en un ángulo de 45 grados o guardan el aceite diciendo «ubicación imposible».

**El aceite se extiende según su cantidad.** Un caldero cubre un número fijo de casillas (41 por defecto) desde el punto elegido. En campo abierto es idéntico al juego original; en pasos estrechos parece varios calderos seguidos. Los edificios inflamables (de chozas a arsenal, iglesia y catedral) pierden hasta un tercio de su salud; muros, torres, puertas y fortalezas no sufren daño.

## Conviene saber

* En multijugador todos necesitan este módulo con los mismos ajustes.
* No se guarda nada en las partidas guardadas.
