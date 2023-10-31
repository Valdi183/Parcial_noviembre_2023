### PARCIAL_NOVIEMBRE_2023
Pregunta_1: Un pull request es una solicitud de fusión (merge) donde solicitas fusionar una rama en la que tu has trabajado, al repositorio principal que has bifurcado con un fork, es decir, al bifurcar un repositorio estas copiando ese repositorio tal cual (en remototo, GitHub) y te lo estás llevando para trabajar con él sin modificar el original. Una vez termines de modificar lo que tuvieses que modificar y hacer un git commit con esos cambios. Tienes la opción de hacer un pull request para que el "dueño" del repositorio original, fusione tus modificaciones y las añada al repositorio original si acepta ese pull request.

Pregunta_2: Un conflicto de fusión, aparece a veces tras ejecutar un git merge. Esto sucede cuando por ejemplo se están fusionando 2 ramas que no son del todo compatibles. Por ejemplo, si ambas ramas tienen un archivo README, con una breve descripción del proyecto, pero en una hay fallos de ortografía (espacios extras etc.) Surgirá un conflicto que nos saltará como si fuese un pequeño error en la consola. Esto simplemente pausará el merge, y nos pedirá que solucionemos los conflictos para poder continuar con el merge. Para ello, podemos solucionar los conflictos manualmente entrando en el/los archivos que hayan tenido conflicto con un editor como puede ser nano (nano README.md si seguimos el ejemplo anterior) borrando lo sobrante, (normalmente aparecen signos como <<<<<<<< o varios guiones -------- sin sentido). Una vez hechos los coambios, ejecutamos git add . (para añadir los cambios) y por último, git merge --continue para terminar con el merge.

Pregunta_3: Para fusionar ambas ramas, primero nos posicionamos en la rama "examen_parcial" con git checkout examen_parcial y ejecutamos desde esa rama git merge main. Solucionamos los conflictos si hubiese como expliqué en la pregunta anterior, y terminamos cambiandonos a la rama "main" haciendo lo mismo desde esa rama (ejecutamos git merge examen_parcial y solucionamos conflictos si los hubiese).

Pregunta_4: Tras hacer un commit erroneo, podemos hacer varias cosas. Si se trata de unas simples modificaciones erroneas de un archivo, podemos editar ese archivo, añadir los cambios (git add "nombre del archivo") y subir los cambios (git commit -m "mensaje que explique los cambios"). En cambio, si se tata de un commit que resulta ser una "cagada", podemos simplemente ejecutar un git reset --hard <hash del commit> el hash (id) del commit, debe ser justo el commit anterior al commit erroeno, de esa forma volveremos al estado del proyecto anterior a ese commit.

Pregunta_5: Para realizar el fork, tan solo tienes que visitar el repositorio que quieres copiar, y allí, veras la opción de fork (bifurcar). El fork como he explicado anteriormente de forma breve para definir el concepto "pull request", se utiliza normalmente para trabajar en proyectos de software grupales. Al hacer un fork a un repositorio (en GitHub), estás haciendo una copia de este y te lo estás llevando a tu cuenta de GitHub, de forma que puedas realizar las modificaciones que deseas sin modificar el repositorio original. De esta forma puedes colaborar en un proyecto con varias personas, donde todas, tengan una copia del repositorio original con un fork, y puedan trabajar de forma simultánea, realizando varias modificaciones independientes sin afectar al repositorio original.

Pregunta_6 a): Me encuentro en el directorio raíz, definido como home o /. Para llegar al archivo.txt desde allí, tengo que seguir lo que se dice la ruta absoluta, es decir, tengo que ir desde el directorio raíz hasta mi destino. Para ello, puedo ejecutar el comando cd ~/nombre del alumno/Universidad/UAX. De esta forma, estaría dentro del directorio que contiene al archivo.txt ( puedo comprobarlo haciendo ls para ver los archivos y directorios que hay dentro de "UAX") el cual podría empezar a editar, modificar...

Pregunta_6 b): Si me encuentro desde el directorio "Universidad", tendría que seguir lo que se conoce como ruta absoluta, es decir, aquella ruta que me lleva desde el directorio actual, hasta mi destino, para lo que puedo ejecutar cd UAX, y como de la forma anterior, puedo comprobarlo haciendo ls y veré lo que hay dentro de el directorio "UAX", donde debería estar el archivo txt.

Pregunta_7:
1)git clone
2)git branch
3)git checkout
4)git add
5)git commit
6)git push
7)git pull
8)git merge
9)git reset --hard
10)git log

Pregunta_8: Para realizar esta tarea, es importante que todos los cambios de cada rama estén en un mismo repositorio remoto, para que sea mucho más sencillo tranajar (Con esto quiero decir que exista un solo repositorio remoto en una cuenta de grupo, para ahorrarse realizar varios pull request, forks... con un repositorio original y varias cuentas con el repositorio copiado) Por esto es muy importante trabajar con distintas ramas. En caso de que el grupo que esté trabajando en la rama matemáticas, halla completado una serie de cambios importantes que quieran subir a develop, al iguaol que el grupo que está trabajando en Diseño UX (estando ya esos cambios en el repositorio remoto), deberíamos hacer un pull del repositorio remoto para comenzar a trabajar en local. Si queremos fusionar esos cambios de esas ramas con la rama develop, primero debemos posicionarnos en la rama Matemáticas, hacer un git merge develop, y arreglar los posibles conflictos que puedan surgir. Después haremos lo mismo desde la rama Diseño UX (para cambiarnos de rama, ejecutamos git checkout Diseño UX) y hacemos git merge develop, solucionando los posibles conflictos que puedan aparecer. Estas fusiones, se han quedado en la rama Matemáticas, y en la rama Diseño UX respectivamente (Esto se hace para ver que no hay ningún problema antes de dejar los cambios en la rama develop). Ahora solo faltaría dejar esos cambios en la rama develop, para lo que ejecutaremos desde esa rama git merge Matemáticas, y después Diseño UX. Por último, solo quedaría subir los cambios al repositorio remoto con git push --all para dejar todos los cambios en el repositorio remoto.

Pregunta_9: C)

























