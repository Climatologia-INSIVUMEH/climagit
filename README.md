# CLIMAGIT

Guía basica de primeros pasos en Github (Linux)

Instalar git en su computadora 

sudo apt-get install git 

En su cuenta en la dirección https://github.com/ 
	-Le dan click su usuario luego en settings. 
		-Click en SSH keys. 
		-New SSH key 
			En el titulo puede ser cualquier nombre y en las opciones de tipo que sea una llave de autenticación. 

En su computadora ir a /home/cdc/.ssh y copiar su llave pública (si no cuenta generarla con `$ssh keygen`). Luego esta se debe de pegar en el apartado siguiente al titulo en la página de ssh key. 

Para configurar las credenciales se deben de ingresar las variables globales.

git config --global user.name "Your Name"
git config --global user.email "youremail@yourdomain.com"

Ejemplo 

	git config --global user.name PedroPicapiedra
	git config --global user.email pedropicapiedra@gmail.com


Para confirmar que se han guardado estas configuraciones puede usar el siguiente comando: 
	
	git config --list


Puede crear un nuevo repositorio con git init (buscar los comandos de git) 

O más facil puede clonar un repositorio de git como ejemplo puede clonar el siguiente 
	
	git clone git@github.com:Climatologia-INSIVUMEH/climagit.git

Listo! 

Ahora puede entrar a la carpeta *climagit* y ejecutar el comando:
	git pull 
	
El mensaje que le tiene que dar es: El repositorio ya está actualizado. Y si revisa las llaves ssh en la página le aparecerá de color verde. 

Comandos importantes:

	Clonar un repositorio:
		git clone <https://link-con-nombre-del-repositorio>

	Al entrar en la carpeta (repositorio creado) puede ejecutar lo siguientes comandos importantes:

		Crear una rama del repositorio:
			git branch <nombre-de-la-rama>

		Estatus:

			git status

		Agregar archivos que se han modificado o creado:

			git add <archivo>  o puede escribir git add .

		Commit (guardar los cambios con comentarios):

			git commit -m "mensaje de esa actualización"

		Enviar los datos al servidor remoto:

			git push 
			
		Si quiere descargar las actualizaciones de repositorio: 
			git pull 

Otros comandos importantes son que si se quiere crear un nuevo repositorio puede hacerlo desde la interfaz web de github y luego ejectura en la carpeta local: 


	git init 

Esta función se utiliza para iniciar un nuevo repositorio de Git en el directorio actual. 


	git add . 

Esta función se utiliza para agregar todos los archivos nuevos o modificados al área de preparación de Git. El punto (.) en la función indica que todos los archivos deben ser agregados. 

	git commit -m 'comentario' 

Esta función se utiliza para confirmar los cambios agregados en el área de preparación.

	git branch -M master 

 Esta función se utiliza para cambiar el nombre de la rama actual del repositorio a "master".

	git remote add origin git@github.com:Climatologia-INSIVUMEH/prueba.git

Esta función se utiliza para agregar un repositorio remoto a Git. En este caso, se agrega un repositorio remoto llamado "origin" que está alojado en GitHub y cuyo nombre es "Climatologia-INSIVUMEH/prueba.git".

	git push -u origin master 

Esta función se utiliza para enviar los cambios confirmados al repositorio remoto en GitHub.

