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

