<h1 align=center>Instal·lació sistema gestor de base de dades. MySQL</h1>
<h3>Aquest document es una documentació tecnica de com instal.lar i configurar el MySQL </h3>


<p>Començem instal.lant el mysql-server amb la seguent comanda</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_001.png>
<p/>

<p>Despres buscarem el port de MySQL per fer-ho necessitem el programa nmap</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_002.png>
</p>

<p>Un cop ja tenim instal·lat el nmap buscarem el port de MySQL que es el 3306</p>

<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_003.png>
</p>
     
<p>Ara executarem la comanda <b>cat /etc/mysql/debian.cnf</b> on trobarem l'usuari i contrasenya</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_004.png>
</p>
     
<p>Ara ja podrem accedir a mysql amb la següent comanda <b>mysql -p -u debian-sys-maint</b></p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_005.png>
</p>
     
<h3>Ara que estem dins realitzarem algunes proves</h3>

<p>Per començar crearem una base de dades anomenada tasks amb la següent comanda<b>CREATE DATABASE tasks;</b></p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_006.png>
</p>
<p>Comprovem que s'ha creat correctament amb la comanda <b>SHOW DATABASE</b></p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_007.png>
</p>     
<p>Amb la comanda <b>USE tasks</b> entrem a la base de dades</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_008.png>
</p>     
<p>Creem una taula amb la comanda <b>CREATE TABLE tasks (descripion text, completed boolean);</b></p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_009.png>
</p>     
<p>Ho comprovarem amb la comanda <b>SHOW TABLES;</b></p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_010.png>
</p>
     
<p>Instal.lem el MySQL Workbench amb la seguent comanda</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_011.png>
</p>

<p>Un cop instal.lat entrem al programa</p>  
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_012.png>
</p>     
<p>Ara farem clic dret a la instancia que hi ha creada per obrir el seguent menu i seleccionarem "Edit Connection"</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_013.png>
</p>     
<p>Cambiem l'usuari pel que ens han indicat anteriorment</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_014.png>
</p>     
<p>Aqui simplement ens demana la contrasenya que anteriorment hem obtingut</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_015.png>
</p>           
<p>Busquem la base de dades creada amb la sentencia SELECT * FROM tasks.tasks i fent clic sobre el rayo. Veiem que ens mostrara les dos columnes creades anteriorment</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_016.png>
</p>   
<p>Instal.lem el seguent paquet que necessitarem per continuar</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_017.png>
</p> 
<p>Ara ens dirigim a la secció Data Sources i assignem el usuari i contrasenya anteriors i crearem la base de dades tasks</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_018.png>
</p>     
<p>Ara crearem una taula dins la base de dades anomenada tasca 1</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_019.png>
</p>    
<p>Tornem a realitzar la sentencia anterior i com podem veure surt la tasca 1</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_020.png>
</p>     
<p>Un cop acabat entrarem a la carpeta que hem creat durant la preparació de la maquina i crearem la seguent carpeta</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_021.png>
</p>     
<p>Ara entrem al Toolbox dins de la configuració de PHPstorm i activarem el "Generar scripts de shell" i farem clic a "Cambiar"</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_022.png>
</p>    
<p>Seleccionem la carpeta phpstorm</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_023.png>
</p>  
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_024.png>
</p> 
<p>Ara entrem a editar el seguent fitxer i li afegim la ultima linia que hi ha per crear un vincle</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_025.png>
</p>    
<p>Entrem a la carpeta anteriorment creada i executarem la comanda phpstorm</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_026.png>
</p>
<p>Ara crearem un fitxer php am Hola Mon! al seu interior</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_028.png>
</p>  
<p>Realitzem la seguent comanda per a que es vegi pel navegador</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_029.png>
</p>   
<p>Com podem veure es pot veure perfectament</p>
<p align=center>
<img src=https://raw.githubusercontent.com/felipcurto/felipcurto/main/Imatges/Selecci%C3%B3_030.png>
</p>  

