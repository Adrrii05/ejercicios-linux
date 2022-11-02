# ejercicios-linux
Introducción de comandos
Ejercicios comandos Linux 


1. Listar todos los archivos del directorio bin. 
cd /bin ; ls -a

2.Listar todos los archivos del directorio tmp. 

cd /temp
ls -a

3. Listar todos los archivos del directorio etc que empiecen port en orden 
inverso. 

cd /etc
ls -a -d -r t*


4. Listar todos los archivos del directorio dev que empiecen por tty y tengan 5 
caracteres.
 
cd /dev
ls -a tt


5. Listar todos los archivos del directorio dev que empiecen por tty y acaben en 
1,2,3 ó 4. 

cd /dev

ls tty*1
ls tty*2
ls tty*3
ls tty*4


6. Listar todos los archivos del directorio dev que empiecen port y acaben en 
C1. 


ls t*c1


7. Listar todos los archivos, incluidos los ocultos, del directorio raíz. 
cd /
ls -a

8. Listar todos los archivos del directorio etc que no empiecen por t. 
ls -d /etc/[^t]*

9. Listar todos los archivos del directorio usr y sus subdirectorios. 
cd /usr | ls -R 

10. Cambiarse al directorio tmp, crear directorio PRUEBA. 
cd /tmp ; mkdir prueba

11. Verificar que el directorio actual ha cambiado. 
pwd

12. Mostrar el día y la hora actual. 
date

13. Con un solo comando posicionarse en el directorio $HOME. 
cd /home

14. Verificar que se está en él. 
pwd

15. Listar todos los ficheros del directorio HOME mostrando su número de inodo. 
cd /home | ls -i

16. Borrar todos los archivos y directorios visibles de vuestro directorio PRUEBA. 
rm -rf prueba/*

17. Crear los directorios dir1, dir2 y dir3 en el directorio PRUEBA. Dentro de dir1 
crear el directorio dir11. Dentro del directorio dir3 crear el directorio dir31. Dentro del directorio dir31, crear los directorios dir311 y dir312. 

mkdir prueba/dir1
mkdir prueba/dir2
mkdir prueba/dir3
mkdir prueba/dir1/dir11
mkdir prueba/dir3/dir31
mkdir prueba/dir3/dir31/dir311
mkdir prueba/dir3/dir31/dir312

18. Copiar el archivo /etc/motd a un archivo llamado mensaje de vuestro 
directorio PRUEBA. 

sudo touch /etc/motd/mensaje


19. Copiar mensaje en dir1, dir2 y dir3. 
cd prueba
cd mensaje dir1/mensaje | cp mensaje dir2/mensaje | cp mensaje dir/mensaje


Comprobar el ejercicio anterior mediante un solo comando. 
ls -R PRUEBA
20. Copiar los archivos del directorio rc.d que se encuentra en /etc al directorio 
dir31. 
cp -r /etc/rc.d dir31

21. Copiar en el directorio dir311 los archivos de /bin que tengan una a como 
segunda letra y su nombre tenga cuatro letras. 

cp -r /bin/?a?? prueba/dir3/dir31/dir311
22. Copiar el directorio de otro usuario y sus subdirectorios debajo de dir11 
(incluido el propio directorio). 
cp -r ../usuario2 PRUEBA/dir1/dir11
23. Mover el directorio dir31 y sus subdirectorios debajo de dir2. 
mv PRUEBA/dir3/dir31 PRUEBA/dir2
24. Mostrar por pantalla los archivos ordinarios del directorio HOME y sus 
subdirectorios. 


ls -R $HOME
25. Ocultar el archivo mensaje del directorio dir3. 
mv PRUEBA/dir3/mensaje
PRUEBA/dir3/.mensaje
26. Borrar los archivos y directorios de dir1, incluido el propio directorio. 
rm -rf PRUEBA/dir1
27. Copiar al directorio dir312 los ficheros del directorio /dev que empiecen por t, 
acaben en una letra que vaya de la a a la by tengan cinco letras en su nombre. 
cp /dev/t??[a*b]
/home/ubuntu/PRUEBA/DIR3/DIR31/DIR312
28. Borrar los archivos de dir312 que no acaben en b y tengan una q como cuarta 
letra. 
rm -r PRUEBA/dir2/dir31/dir312/???q[^b]
29. Mover el directorio dir312 debajo de dir3. 
mv PRUEBA/dir2/dir31/dir312/PRUEBA/dir3
30. Crear un enlace simbólico al directorio dir1 dentro del directorio dir3 llamado 
enlacedir1. 
ln -s /home/ubuntu/PRUEBA/dir1prueba/dir3/enlacedir1
31. Posicionarse en dir3 y, empleando el enlace creado en el ejercicio anterior, 
crear el directorio nuevo1 dentro de dir1. 
cd dir3 mkdir enlacedir1/nuevo1
32. Utilizando el enlace creado copiar los archivos que empiecen por u del 
directorio /bin en directorio nuevo1. 

cp -r /bin/u enlacedir1/nuevo1

33. Crear dos enlaces duros del fichero fich1, llamarlo enlace, en los directorios 
dir1 y dir2. 
ln fich1 dir1/enlace in fich1 dir2/enlace
34. Borrar el archivo fich1 y copiar enlace en dir3. 
rm fich1 dir1/enlace dir3/
35. Crear un enlace simbólico (llamado enlafich1) al fichero enlace de dir2 en 
dir1. 
ln -s /home/ubuntu/prueba/dir2//home/ubuntu/PRUEB/di1/enlafich1
