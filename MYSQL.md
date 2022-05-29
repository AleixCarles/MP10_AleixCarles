<h1 align="center">MYSQL</h1>
<h3 align="center">Objectiu: L'objectiu de la tasca és instal·lar el sistema gestor de base de dades MySQL i ajustar-lo per tal que funcioni amb una aplicació/plantilla que us proporciona el professor.</h3>

<p>Primer de tot instalem el mysql server de la següent manera:</p>

![Selecció_2029](https://user-images.githubusercontent.com/91152783/170866867-145a321f-1d39-4741-9716-c2d2058fbad8.png)

<p>Una vegada instal·lat farem la comanda mysql i veurem que ens donara un error a l'acces, això o canviarem ara per a que poguessim accesdir.</p>

![Selecció_2030](https://user-images.githubusercontent.com/91152783/170867139-6ca08b2f-731b-4097-8aeb-388f6f783238.png)

<p> Primer mirem si tenim insta·lat nmap (si no ho està ho instalem amb la comanda apt-get install namp), una vegada confirmem que esta instal·lat mirem que el port de mysql esta obert.</p>

![Selecció_2031](https://user-images.githubusercontent.com/91152783/170867293-e0b82376-2c91-486c-bb36-d542c5a46683.png)

<p>Ara mirem el usuari i contrasenya que ens crea per defecte el sistema de debian.</p>

![Selecció_2032](https://user-images.githubusercontent.com/91152783/170868780-a277ddf4-2ac3-4165-97f2-92725c844bb5.png)

<p> Per entrar des de aquest usuari fem la comanda mysql -p (per a que ens pregunte la contrasenya) -u (per l'usuari) i el nom de l'usuari que amb el nostre cas es debian-sys-maint. Una vegada fem la comanda ens pregunta sobre una contrasenya, aquesta contrasenya que ens pregunta es la que hem mostrat al pas anterior acompanyada de l'usuari.</p>

![Selecció_2033](https://user-images.githubusercontent.com/91152783/170870707-d55fc918-393e-45c3-9d7c-fd7b6177aefc.png)

<p> Ara que estem dins crearem una base de dades, aquesta es crea des de dins del mysql i ficarem CREATE DATABASE (nom de la base de dades que voldrem).</p>

![Selecció_2034](https://user-images.githubusercontent.com/91152783/170870902-7b399ba2-2c14-4727-95bd-a4cf3163479a.png)

<p> I una vegada creada per confirmar-ho farem SHOW DATABASES; per veure totes les bases de dades creades.</p>

![Selecció_2035](https://user-images.githubusercontent.com/91152783/170870972-3479c010-5773-40bf-9b08-07df26bb96ee.png)

<p> Podem confirma que esta la base de dades creada , ara dins d'ella crearem una taula.</p>
<p> Primer de tot li assignarem la Database (base de dades) que volem utilitzar, amb el meu cas es task ja que es la creada anteriorment, llavors dicare per poder entrar dins d'ell use tasks; .</p>

![image](https://user-images.githubusercontent.com/91152783/170871179-fddb3f74-92e5-45c3-bd7e-58e5925d669c.png)

<p> Per crear la taula  ficarem create table "nom de la taula" amb el meu cas fico tasks i entre parentesis ficarem les columnes que voldrem, jo fico la descripcio de la tasca i un boolean on ens digui si esta completat o no.</p>

![image](https://user-images.githubusercontent.com/91152783/170872078-cade3f49-ac08-4d71-8479-f711c7d176f3.png)

<p>Per veure les taules creades farem SHOW TABLES.</p>

![image](https://user-images.githubusercontent.com/91152783/170872161-0507f18b-68f7-470c-8d0d-ee14f5d68e61.png)

<p> Ara farem la instal·lació de MySQL Workbench</p>
<p>Per començar anirem a la pagina de <a href="https://dev.mysql.com/downloads/" title="MySQL_Downloads">MySQL Community Downloads</a> on trobarem per descarregar el Workbench</p>


  
  
  
