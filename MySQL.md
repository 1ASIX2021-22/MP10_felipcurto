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
<p>Hi tornem a la imatge anterior i fem clic en download, després on posa user i password posem l’usuari i la contrasenya que hem trobat anteriorment, <b>també on fica database, posem tasks, importan ja que en la imatge no esta</b> i fem clic al botó de apply</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171676102-aebb286b-95c6-4b07-add8-cdec17ccb06f.png>
</p>    
<p>Aquí veiem com se’ns té que mostra actualment el Php</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171676635-88bf6014-28ba-47c6-918c-df0136d5dd9d.png>
</p>     
<p>Fem doble clic sobre tasks, se'ns obrira una pestanya nova i allí hi afegim la primera tasca fent clic dret i Add Row, quan ja l'hem afegit fem clic en la fletxa verda per penjar-ho al servidor</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171676716-df9582b9-4853-475a-9578-95859c9fcce9.png>
</p>     
<p>Tornem al workbench i fent clic en el botó del llamp ja podem veure com es mostra la taula creada al PhpStorm</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171676875-706d7692-a188-4828-beda-bd3c602a11f9.png>
</p>    
<p>Una altra forma de veure com s’ha creat es amb un <b>SELECT*FROM tasks</b> dintre del MySQL</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171676925-ace692c1-934d-4bb4-a6ca-daa8606fece5.png>
</p>     
<p>Obrim un altre terminal hi anem a la carpeta Code, tot seguit, la nostre directori i alli hi creem una carpeta anomenada PHP_PDO.</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171676993-aaf41eb7-b231-4ada-acea-433804dcdcbd.png>
</p>    
<p>Obrim el Toolbox, tot seguit, a settings, i activem la opció de <b>Generate shell scripts</b> que es trova dintre de Tools, després hi fem clic en change</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171677226-b0b08e8b-25fb-4f5b-8344-88f962806ea9.png>
</p>
<p>El qual ens obrirà una nova pestanya i allí fem click en new folder per crear una nova carpeta la qual anomenarem phpstorm, la seleccionem en els Folders i finalment presionem  OK, tornem al Toolbox i fem clic en Apply</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171677302-9c576c43-7fac-4473-80cb-152d2e4898aa.png>
</p> 
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169119903-2a8ec550-a32b-46e8-9382-8ac645399e0e.png>
</p>  
<p>Hi accedirem a la carpeta per fer-li un ls el qual ens motrar els executables següents:</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171677493-373b32e4-f17b-4a63-b315-514d65952c82.png>
</p>   
<p>Accedim a la carpeta de phpstorm i amb <b>joe ~/.zshrc</b> obrim l’editor i escrivim la ruta en la que es trova la carpeta phpstorm en la part inferior del fitxer</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171677785-9a5703d3-4c28-4ba2-9992-481ea745584c.png>
</p>  
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171677619-0682eb10-8a68-4a6a-a66f-bef2e68f5cb5.png>
</p>    
<p>Tornem a la carpeta PHP_PDO i executem <b>phpstorm .</b></p>
<p>Automàticament quan entrem al phpstorm ens apareix una carpeta per obrir el PHP_PDO, l’obrim i creem un fitxer anomenat <b>index.php</b> </p>
<p>Dintre del fitxer creat escrivim el següent</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171677973-6506f23d-6b02-4867-8918-d53f83e87ab7.png>
</p>    
<p>Tornem al terminal a la carpeta de PHP_PDO allí amb un ls ens mostrara l'índex creat, llavors si fem <b>php index.php</b> ens mostra el text escrit</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91154202/169137727-a602c0cf-bf70-4f58-ad79-361b252aed38.png>
</p> 

<p>Si es vol es pot fer que ho retorni al servidor amb <b>php -S localhost:3306 index.php</b>, quan executem aquesta comanda se'ns obrira un link al qual accedim fent Ctrl clic esquerre</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171678039-6ebbc367-3e31-4cda-8a31-9f0792d8d666.png>
</p>
