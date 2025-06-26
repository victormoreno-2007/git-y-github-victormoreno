# manejo de ramas 🌳
- 🌿 Las ramas en Git son como espacios de trabajo independientes que te permiten organizar y gestionar tu desarrollo de software de manera eficaz, lo que facilita la colaboración y la gestión de versiones en proyectos de cualquier tamaño.

## crear rama 🆕
- 🏗️ cuando inicializamos nuestro repositorio local por defecto ya nos ubica en una rama principal la cual se llama main o master.
• para crear una nueva rama partiendo de la principal es con el comando **git branch + nombre de la nueva rama**

## ver ramas ✨
- 👀 al nosotros tener varias zonas de trabajo como lo son las ramas tenemos la opcion de ver todas las ramas qu tenemos a partir de la rama principal.
• para ver las ramas que parte de la q estamos ubicados es con el comando **git branch**

## movernos a una rama 🏃
- 🔄 si ya bien sabemos que contamos con varias ramas tenemos la oportunidad movernos entre ellas ya sea para hacer cambios o simplemente ver su contenido
• esto lo podemos hacer con el comando **git checkout + nombre de la rama a la que nos dirigimos** o tambien podemos hacerlo con **git switch + nombre de la rama a la que nos dirigimos**

## unir ramas 🧩
- 🔗 cuando nuestro trabajo en una rama a terminado simplemente podemos unirlas, esto hace que el contenido de la rama secundaria se implemente un nuestra rama principal
esto lo podemos hacer de la siguiente manera:
• primero debemos movernos a la rama principal o a la que queremos que se implementen el contenido, luego de ya estar ubicados implementamos el comando **git merge + nombre de la rama secundaria** 

## eliminar ramas ❌
- 🗑️ si luego de unir las ramas o simplemente que su contenido no es para nada util tenemos la opcion de eliminar esa rama para evitar confuciones o tener nuestro repositorio en completo orden
• esto lo podemos hacer con el comando **git branch -d + nombre de la rama a eliminar** con esto aparece un mensaje de confirmacion el cual nos indica que para poder eliminarla por completo utilizamos el comando **git branch -D + nombre de la rama a eliminar** este va despues del primero, sin ninguna interrupcion estre estas dos

## renombrar rama o combiar nombre de rama 🔤
- ✏️ esto se utiliza cuando por equivocacion al crear una rama colocamos el nombre mal o simplemente si por defecto nos coloca la rama principal master pero nosotros queremos que se llame main
• para hacer este cambio utilizamos el comando **git branch -m + nuevo nombre de la rama** esto se utiliza cuando estamos en esa rama
• si estamos en una rama distinta y no queremos viajar hasta alla, simplemente utilizamos el comando **git branch -m + viejo nombre de la rama + nuevo nombre de la rama** y asi cambiamos el nombre de una rama sin estar ubicados en ella.

## enlazar repositorio local con el remoto 🧬
- 🔀 esto consiste en mandar nuestro contenido local a nuestro remoto, por el cual permite acceder desde cualquier parte a nosotros y a compañeros de trabajo.
### pasos para realizarlo ⚙️
1. 🎉 debemos crear nuestro repositorio en el remoto PUBLICO en donde vamos a guardar nuestro contenido que tenemos en el local
2. ✅ debemos verificar nuestros credenciales en el code
3. 👁️ al crear nuestro repositorio el nos muestra una serie de comandos para ejecutar y madar nuestro local al remoto, solo vamos a utilizar los siguientes:
• git remote add origin + URL del repositorio creado
• git branch -M main
• git push -u origin main  
los podemos ejecutar todos a la ves o uno por uno

## manejo de conflictos ⚔️
- 🚨 los conflictos se refiere a que git al intentar unir dos ramas no es capaz de hacerlo por varios factores, puede ser por tener dos versiones del mismo archivo o simplemente que la rama principal esta mas adelantada que la rama secundaria.
### solucion ✅
1. 🔍 detectar el conflicto con el comando **git pull** o **git merge** luego de hacer el commit 
2. 📺 al git marcar o mostrar los archivos en conflicto debemos editar a lo que consideremos mas viable
3. ➕ ya una ves editado se agrega el archivo al staging area se realiza un commit de la solucion
