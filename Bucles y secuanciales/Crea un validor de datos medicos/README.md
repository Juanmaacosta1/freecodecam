Declara una variable llamada medical_records y asígnale una lista vacía. En los siguientes pasos, la vas a usar para almacenar tus datos médicos.
La lista medical_records almacenará diccionarios, cada uno representando a un paciente. Agrega un diccionario con una clave patient_id y un valor de la cadena P1001 a la lista medical_records.
Agrega una clave age con el valor del entero 34 y una clave gender con el valor de la cadena Female a tu diccionario. No olvides la coma entre los pares clave-valor.
Una clave diagnosis con el valor de Hypertension
Una clave medications con el valor de la lista ['Lisinopril']
Una clave last_visit_id con el valor de V2301
iguiendo la misma estructura que usaste en los pasos anteriores, la lista medical_records ha sido completada para ti con los datos de otros pacientes. Siéntete libre de echarle un vistazo.

A continuación comenzarás a escribir la función para validar el conjunto de datos. Crea una función llamada validate con un solo parámetro data.

Quieres asegurarte de que tus datos sean una lista o una tupla. Por lo tanto, dentro de la función validate, declara una variable llamada is_sequence y asígnale una llamada a isinstance. Pasa data como el primer argumento y una tupla que contiene list y tuple como el segundo argumento.
Crea una estructura if. Para su condición, usa el operador not para negar is_sequence. Dentro de la estructura if, imprime Invalid format: expected a list or tuple. y retorna False.
Justo después de tu sentencia if, declara una variable llamada is_invalid y asígnale False. Más adelante, la usarás como una bandera para ejecutar una sentencia condicional.
Crea un ciclo for que itere sobre data. Usa la función enumerate para obtener tanto el índice como el elemento en data en cada iteración. Usa index y dictionary como variables de iteración.

Por ahora usa pass para llenar el cuerpo del ciclo.
Dentro de tu ciclo for, si el elemento en dictionary no es una instancia de dict, imprime Invalid format: expected a dictionary at position <index>. (donde <index> debe ser reemplazado por el índice actual) y asigna True a is_invalid
Después de tu ciclo for, aún dentro de la función validate, crea una estructura if. Si is_invalid es True, devuelve False.
Al final de tu código, llama a la función validate con medical_records como argumento. Deberías ver Valid format. impreso en el terminal.
Para probar la primera estructura if de tu función, convierte medical_records en una cadena. Deberías ver Invalid format: expected a list or tuple. impreso en el terminal.Ahora convierte medical_records de nuevo en una lista/tupla de diccionarios.

Para probar la segunda estructura condicional, agrega dos elementos de tu elección que no sean diccionarios al final de la lista medical_records. Deberías ver dos mensajes de validación impresos en el terminal.
Ahora que probaste la validación para esta parte, elimina los últimos dos elementos de la lista medical_records.Vas a usar un conjunto para asegurarte de que cada diccionario no contenga claves adicionales o mal escritas.

Dentro de la función validate, usa la estructura set() para crear un conjunto a partir de la siguiente lista de claves que cada diccionario debe tener: ['patient_id', 'age', 'gender', 'diagnosis', 'medications', 'last_visit_id']. Asigna el conjunto a una variable llamada key_set.
Dentro de tu ciclo for, después de la primera sentencia if, crea una sentencia if que se ejecute cuando el conjunto de claves del diccionario actual sea diferente de key_set. Esto es para asegurar que no haya claves faltantes o inválidas en el diccionario.

Dentro de la nueva estructura if, imprime Invalid format: <dictionary> at position <index> has missing and/or invalid keys. (donde <dictionary> y <index> deben ser reemplazados por el diccionario y el índice en la iteración actual) y asigna True a is_invalid.Para probar que todo funciona correctamente, intenta comentar la clave age del primer diccionario en medical_records.

Deberías ver un mensaje de validación aparecer en el terminal.
Ahora restaura la línea 'age': 34,.

Ahora vas a hacer que la validación sea más granular. Crea una función llamada find_invalid_records para encontrar valores inválidos en un diccionario. Dale los siguientes parámetros: patient_id, age, gender, diagnosis, medications, last_visit_id.

Dentro de tu nueva función, crea un diccionario vacío llamado constraints. Luego, devuelve constraints desde tu nueva función.
En el ejemplo anterior, sum(**nums) es equivalente a sum(a=2, b=4, c=1).

Al final de tu código, imprime el resultado de llamar a la función find_invalid_records. Para sus argumentos, usa el operador ** para desempaquetar medical_records[0].
El diccionario constraints contendrá cada clave que debes esperar tener en los datos para validar. El valor asociado a cada una indicará el resultado de la validación.

Agrega la clave patient_id al diccionario constraints. Para su valor, usa una llamada a isinstance pasando patient_id y str como argumentos.
Como escribiste en el paso anterior, patient_id debería ser una cadena. Sin embargo, quieres verificar que también tenga un patrón específico.

Para eso, vas a usar una expresión regular. Por lo tanto, en la parte superior de tu código, usa la palabra clave import para importar el módulo re.

Agrega re.IGNORECASE como el tercer argumento a tu llamada re.search. Esto hará que tu búsqueda con regex no distinga entre mayúsculas y minúsculas.

Después de eso, verás que None es reemplazado por el objeto de coincidencia <re.Match object; span=(0, 1), match='P'>, donde match indica la coincidencia y span indica su ubicación en la cadena.Después de la letra p, patient_id debe tener una serie de números. Entonces, modifica tu patrón regex para que tenga el carácter p seguido de la secuencia especial \d.Entonces añade un cuantificador + a tu patrón regex para que coincida con uno o más dígitos.Reemplaza la llamada search con una llamada fullmatch manteniendo los mismos argumentos.A continuación, quieres verificar que age sea un entero. Así que agrega otra clave age al diccionario constraints. Para su valor, llama a isinstance pasando age e int como sus argumentos.age no solo debe ser un entero, debe ser un entero positivo mayor o igual a 18.

Usando el operador and, añade una segunda expresión al valor de la clave age para verificar eso.Agrega otra clave gender al diccionario constraints. Siguiendo el formato de la expresión que escribiste en los pasos anteriores, verifica que gender sea una cadena. Luego, usa el operador and para comprobar que el gender en minúsculas esté en ('male', 'female').Ahora agrega una clave diagnosis al diccionario constraints. Para su valor, escribe una expresión que verifique que diagnosis sea una instancia de str o sea None.A continuación, agrega una clave medications al diccionario constraints. Para su valor, usa isinstance para verificar que medications sea una lista.
Cada elemento en la lista medications debe ser una cadena. En este paso y en el siguiente escribirás una expresión para verificar eso. Usa el operador and para agregar otra expresión al valor de la clave medications.

En el lado derecho del operador and, usa la sintaxis de comprensión de listas para crear una lista evaluando isinstance(i, str) para cada i en medications.Pasa la lista [isinstance(i, str) for i in medications] a la función all para asegurarte de que cada elemento en ella sea una cadena.
Pasa la lista [isinstance(i, str) for i in medications] a la función all para asegurarte de que cada elemento en ella sea una cadena.Agrega una última clave last_visit_id al diccionario constraints. Para su valor, usa isinstance para verificar que last_visit_id sea una cadena.Ahora que tu diccionario constraints está completo, cambiarás la sentencia return de find_invalid_records para que devuelva una lista de las claves inválidas.

Usando la sintaxis de comprensión de listas, devuelve una lista que evalúa key para cada key, value en constraints.items().Como quieres devolver una lista que contenga solo las claves inválidas, agrega una cláusula if a tu comprensión para que cada key se agregue a la lista solo cuando value sea falsoLa función find_invalid_records está completa. Ahora, elimina print(find_invalid_records(**medical_records[0])) de tu código.
Volviendo a la función validate, después de las dos sentencias if y aún dentro del ciclo for, crea una variable llamada invalid_records.

Luego, asígnale una llamada a find_invalid_records usando el operador ** para desempaquetar dictionary.Si pasas datos inválidos a la función validate, por ejemplo una lista que contiene elementos que no son diccionarios o diccionarios con claves faltantes y/o inválidas, Python generará un AttributeError y un TypeError, respectivamente. Siéntete libre de verificarlo modificando la lista medical_records.

Para evitar eso, después de establecer is_invalid en True, usa la palabra clave continue para saltar a la siguiente iteración en ambas sentencias if.