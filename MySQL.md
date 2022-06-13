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
     
<p>Ara hi farem un <b>cat /etc/mysql/debian.cnf</b> on hi trobarem el usuari que es diu debian-sys-maint amb la seva contrasenya.</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171663559-c923885c-ea4d-46c9-a8e7-fbbd4e96dc29.png>
</p>
     
<p>Gracies que ja sabem la contrasenya, ja hi podrem accedir a mysql amb l'usuari fent la següent comanda <b>mysql -p -u debian-sys-maint</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171663946-b3a5fce4-0826-4dfb-9047-e383cb541212.png>
</p>
     
<h3>Una vegada dins de MySQL hi aprofitarem per provar certes coses: </h3>
<p>Primer de tot hi posem la comanda <b>SHOW DATABASE;</b> on hi podem veure bases de dades creades per el nostre propi sistema operatiu</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171664186-13cb9413-2dfd-4ce1-8211-1e96301ede9c.png>
</p>
     
<p>Ara hi crearem una base de dades amb la següent comanda<b>CREATE DATABASE tasks;</b> la qual tindrà el nom de tasks </p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171664966-d13dc99e-237f-4c86-a5cb-322bc89d4b06.png>
</p>
<p>Tornem a posar <b>SHOW DATABASE</b> per comprovar que esta creada.</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171665066-fd7f10b1-103e-42f5-9476-494915eea538.png>
</p>     
<p>Amb la comanda <b>USE tasks</b> comencem a treballar amb tasks</p>
<p align=center>
<img src=![image](https://user-images.githubusercontent.com/91246894/171665114-d33fad1c-1b83-4889-8338-e270a15b0783.png>
</p>     
<p>Procedirem a crear una taula dintre de tasks posan<b>CREATE TABLE tasks (descripion text, completed boolean);</b> i despres ho comprovem la seva creació amb un <b>SHOW tables;</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171665280-bb59ac43-f0e4-4cda-8daa-80708196917d.png>
</p>     
<p>Un cop fet el anterior hi anirem a descarregar MySQL Workbench, per fer això hi anem al nostre navegador i busquem MySQL community downloads i en l'apartat de MySQL Workbench</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171665638-99caa541-e5c7-4afe-8e6e-2951376b2fad.png>
</p>
     
<p>Quan ens trobem dins descarreguem el fitxer corresponent a la nostra versió del sistema</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171665758-b1bdd4e2-6ff5-493f-81a4-fdb304773a89.png>
</p>

<p>Hi anirem al terminal, on ens ubicarem on esta el fitxer anteriorment descarregat en el meu cas Baixades/ i ficarem la següent comanda per instal·lar-lo <b>sudo dpkg -i "El Nom del nostre paquet"</b></p>  
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171665831-de8073c6-d792-4fe9-a04b-f09ccc4746d4.png>
</p>     
<p>Abans d'instal·lar-lo necessitem el mysql-workbench-community i procedim a instalarlo amb <b>mysql-workbench-community</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171666203-d7dac486-0078-4bb2-82cc-d767be837988.png>
</p>     
<p>Ens dona un error i el qual el solucionarem amb la següent comanda <b>apt --fix-broken install</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171666299-a8fc19d4-1bd1-4db5-8786-60bf1fc1ad01.png>
</p>     
<p>Per tindreu tot instal·lat hi farem la següent comanda<b>sudo apt-get install libopengl0 libpcrecpp0v5 libproj15 libzip5</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171666409-73109d29-08b8-4a30-a85f-f4b674015622.png>
<img src=https://user-images.githubusercontent.com/91246894/171666720-50e9f3b1-91a8-400d-82ec-c4a6bec52227.png>
</p>     
<p>Una vegada hem instal·lat el workbench i anirem a un terminal hi ficarem mysql-workbench per iniciar-ho</p>  
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171666809-5a609027-91e0-425d-a784-357da15c4dfc.png>
</p>     
<p>No ens deixar accedir ja que no tenim l'usuari i la contrasenya configurada per fer-ho tindrem que anar-hi a <b>Edit Conneciton></b> i tindrem que ficar els que hem utilizat anteriorment</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171667162-9ce8a32e-1b1d-451e-9d2f-7bae9839c019.png>
</p>   
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171667346-24600f04-1ea7-49f3-a6a0-b987d214f1c4.png>
</p>   
<p>Hi iniciem el workbench i busquem la base de dades creada, per fer-ho hi tenim que escriure SELECT * FROM tasks.tasks i fer clic sobre el relampago. Veiem que ens mostrara les dos columnes que hi tenim creades.</p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171667833-ad33aca3-3f3e-49dd-9220-04a0134f4506.png>
</p>   
<p>Ara procedirem a instalar el PhpSorm amb el toolbox i crear un nou projecte i accedim a l’apartat de database</p>
<p>Accedim a l'apartat que mostra la imatge i en aquesta pestanya que ens mostra és el configurador de MySQL</p>
<p align=center>
</p>  
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171675937-ffe7ad48-9489-408d-80cc-c85434a78e5a.png>
</p> 
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171675031-20b4d685-8272-4034-834c-48fdcb78cdb5.png>
</p> 
<p>Ens informa que no podem utilizar-ho ja que ens falten drivers, els quals instal·larem amb la comanda<b>sudo apt-get install php7.4-mysql</b></p>
<p align=center>
<img src=https://user-images.githubusercontent.com/91246894/171676072-b1c5b864-2510-4c84-bc8e-194f20b95ee5.png>
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
