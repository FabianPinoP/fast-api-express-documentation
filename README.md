![Descargas](https://img.shields.io/npm/dm/express-swift-api.svg)


🚀 ¡Bienvenido a express-swift-api! 🚀

Este paquete te ayuda a crear un proyecto desde cero en cuestión de segundos. Olvídate de las tareas tediosas al iniciar un proyecto, con express-swift-api podrás crear un proyecto completo, incluyendo la configuración de la base de datos y las operaciones principales. Además, cuenta con generadores automáticos de controladores, modelos y rutas. ¡Genial! Tú solo debes preocuparte por la lógica de tu proyecto. La API se construye con Express y otras librerías que te permiten comenzar a usar tu nuevo proyecto rápidamente.

¡Comencemos...!!

❗️ Pasos previos
Antes de comenzar, asegúrate de tener instalado Node.js v-16 en adelante en tu sistema.

Instala el packete
```bash
npm install -g express-swift-api
```
Si quieres colaborar 
Antes debes solicitar acceso al proyecto
Descarga el proyecto para testear y ejecuta los siguientes comandos en la terminal:
```bash
cd express-swift-api
npm install
npm link
```

❓ Modo de uso
Para ejecutar cualquier opción, llama al paquete desde la línea de comandos de la siguiente manera:

```bash
express-swift-api "acción a realizar"
```
⚙️ Acciones disponibles
new: Crea un nuevo proyecto API con la estructura predefinida. Incluye carpetas como node_modules, src, .env, package-lock.json y package.json.

create-database name_database: Crea una base de datos con el nombre proporcionado en el archivo .env. Asegúrate de haber configurado previamente las credenciales de tu base de datos en ese archivo.

create-table: Crea una tabla en la base de datos. Debes ingresar el nombre de la tabla y sus atributos. La tabla se generará automáticamente con un campo id como clave primaria (SERIAL PK).

add-references: Crea relaciones entre tablas. Genera automáticamente el atributo en la tabla que servirá como clave externa (FK). El formato del nombre será: tabla_referenciada_id. Por ejemplo, si tienes una tabla users y una tabla comments, se generará el atributo users_id en la tabla comments como una FK que referencia a users a través de su id.

add-column: Agrega una columna y su tipo de dato a una tabla existente.

drop-column: Elimina una columna de una tabla existente.

rename-column: Cambia el nombre y el tipo de dato de una columna en una tabla existente.

delete-cascade: Agrega una opción de borrado en cascada (CASCADE) en la clave externa (FK) de una tabla.

🔍 Prueba tu proyecto
Después de crear el proyecto, ejecuta el siguiente comando para iniciar el servidor:

```bash
npm run dev
```
Asegúrate de que el servidor se esté ejecutando correctamente.

Realiza una solicitud a la siguiente URL para probar el endpoint de ejemplo:

```bash
http://localhost:3000/indexExample
```
Deberías obtener la siguiente respuesta:

```javascript
{ "message": "Esto es un controlador de ejemplo" }
```
Si todo funciona correctamente, ¡estás listo para comenzar a desarrollar tu proyecto!

📚 Generando modelos y controladores
Generando modelos (g-model): Esta acción generará un archivo .js en la carpeta models. El archivo contendrá funciones vacías y la conexión a la base de datos. Solo encontrarás el esqueleto de las funciones, para que puedas agregar tu lógica personalizada. El nombre del archivo se basará en la entidad ingresada. Además, se creará una tabla en la base de datos con los atributos y tipos de datos especificados. La tabla seguirá el mismo criterio del modelo. Cada tabla se creará con un campo id como clave primaria (SERIAL PK), esto ya está configurado previamente.
⚠️ Es importante tener tus credenciales de base de datos ingresadas en el archivo .env y asegurarte de que la base de datos ya esté creada y que su nombre también esté especificado en el archivo .env para generar las tablas correctamente.

No olvides importar tus funciones de modelo en el controlador correspondiente.

Generando controladores (g-controller): Esta acción generará un controlador con extensión .js y las rutas GET, POST, PUT y DELETE predefinidas. El nombre del controlador se basará en la entidad ingresada. Se crearán funciones vacías para que puedas implementar tu lógica personalizada. ¡No te preocupes por importar las rutas, nosotros nos encargamos de ello!


🌟 ¡Espero que encuentres útil esta herramienta! Estaré trabajando continuamente para agregar más acciones y facilitar aún más tu experiencia de desarrollo. ¡Diviértete programando! 🎉😃
