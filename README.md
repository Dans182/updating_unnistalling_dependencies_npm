# react-base

En este proyecto, cloné el repositorio, el cual ya tiene años de haber sido creado y tiene las dependencias desactualizadas.

git clone 
npm list => Acá me muestra un listado de dependencias, pero estas me arrojan errores, y claro. Son dependencias que existe en el repositorio pero no están instaladas en el mismo.

Procedo a hacer el npm install, para que me instale todas las dependencias existentes en el package.json del repositorio clonado.

Después npm outdate => sirve para ver todo el arbol de versiones de las dependencias que tenemos instaladas. De esta manera, vemos si efectivamente existen versiones posteriores y mas actualizadas a la que tenemos instalada.

Acá procedemos a ir, dependencia por dependencia, actualizandola con el comando npm install <paquete>@latest

En nuestro proyecto ya corriendo, podemos hacer uso de npm install para hacer un review de las vulnerabilidades.

npm audit --> Audita las dependencias que tenemos instaladas en busca de vulnerabilidades.

npm audit fix --> Audita e intenta arreglar las vulnerabilidades de nuestras dependencias.

npm audit --json --> Muestra los resultados de la auditoría a manera más profunda en formato json.

npm audit fix --force --> Corrige los problemas encontrados en las librerías instalando otras dependencias por debajo si es necesario.

Muchas de las vulnerabilidades que aparecen se deben a que las dependencias se encuentran desactualizadas. Es por ello que debemos intentar que todo se actualice a la ultima version.

Para eliminar dependencias ya instaladas puedes o ejecutar el comando npm uninstall <nombre-paquete> o directamente meterte en el archivo package.json de tu proyecto y eliminar del listado de dependencias la línea del nombre de la dependencia que queremos eliminar. Posteriormente ejecutamos

rm -rf node_modules/ => para eliminar toda la carpeta de node_modules y así depurar y recompilar todo lo que no se usa, y volvemos a ejecutar: npm install

rm (remove)

con ls listamos todo lo que tengo en mi directorio y con ls -l me lo muestra en vertical.



Para compilar el proyecto y prepararlo para producción usamos:

npm run build

Para compilar el proyecto y obtener mas informacion usamos

npm run build --dd

Para ver librerias que tenemos instaladas en nuestro proyecto que se encuentran deprecadas o que ya no tendrán actualizaciones.
Este comando tambien sincroniza lo que es mi package.json con mi package-lock.

npm ci



♻️ npm uninstall babel-eslint --> *babel-eslint* es solo un paquete de ejemplo, este comando borra la dependecia junto con todo su arbol de sub-dependencias

☠️ Borrar las dependencias desde el archivo de 📦package.json📦 posterior a esto es 
⚠️IMPORTANTE⚠️ borrar la carpeta node_modules con rm -r node_modules y hacer una reinstalacion limpia via "npm install"

Este proceso es necesario cuando se le esta haciendo una "limpia al proyecto" xd para posteriomente hacerle un REFACTOR tambien suele suceder cuando se trabaja con proyectos de prueba 

* npm run build --> Este comando prepara el proyecto para produccion

* npm run build --dd  --> Activa el modo Verbose, nos muestra una informacion mas robusta de lo que esta haciendo o de lo que ejecutarse el comando a la hora de ejecutar el build, asi en dado caso que el proyecto se rompa o una dependencia este mal instala da con esta opcion es mas facil identificar el problema.

*npm ci  => Muestra mensajes como librerias deprecadas o que dejaran de tener soporte, tambien sincroniza 📦package.json📦 con el 📦package-lock.json🔐

¿Que es el 📦package-lock.json🔐?
Este archivo contiene toda la informacion necesaria de cada uno de lo elementos del proyecto, en palabras mas sencillas el 📦package-lock.json🔐 tiene todo el arbol🌳 de dependencias y SUBdependencias que el proyecto tiene, este archivo toma mas relevancia cuando el proyecto se tiene que compilar en la nube o en un servevidor externo 