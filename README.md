# nodejs-first-project

1)	Modulo “filesystem”:
Me permite trabajar con archivos, también crearlos, escribir código dentro de ellos y trabajar con archivos de texto plano.
Como se usa:
•	Para leer un archivo:
Utilizamos readFile(path, callback) para leer el contenido de un archivo.
•	Para escribir un archivo:
Utilizamos writeFile(path, data , callback) para escribir datos en un archivo.
(si el archivo no existe, lo crea)
•	Para escribir sobre un archivo:
appendFile(path, data, callback) para agregar contenido a un archive previamente creado.

2)	¿Qué es middleware y cuál es su propósito?
El middleware es un tipo de software que se ubica entre el sistema operativo y las aplicaciones que se ejecutan en él. Su función principal es facilitar la comunicación y el intercambio de datos entre diferentes aplicaciones, sistemas y bases de datos. Imagina que actúa como un mediador que asegura la integración y conexión constante entre los componentes. En resumen, permite que las aplicaciones distribuidas se comuniquen entre sí y compartan información.
3)	¿Qué es un endpoint en una API RESTful y cuál es su función?
En el contexto de una API RESTful, un endpoint se refiere a una URL específica donde la API puede acceder a los recursos que necesita1. Cada endpoint está asociado con una funcionalidad particular ofrecida por la API, lo que permite a los clientes recuperar, crear, actualizar o eliminar recursos de datos2. En resumen, los endpoints son los puntos de acceso designados para interactuar con una API y sus recursos. 
4)	¿Qué son los verbos HTTP y cuáles son los más comunes?
Los verbos HTTP, también conocidos como métodos HTTP, son acciones estándar utilizadas para operar sobre recursos en una arquitectura RESTful. Los más comunes son:
GET: Se utiliza para recuperar información de un recurso sin modificarlo. Es seguro y debe ser idempotente (aquel que cuando se aplica varias veces, no cambia el estado del servidor más allá de la primera solicitud).
POST: Crea un nuevo recurso o subordinado. No es seguro ni idempotente 
PUT: Actualiza un recurso existente o crea uno si no existe. Debe ser idempotente.
DELETE: Elimina un recurso. También debe ser idempotente.
PATCH: Aplica modificaciones parciales a un recurso existente. 
6)
JSON (JavaScript Object Notation) es un formato ligero y legible para representar datos estructurados. Se utiliza ampliamente en las API RESTful debido a sus ventajas:
1.	Legibilidad: JSON es fácil de entender tanto para los desarrolladores como para las máquinas.
2.	Ligereza: Los datos en formato JSON son compactos, lo que reduce la sobrecarga de la red.
3.	Soporte universal: Casi todos los lenguajes de programación pueden analizar y generar JSON.
4.	Independencia de plataforma: Funciona en diferentes sistemas operativos y dispositivos.
5.	Flexibilidad: Puede representar objetos, listas, números, cadenas, booleanos y valores nulos.
En resumen, JSON es una excelente opción para intercambiar datos entre aplicaciones debido a su simplicidad y compatibilidad. 
6.1) ¿Qué es el body de una petición HTTP?
El body de una petición HTTP es la parte donde se envían datos adicionales junto con la solicitud. En una petición POST, PUT o PATCH, el body contiene información que se debe procesar en el servidor. Por ejemplo, al crear un nuevo recurso en una API RESTful, los detalles del recurso (como nombre, descripción, etc.) se incluyen en el body de la solicitud. En resumen, el body es como un paquete de datos que viaja junto con la solicitud HTTP. 
6.2) ¿Qué es el body de una respuesta HTTP?
El body de una respuesta HTTP contiene los datos enviados por el servidor en respuesta a una solicitud. Por ejemplo, cuando solicitas información de un recurso (mediante GET), el servidor envía los detalles del recurso en el body de la respuesta. Los datos pueden estar en formato JSON, XML u otros. En resumen, el body es la parte de la respuesta que contiene la información relevante que el cliente necesita procesar.
6.3) ¿Qué es el query de una petición HTTP?
El query en una petición HTTP se refiere a los parámetros que se envían junto con la URL para especificar detalles adicionales. Por ejemplo, en una solicitud GET, los parámetros de consulta se agregan a la URL después del signo de interrogación (?). Estos parámetros pueden incluir filtros, criterios de búsqueda o valores específicos. Si la información es extensa, se puede incluir en el body de la solicitud en lugar de la URL.
6.4) ¿Qué es el params de una petición HTTP?
En una petición HTTP, los parámetros se envían de diferentes maneras según el método utilizado:
GET: Los parámetros se incluyen en la URL como una cadena de consulta, por ejemplo: http://ejemplo.com/recurso?parametro=valor&otro=otro_valor1.
1.	POST: Los valores se envían en el cuerpo de la solicitud. El formato depende del tipo de contenido especificado. Por lo general, se utiliza application/x-www-form-urlencoded, similar a la cadena de consulta: parametro=valor&otro=otro_valor. Si hay una carga más compleja, como una carga de archivos, se utiliza multipart/form-data.
En resumen, los parámetros permiten que el cliente pase datos a la API de manera simple y estandarizada. 
7.1) ¿Qué es un verbo POST y cuál es su propósito? 
El verbo POST en una petición HTTP se utiliza para enviar datos al servidor. Su propósito principal es crear recursos nuevos. Cuando realizas una solicitud POST, estás indicando que deseas agregar un nuevo recurso a una colección existente. Por ejemplo, al completar y enviar un formulario de contacto en un sitio web, estás utilizando una petición POST para que el servidor reciba esa información. En resumen, el método POST está diseñado para:
1.	Crear recursos nuevos.
2.	Modificar recursos existentes.
3.	Publicar mensajes en tablones de anuncios, grupos de noticias o listas de correos.
4.	Agregar nuevos usuarios a través de formularios de suscripción.
5.	Proporcionar conjuntos de datos como resultado del envío de formularios.
6.	Extender bases de datos mediante operaciones de concatenación.
7.2) ¿En qué se diferencia un verbo POST de los otros verbos HTTP como GET, PUT Y DELETE?
Los verbos HTTP, como GET, POST, PUT y DELETE, tienen diferentes propósitos y se utilizan en situaciones específicas. Aquí están las diferencias clave:
1.	GET: Se utiliza para recuperar datos del servidor. No debe tener efectos secundarios ni alterar el estado del recurso. Por ejemplo, obtener información de una página web.
2.	POST: Sirve para enviar datos al servidor. Se utiliza para crear recursos nuevos o modificar recursos existentes. Por ejemplo, enviar un formulario con datos de usuario.
3.	PUT: Reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición. Se utiliza para actualizar recursos existentes. Por ejemplo, modificar información de un usuario.
4.	DELETE: Borra un recurso específico. Se utiliza para eliminar recursos. Por ejemplo, eliminar una publicación de un blog.
7.3) ¿Cómo se envían datos en un verbo POST?
Cuando se envía un formulario HTML mediante el método POST, los datos se transmiten en el cuerpo de la solicitud HTTP. A diferencia del método GET, donde los datos se incluyen en la URL, en POST no son visibles en la URL y no tienen una longitud limitada. Principalmente, POST se utiliza para enviar información al servidor, como formularios, contraseñas u otros datos sensibles. 
8.1) ¿Qué es un verbo GET y cuál es su propósito?
El verbo GET en una petición HTTP se utiliza para recuperar datos del servidor. Su propósito principal es obtener información sin alterar el estado del recurso. 
En resumen, el método GET se emplea para obtener datos sin modificar nada en el servidor. Si tienes más preguntas, no dudes en preguntar. 
8.2) ¿En qué se diferencia el verbo GET de los otros verbos HTTP?
Los verbos HTTP, como GET, POST, PUT y DELETE, tienen diferentes propósitos y se utilizan en situaciones específicas. Aquí están las diferencias clave:
1.	GET: Se utiliza para recuperar datos del servidor. No debe tener efectos secundarios ni alterar el estado del recurso. Por ejemplo, obtener información de una página web.
2.	POST: Sirve para enviar datos al servidor. Se utiliza para crear recursos nuevos o modificar recursos existentes. Por ejemplo, enviar un formulario con datos de usuario.
3.	PUT: Reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición. Se utiliza para actualizar recursos existentes. Por ejemplo, modificar información de un usuario.
4.	DELETE: Borra un recurso específico. Se utiliza para eliminar recursos. Por ejemplo, eliminar una publicación de un blog.
9.1) ¿Qué es un verbo PUT y cuál es su propósito?
El verbo PUT en una petición HTTP se utiliza para reemplazar completamente un recurso en el servidor. Cuando realizas una solicitud PUT, estás indicando que deseas sustituir el recurso en su totalidad con la información proporcionada en la solicitud. En resumen, el método PUT se emplea para:
1.	Reemplazar completamente un recurso existente.
2.	Actualizar la representación completa de un recurso.

9.2) ¿En qué se diferencia el verbo PUT de los otros verbos HTTP?
1.	GET: Se utiliza para recuperar datos del servidor. No debe tener efectos secundarios ni alterar el estado del recurso. Por ejemplo, obtener información de una página web.
2.	POST: Sirve para enviar datos al servidor. Se utiliza para crear recursos nuevos o modificar recursos existentes. Por ejemplo, enviar un formulario con datos de usuario.
3.	PUT: Reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición. Se utiliza para actualizar recursos existentes. Por ejemplo, modificar información de un usuario.
4.	DELETE: Borra un recurso específico. Se utiliza para eliminar recursos. Por ejemplo, eliminar una publicación de un blog.
10.1) ¿Qué es un verbo DELETE y cuál es su propósito?
El verbo DELETE en una petición HTTP se utiliza para borrar un recurso específico. Cuando realizas una solicitud DELETE, estás indicando que deseas eliminar un recurso en particular. Por ejemplo, si deseas eliminar una publicación de un blog o un archivo en un servidor, usarías una petición DELETE1. Si tienes más preguntas, no dudes en preguntar. 
10.2) ¿En qué se diferencia el verbo DELETE de los otros verbos HTTP?
5.	GET: Se utiliza para recuperar datos del servidor. No debe tener efectos secundarios ni alterar el estado del recurso. Por ejemplo, obtener información de una página web.
6.	POST: Sirve para enviar datos al servidor. Se utiliza para crear recursos nuevos o modificar recursos existentes. Por ejemplo, enviar un formulario con datos de usuario.
7.	PUT: Reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición. Se utiliza para actualizar recursos existentes. Por ejemplo, modificar información de un usuario.
8.	DELETE: Borra un recurso específico. Se utiliza para eliminar recursos. Por ejemplo, eliminar una publicación de un blog.
11) ¿Qué es un status code y cuáles son los más comunes?
Los códigos de estado HTTP indican si una solicitud específica se ha completado con éxito. Estos códigos se agrupan en cinco clases1:
1.	Respuestas informativas (100 – 199): Indican que el servidor aún está procesando la solicitud, pero rara vez se utilizan.
2.	Respuestas exitosas (200 – 299): 
o	200 OK: La solicitud tuvo éxito, y el servidor devolvió los datos solicitados.
o	201 Created: La solicitud fue exitosa, y se creó un nuevo recurso.
3.	Mensajes de redirección (300 – 399).
4.	Respuestas de error del cliente (400 – 499).
5.	Respuestas de error del servidor (500 – 599).

12) ¿Cuáles son los status code más comunes para el verbo POST?
Los códigos de estado HTTP más comunes para el verbo POST son:
1.	200 OK: Indica que la solicitud fue exitosa y el servidor devolvió los datos solicitados. En el caso de POST, la respuesta puede incluir información sobre el recurso creado o modificado1.
2.	201 Created: Se envía después de las solicitudes POST y significa que se creó un nuevo recurso con éxito2.

13) ¿Cuáles son los status code más comunes para el verbo GET?
Los códigos de estado de respuesta HTTP indican si se ha completado satisfactoriamente una solicitud HTTP específica. Aquí están algunos de los más comunes relacionados con el verbo “GET”:
1.	200 OK: La solicitud ha tenido éxito. En el contexto de una petición HTTP, esto significa que el recurso solicitado se encontró y se transmite en el cuerpo del mensaje 12.
2.	204 No Content: La petición se ha completado con éxito, pero su respuesta no tiene ningún contenido. Aunque los encabezados pueden ser útiles, el cuerpo del mensaje está vacío 1.
3.	304 Not Modified: Indica que el recurso no ha cambiado desde la última vez que se solicitó. El cliente puede usar su caché local sin descargar el recurso nuevamente 1.
4.	400 Bad Request: Se produce cuando la solicitud del cliente es incorrecta o no se puede procesar por parte del servidor 1.
5.	404 Not Found: El servidor no pudo encontrar el recurso solicitado 1.
6.	401 Unauthorized: El cliente no se identificó ni se verificó a sí mismo cuando fue necesario 3.

14) ¿Cuáles son los status code más comunes para el verbo PUT?
Los códigos de estado de respuesta HTTP relacionados con el verbo “PUT” son los siguientes:
1.	200 OK: Indica que la solicitud ha tenido éxito. Es típicamente la respuesta enviada después de una petición PUT, cuando se ha creado un nuevo recurso 1.
2.	201 Created: La solicitud ha tenido éxito y se ha creado un nuevo recurso como resultado de ella 1.
3.	202 Accepted: La solicitud se ha recibido, pero aún no se ha actuado. Es una petición “sin compromiso”, lo que significa que no hay manera en HTTP que permite enviar una respuesta asíncrona que indique el resultado del procesamiento de la solicitud 1.
4.	204 No Content: La petición se ha completado con éxito, pero su respuesta no tiene ningún contenido. Aunque los encabezados pueden ser útiles, el cuerpo del mensaje está vacío 1.

15) ¿Cuáles son los status code más comunes para el verbo DELETE?
Los códigos de estado de respuesta HTTP relacionados con el verbo “DELETE” son los siguientes:
1.	200 OK: Indica que la solicitud ha tenido éxito. En el contexto de una petición DELETE, esto significa que el recurso se ha eliminado correctamente 1.
2.	202 Accepted: La solicitud se ha recibido, pero aún no se ha ejecutado completamente. Este código se utiliza cuando la acción ha sido aceptada por el servidor, pero no se ha aplicado por completo 2.
3.	204 No Content: La petición se ha completado con éxito, pero su respuesta no tiene ningún contenido. Aunque los encabezados pueden ser útiles, el cuerpo del mensaje está vacío .










