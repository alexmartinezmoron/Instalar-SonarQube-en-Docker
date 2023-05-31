# Instalar-SonarQube-en-Docker
 Instalar SonarQube en Docker para windows y con bbdd Postgre

En primer lugar tras tener docker funcionando en windows accedemos al PowerShell y ejecutamos el comando "wsl -d docker-desktop" para iniciar la aplicación Docker Desktop dentro de Windows Subsystem for Linux (WSL).

Definimos la cantidad máxima de áreas de memoria virtual permitidas el proceso con el comando "sysctl -w vm.max_map_count=262144".

Listo ahora nos toca navegar desde el cmd hasta el directorio donde tenemos descargado el docker-compose.yml y ejecutar el comando "docker-compose up -d", esto hará que docker lea nuestro compose comience a descargar y configurar las imagenes de SonarQube y Postgre  desde el propio hub de Docker, tras finalizar podemos comprobar si los servicios estan en ejecucion con el comando "docker ps".

Sonar se ha configurado en el puerto 9000 tanto origen como destino, por la ruta en nuestro navegador será http://localhost:9000.
Tanto el usuario como la contreseña por defecto de SonarQube es admi, tras el primer incicio podremos cambiar dicha contraseña.

Postgre queda configurado en el puerto 5432/tcp.
