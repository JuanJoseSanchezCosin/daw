Comandos de instalación vsftpd por Juan José Sánchez Cosín





1º Comenzamos en la máquina virtual de Debian 12 actualizando repositorios con el comando sudo apt update



2º Instalamos el servidor FTP con el comando sudo apt install vsftpd - y



3º Comprobamos la versión que nos ha instalado con el comando sudo vsftpd -v



&nbsp;

Configuración de vsftpd.conf



4º Creamos una copia del archivo de configuración con el comando sudo cp /etc/vsftpd.conf /etcvsftpd.conf.backup



5º Dentro del archivo hacemos las modificaciones necesarias y comprobamos que no esten comentadas ciertas líneas y añadimos otras al final del archivo.





Configuración de firewall



6º Configuración de los puertos del firewall con los siguientes comandos sudo ufw status

sudo ufw allow 21/tcp, sudo ufw allow 40000:50000/tcp, sudo ufw reload, sudo ufw status numbered



7º Reiniciamos el servidor y vemos su estado con los comandos sudo systemctl restart vsftpd y sudo systemctl status vsftpd





Pruebas con FileZilla



8º Después de tener instalado FileZilla en nuestra máquina anfitriona conectamos con nuestra maquina virtual Debian. Comprobamos nuestra IP de la MV y con usuario y contraseña en el puerto 21 accedemos.



9º Creamos una carpeta desde Windows en nuestro servidor remoto.



10º Creamos un archivo en notepad en Windows y lo arrastramos a nuestra carpeta creada en nuestro sitio remoto. Comprobamos abajo que la transferencia  a tenido éxito.



11º Comprobamos en nuestra MV que el archivo esta en la localización que hemos seleccionado desde FileZilla.



Capturas incluidas









&nbsp;



&nbsp;







&nbsp;





&nbsp;













&nbsp;



&nbsp;





&nbsp;





















































































&nbsp;

































