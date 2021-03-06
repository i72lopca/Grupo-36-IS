## Diagrama de secuencia 03 modificar alumno

Comienza cuando el profesor solicita modificar los datos de un alumno. La interfaz pregunta que opción de búsqueda desea ejecutar y el profesor la indica, luego pide los datos del alumno al usuario, y los envía a la base de datos que procede a su búsqueda. Se inicia un bloque **ALT**.
* Si el alumno ha sido encontrado, se le pide al profesor que modifique los datos que considere oportunos. El sistema comprueba en un bucle **LOOP** que la modificación es válida, saliendo del mismo cuando ha sido correcta.

Si se modifican datos opcionales, relacionados con la gestión de líderes, entraríamos en un bloque **OPT** con un bloque **ALT** dentro de este.
  * Si el grupo tiene líder, permite que se modifique el líder.
  * Si el grupo no posee líder, devuelve un mensaje de que el grupo no tiene líder, y pasa a modificar otros datos opcionales. Finalizan ambos bucles. 
  
  Se comprobará que las modificaciones son válidas, iniciando un bloque **ALT** con un efecto u otro dependiendo del resultado de esta comprobación.
  
  * Si son válidas, se procede a modificar los datos en la base de datos, y se devuelve un mensaje de confirmacion.
  * Si no son válidas, devuelve un mensaje de error y continua en el bucle hasta que se corrija la validez de las modificaciones.
* Si el alumno no ha sido encontrado, devuelve un mensaje de error indicando que no se ha encontrado un alumno que cumpla los criterios de búsqueda.
