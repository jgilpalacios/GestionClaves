# GestionClaves
para gestionar las claves en archivos encriptados.
Se utilizan dos claves:
   Clave maestra: Una clave que deberemos memorizar para poder utilizar este sistema.
   Clave encriptadora: Una clave larga (si se pulsa el botón EncNueva se genera una clave de 256 caracteres elegidos al azar).
El sistema funciona añadiendo tarjetas (+ del menu general)con los datos de nuestras claves en una tarjeta vacía (basicamente datos que identifican incluido URL si es de un sitio) y la clave que se puede poner a mano o bien que se genere al azar usando el boton + del pie de la tarjeta (con la configuración definida tambien al pie (tipo de caracteres y numero de caracteres)). Una tarjeta se elimina con el boton - del pie de la tarjeta.

Una vez definidas la clave maestra, la clave encriptadora y las tarjetas con nuestras claves, el botón "guarda" nos descarga dos archivos de texto: uno de ellos contiene los datos de nuestras claves encriptados AES con la clave maestra y la encriptadora (fk....). El otro archivo de texto (fd....) contiene la clave encriptadora encriptada AES con la clave maestra.
Para mantener seguras nuestras claves estos archivos se deberían guardar en soportes diferentes.
Caso de substracción del soporte con el archivo que contiene nuestras claves el substractor no podría acceder a ellas al no conocer la clave maestra ni la clave decriptadora. 
Si se sustrajera solo el soporte con la clave decriptadora, nuestras claves no estarían compormetidas ya que no contiene informacion sobre las mismas. 
En el caso de que el substactor tuviera ambos archivos, todavía estarían protegidos ya que no tendría la clave maestra.

Normalmente para obtener nuestras claves deberemos cargar dichos archivos con los exploradores de archivo  de la cabecera de la pagina, introducier la clave maestra en el espacio "introducier nuestra clave personal" y pulsar el boton "desencripta". Apareceran las tarjetas con los datos de nuestras claves. Se puede pasar a verlas como tabla o tarjetas pulsando el selector (bloques/tablas), tambien se pueden exportar a un csv en texto plano pulsando (aCSV), SE DEBE TENER PRECAUCIÓN CON ESTE CSV.

Una vez desencriptadas, se pueden modificar los datos de cualquier tarjeta/fila de la tabla, se puede eliminar cualquier tarjeta/fila, así como se pueden añadir nuevas claves (boton +). Pulsando guardar se vuelven a generar los dos nuevos archivos con las claves actuales.

fin