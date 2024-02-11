Crear un directorio y convertirlo en un repositorio Git:

mkdir practica_evaluable: Crea un nuevo directorio llamado "practica_evaluable".
cd practica_evaluable: Cambia al directorio "practica_evaluable".
git init: Inicializa un repositorio Git en el directorio actual.


Crear archivos y añadir texto:

touch documento1.txt documento2.txt: Crea dos archivos vacíos llamados "documento1.txt" y "documento2.txt".
echo "Texto para documento1" > documento1.txt: Añade texto al archivo "documento1.txt".
echo "Texto para documento2" > documento2.txt: Añade texto al archivo "documento2.txt".


Validar cambios en el repositorio local:

git add documento1.txt documento2.txt: Añade los archivos "documento1.txt" y "documento2.txt" al área de preparación.
git commit -m "Añadir documento1.txt y documento2.txt": Guarda los cambios en el repositorio local con un mensaje descriptivo.


Realizar cambios en documento1.txt:

echo "Nuevas líneas en documento1" >> documento1.txt: Añade nuevas líneas al archivo "documento1.txt".
git add documento1.txt: Añade el archivo "documento1.txt" modificado al área de preparación.
git commit -m "Cambios en documento1.txt": Guarda los cambios en el repositorio local con un mensaje descriptivo.


Realizar cambios en documento2.txt:

echo "Nuevas líneas en documento2" >> documento2.txt: Añade nuevas líneas al archivo "documento2.txt".
git add documento2.txt: Añade el archivo "documento2.txt" modificado al área de preparación.
git commit -m "Cambios en documento2.txt": Guarda los cambios en el repositorio local con un mensaje descriptivo.


Volver a la situación antes de los cambios en documento2.txt:

git reset --hard HEAD^: Regresa al commit anterior, deshaciendo los cambios realizados en "documento2.txt".


Crear documento3.txt, añadir cambios y validar:

touch documento3.txt: Crea un nuevo archivo llamado "documento3.txt".
echo "Contenido para documento3" > documento3.txt: Añade contenido al archivo "documento3.txt".
git add documento3.txt: Añade el archivo "documento3.txt" al área de preparación.
git commit -m "Añadir documento3.txt": Guarda los cambios en el repositorio local con un mensaje descriptivo.


Revertir el último commit:

git revert HEAD: Revierte el último commit, deshaciendo los cambios realizados en el último commit sin perder el historial.


Conectar con un repositorio remoto y subir la información:

git remote add origin <URL_del_repositorio>: Asocia el repositorio local con un repositorio remoto en GitHub.
git push -u origin main: Sube la información del repositorio local al repositorio remoto en la rama main.


Crear una rama y añadir archivos:

git checkout -b mirama: Crea una nueva rama llamada "mirama" y cambia a ella.
touch rama1.txt rama2.txt: Crea dos archivos en la nueva rama.
git add rama1.txt rama2.txt: Añade los archivos al área de preparación.
git commit -m "Añadir archivos en la rama mirama": Guarda los cambios en la nueva rama con un mensaje descriptivo.


Fusionar la rama mirama con la rama main:

git checkout main: Cambia a la rama main.
git merge mirama: Fusiona los cambios de la rama mirama con la rama main.


Borrar la rama mirama:

git branch -d mirama: Elimina la rama mirama.


Sincronizar cambios con el repositorio remoto:

git push origin main: Sube los cambios de la rama main al repositorio remoto.


Crear una etiqueta y subirla al remoto:

git tag V1: Crea una etiqueta llamada "V1" en el commit actual.
