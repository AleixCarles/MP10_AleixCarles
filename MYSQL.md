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
<p>Per començar anirem a la pagina de <a href="https://dev.mysql.com/downloads/" title="MySQL_Downloads">MySQL Community Downloads</a> on trobarem per descarregar el Workbench.</p>

![Selecció_2039](https://user-images.githubusercontent.com/91152783/170872734-fee2d3d8-352c-4767-8e86-7bc93e11eb9e.png)

<p> Una vegada dins elegim l'opció que correspongui millor al nostre sistrema operatiu i ho descarreguem.</p>

![Selecció_2040](https://user-images.githubusercontent.com/91152783/170872868-4477400a-f536-48e8-9bb6-e4957d9a9f39.png)

<p> Una vegada descarregat des de el terminal anem anem al directori/carpeta que esta descarregat el paquet i començarem la instal·lació. Al ser un paquet .deb aques el instal·lem amb dpkg -i i el nomdel paquet, aquí una captura de com es fa:</p>

![image](https://user-images.githubusercontent.com/91152783/170873165-d69fb635-44a1-4a37-8deb-cb1eaa06c1d3.png)

<p> Veurem que ens salta un error, ens indica que falta una paquet per instalar aquest paquet es el workbench-community així que procedim a instal·lar-ho.</p>

![Selecció_2045](https://user-images.githubusercontent.com/91152783/170873357-73483cd7-4665-456b-b30d-e085b07a06fa.png)

<p> I ara instal·lem aquest amb la comanda anterior </p>

![image](https://user-images.githubusercontent.com/91152783/170873513-623ccbdd-3ec0-410d-bdca-adc3fefc7c69.png)

<p> Una vegada instal·lat veurem que ja tenim l'aplicaciò</p>

![image](https://user-images.githubusercontent.com/91152783/170873571-5a113e46-e4da-4151-a2a6-cd19a1434b7a.png)

<p> Ara obrim l'aplicació, si no s'obre prova de fer la comanda apt --fix-broken install. Per executtar-ho fiquem /usr/bin/mysql-workbench .</p>

![Selecció_2048](https://user-images.githubusercontent.com/91152783/170874218-7d91801c-701b-42b5-b21f-aa7f8db3a827.png)

<p> Si intentem entrar al MySQl que ens surt ens donara error ja que l'usuari que esta ficat no es el correcte.</p>

  ![Selecció_2050](https://user-images.githubusercontent.com/91152783/170874342-b7af7766-979e-4407-a0f3-3c8e4864e11a.png)

  ![Selecció_2049](https://user-images.githubusercontent.com/91152783/170874355-ec9236fc-4dfc-475d-82f4-a923ea2d86bb.png)

<p> Per canviar el usuari, fem clic dret sobre ell i anem a l'opció Edit connection...</p>

![Selecció_2051](https://user-images.githubusercontent.com/91152783/170874528-e7454968-97bb-4ce2-b7fd-7df374fdf7a6.png)

<p> Dins d'ell fiquem l'usuari i la contrasenya que hem vist anteriorment.</p>

![image](https://user-images.githubusercontent.com/91152783/170875354-d0ff4e7a-2086-4cdc-b9fc-17ea31d181b0.png)

<p> Per comprovar que està bé podem fer un test de conexio fen clic sobre la casella senyalada.</p>

![Selecció_2054](https://user-images.githubusercontent.com/91152783/170875888-3803019e-7337-4b05-9292-4add97096697.png)

<p> Veurem que esta tot correcte quan ens surte aquesta pestanya.</p>

![Selecció_2053](https://user-images.githubusercontent.com/91152783/170875919-bf7c02a6-2fcb-441a-9c10-aaf2e679b991.png)

<p> Des de aquesta eina podrem entrar a la base de dades que hem creat al principi o esta la taula creada, a aquesta podrem afegir files modificarles entre altres coses de manera grafica.</p>

![image](https://user-images.githubusercontent.com/91152783/170876120-4ca61966-9b17-4b83-8f1f-e4983bd145f9.png)

<p> Ara ens fiquem al Phpstorm. </p>
<p> Una vegada estem dins del Phpstorm i creem un nou preojecte, anirem a afegir noves bases de dades, per a fer-ho anirem a fer clic sobre la pestanta que surt apegada a la dreta de tot on fica Databases, veurem que s'obrira una pestanya, dins d'aquesta pestanya podrem fixar-nos amb una casella on hi ha un +.</p>

![Selecció_2057](https://user-images.githubusercontent.com/91152783/170876786-4ef24e9f-270c-4fd3-ab85-471123d4e848.png)

<p>Dins d'aquest + veure anirem a Data source on hi ha suport per bastants sistemes, nosalres utilitzarem la MySQL així dons farem clic a ell.</p>

![Selecció_2058](https://user-images.githubusercontent.com/91152783/170876882-a974c334-d5fd-4f53-b435-a8c91ce81618.png)

<p>Una vegada obert veurem que tindrem ka configuració dek project pero abaix ens surt una pestanya de avís de que ens falta els drivers. Fen clic sobre Download es descarrega.</p>

![Selecció_2059](https://user-images.githubusercontent.com/91152783/170877020-e5f55eed-c6ad-4eab-ba6f-d835aace3c1d.png)

<p>A la configuració ficarem el usuari i contrasenya d'anteriorment o aplicarem i farem un test de conexió si tot va bé tindria que sortir així.</p>

![Selecció_2061](https://user-images.githubusercontent.com/91152783/170877277-3b0d0a03-2203-49fa-a4df-a9b9e9454213.png)
 
<p> I ja tindriem acces a la base de dades. </p>

![image](https://user-images.githubusercontent.com/91152783/170877408-7f0dc5f7-8ef2-41d2-821b-ea01e69d861f.png)

<p> Des de la taula ja podriem afegir mes linies com aquestes. </p>

![image](https://user-images.githubusercontent.com/91152783/170877484-908f788b-1852-4061-b2e7-199070668796.png)

<p> Ara anem al terminal ens ubiquem a la carpeta Code i disn de code a la carpeta amb el nom que heu ficat amb el meu cas aleixcarles i creem una nova que es dira PHP_PDO. </p>

![image](https://user-images.githubusercontent.com/91152783/170877844-6923edd8-0043-45f2-b1e4-71294a75ce8a.png)

<p> Després de crear-ho anirem al toolbox i farem clic a la rodeta de menú toolbox i farem clic sobre conficuración.</p>
  
![Selecció_2066](https://user-images.githubusercontent.com/91152783/170878036-e0b406da-0420-451f-9c04-fa8aba174140.png)

<p> Una vegada dins busquem l'apartat Herramientas, fem clic per a que s'obre i dins veurem que la pestanya de generar scripts de shell esta desactivada, farem clic sobre ell per activar, despres fem clic a Cambiar... per canviar l'ubicació del script.</p>

![Selecció_2067](https://user-images.githubusercontent.com/91152783/170878217-e752ed31-dec1-43ce-b714-94f662a760bc.png)

<p> Quan estigui obert farem clic a Nueva carpeta i crearem una que es dira phpstorm, i li assignarem aquesta per a ubicarse.</p>

![Selecció_2069](https://user-images.githubusercontent.com/91152783/170878381-0e1baa6c-cc50-46f5-b88b-4d49c83e9bf1.png)

<p> Ara al terminal ens ubiquem i anem a la carpeta creada phpstorm i dins d'ella fem en pwd per veure la dirreció. Aquesta direcció la compiarem ja que la tindrem que ficar als 2 fitxers, al .zshrc i al .bashrc . </p>

![Selecció_2070](https://user-images.githubusercontent.com/91152783/170878753-084cc132-7411-4568-afd8-4ea0c585bb75.png)

![Selecció_2071](https://user-images.githubusercontent.com/91152783/170878765-d85f5e31-f305-4c35-96d3-21d1d1e68c0e.png)

![Selecció_2072](https://user-images.githubusercontent.com/91152783/170878811-39bd28bc-a300-459e-b999-a80c04e8b136.png)

<p>Farem des de la carpeta abans creada phpstorm . i veurem que ja podrem obrir des de el terminal el phpstorm.</p>

![image](https://user-images.githubusercontent.com/91152783/170878977-ee37b481-80ae-48dc-bb27-e1decc543d28.png)

<p> Dins del phpstorm creem el fitxer index.php aquest es pot crear fen clic dret sobre la carpeta anar a New i dins de New a File, fiques el nom i estaria creat.</p>

![Selecció_2075](https://user-images.githubusercontent.com/91152783/170879516-e84cab6e-4cf5-49dd-bd93-2f3a8297cc12.png)

<p> Fiquem contingut dins del fitxer</p>

![image](https://user-images.githubusercontent.com/91152783/170879686-d2607a47-8c13-4809-81f4-a7a0e5a35694.png)

<p> Anem al terminal i executem el fitxer creat, veurem que ens torna un Hola mon tal i com li hem dit</p>

![image](https://user-images.githubusercontent.com/91152783/170879875-06d09b06-6293-4ed9-8bc9-ec18b81af55c.png)

<p> Ara fem la comanda per a que s'uneixi al localhost i poder veureu des de el navegador</p>

![Selecció_2079](https://user-images.githubusercontent.com/91152783/170880396-576ab226-863c-46b2-922e-2d48221d813a.png)

![Selecció_2080](https://user-images.githubusercontent.com/91152783/170880406-e67b8a55-df55-44fb-a4f2-504d8e28d792.png)

<p> Tornem a fer el codi pero esta vegada mes consistent que l'altre i vinculant-ho amb un altre que es diu task.php </p>

![Selecció_2081](https://user-images.githubusercontent.com/91152783/170881673-19df2b37-66a0-4960-b397-4b3b2308e22b.png)
![image](https://user-images.githubusercontent.com/91152783/170881685-2e3a15c5-b9b5-45d7-9213-76d5c4ba69cd.png)

<p> I d'aquesta manera es consegueix fer la base de dades diferents maneres de editar amb php i diferents eines que s'utilitzen.</p>

 

  





