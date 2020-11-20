# Tech

## Autogestión Académica 
### Intro
Compartir nuestra Autogestión es un placer para ver crecer no solo nuestra Regional Córdoba sino todas las Regionales de Nuestra Universidad Tecnológica Nacional.
La misma se viene implementando a través de los años y crece de acuerdo a los requerimientos que se plantean día a día.
Pueden ver la evolución y probar partes de ella en : https://autogestion.frc.utn.edu.ar/

### Estructura (ver pdf)
Nuestra Autogestión 4 se encuentra divida aplicando el modelo empresarial que implementan las aplicaciones desarrolladas en Java. Básicamente está divida en:  
 EJB (el backend),    
 Web (el frontend)   
todo esto se genera en un único archivo .EAR (Enterprise Application aRchive). Mas info en : https://en.wikipedia.org/wiki/EAR_(file_format)

#### Acceso a datos
En la autogestión definimos el acceso a datos a traves de 5 base importantes, de las cuales 3 de ella son el core de la misma. 
La primera es la conetividad con el Sysacad, la segunda es un Cache, (replica de la primera), para no afectar la performance del propio Sysacad Desktop y por último la de Autogestion4. Por otro lado, tambien poseemos un conexión que mantiene nuestras sesiones entre servidores y otra con la versión de Autogestion3.  

#### Integraciones
La Autogestión tiene unos años y viene integrando diversos sistemas de allí podemos enumerar alguno de ellos:  
+ La misma se basa a partir del SysAcad, donde se adquiere la información académica, e integra funcionalidades propias.
+ El file server de Windows en donde se encuentra la autogestion3.
+ El NAS donde se encuentran los archivos compartidos entre servers.
+ Gitlab donde se encuentra la Ayuda y el código de la misma.
+ A su vez tambien, integra partes del SysAdmin y Moodle (en la cual tenemos una librería propia)
+ El LDAP para los usuarios.

### Instalación
Para la instalación necesitamos un servidor Linux actualizado de su agrado como mínimo 2 core y 8GB de memoria (ideal 8 core y 16/32GB).  
En nuestro caso usamos siempre usamos Ubuntu en sus versiones LTS. La ultima es Ubuntu 20.04 y se puede descargar desde aqui:   
https://ubuntu.com/download/server   
Tambien recomendamos descargar la version minima del server que se encuentra en: http://archive.ubuntu.com/ubuntu/dists/focal/main/installer-amd64/current/legacy-images/netboot/   
Por otro lado necesitamos Java para ejecutar el servidor de aplicaciones y la aplicación propiamente dicha.   
Para ellos podemos optar por descargar los paquetes oficiales de los repositorios de las distrubuciones de linux.   
En nuestro caso al igual que con los servidores usamos versiones LTS. En Java actualmente contamos con 2 versiones LTS, la 8 y 11, la que usaremos será la 8 aunque creemos que con la version 11 tambien funcionaría la aplicación sin problemas.   
Tambien pueden descargar la versiones de Java en https://adoptopenjdk.net/    
Con respecto al servidor de aplicaciones usamos JBoss AS 6.3 y estamos migrando a una infraestructura full open source en donde usaremos Wildfly. La información la podemos encontra en https://www.wildfly.org/ o descargar JBoss AS 6.4  


