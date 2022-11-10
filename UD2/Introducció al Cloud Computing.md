# CLOUD COMPUTING 

 
:cloud: **Cloud Computing** o **computació en el núvol** és la prestació de serveis a través d'internet proporcionats per tercers. En els darrers any ha anat creixent el seu ús sobretot en el món empresarial ( on es dirigeix gran part dels serveis ) però també per a professionals i particulars.  

Els avantatges principals son:

  * Econòmics. Estalviem infraestructura i manteniment.
  * Accesibilitat. Els usuaris poden accedir-hi des de qualsevol lloc i dispositiu a través d'Internet.
  * Escalabilitat. L'ampliació dels serveis contractats és molt 

## On Premise vs CLOUD

Front al concepte de Cloud Computing tindrem el de On Premise. 

:computer: **On premise.**

Parlem del software o recursos que es troba als servidors de l'empresa de forma que permet a l'administrador de la xarxa un accés físic. Pot ser que este accés haja de ser remot.

:cloud: **Cloud computing.**

Com hem explicat seria quan no tenim infraestructura per als servicis de HW o SW. Accedim a les dades i aplicacions mitjançant internet. De forma que ens desentenem de moltes tasques de manteniment com una ampliació del sistema.

## Cloud Computing vs Virtualització

Hem vist la virtualització en hipervisors per a crear entorns de prova i estudi ( exemple de VirtualBox) i hem parlat de la virtualització de servidors en instal·lacions locals ( exemple de Proxmox). Ara estem veient un altre aspecte que seria el Cloud Computing i que no devem confondre.

**Consideracions:**

* Els dos conceptes tracten sobre creació d'entorns útils a partir de recursos abstractes. 
* Ara bé, la virtualització és una **tecnologia** que permet crear entorns (emular) a partir d'un sol sistema. 
* El núvol, en canvi, és un **entorn de TI** que obté recursos i els agrupa de forma ajustable.

* Els serveis que ofereix el Cloud Computig s'hi presten a través d'un infraestructura prèviament virtualitzada.
* A més, ofereix avantatges com l'escalabilitat, flexibilitat, administració automatizada i un estalvi econòmic ( o ajust) en poder pagar per ús ( temps, espai...)

## Núvol privat vs públic.

Parlem en tot moment del núvol públic. És a dir, aquell que està a l'abast de qualsevol client a través de la xarxa pública que vullga contractar el servici gràcies a la virtualització de serveis.
Existeixen núvols privats creat per cada empresa en la seua infraestructura pròpia per a ús privatiu.

# El model de capes i els serveis IaaS, PaaS i SaaS

El Cloud Computing es basa en un model de capes per donar serveis que podem resumir en la següent taula. 


|Capes|IaaS|PaaS|SaaS|
|---|---|---|---|
|Dades i accés|:computer:|:computer:|:computer:|
|Aplicacions|:computer:|:computer:|:cloud:|
|Runtime|:computer:|:cloud:|:cloud:|
|SO|:computer:|:cloud:|:cloud:|
|MV|:cloud:|:cloud:|:cloud:|
|Xarxa|:cloud:|:cloud:|:cloud:|
|Computació|:cloud:|:cloud:|:cloud:|
|Magatzematge|:cloud:|:cloud:|:cloud:|

:cloud: Cloud Computing. El proveïdor dels servei ( SW o HW )se'n responsabilitza.

:computer: El client ha de responsabilitzar-se'n.

En els següents subapartats detallem un poc esta informació.

## IaaS 

Mitjançant un quota o lloguer decidim la infraestructura que volem 

Infraestructura de hardware: 
* Espai de magatzematge ( capacitat de discos )
* Memòria principal ( RAM )
* Capacitat de procés( CPU )
* Els serveis de virtualització:
  * Maquines virtuals
  * IP estàtiques
  * Velocitat de xarxa
  * Tallafocs 
  * Sistemes de backups
  * Balancejadors d e càrrega 

IaaS és, per tant, la part més bàsica del TI al núvol. A partir d’esta es construeixen el altres serveis. 


## PaaS 

En un segon nivell tenim les plataformes ( el servici PaaS ) enteses estes com a software que permet desenvolupar aplicacions. des de les quals podem llaçar aplicacions. Allò més habitual serien Bases de dades o també, middleware, eines de desenvolupament, serveis d’intel·ligència empresarial. 

Es un servei pensat per a desenvolupadors que necessiten desentendre’s del software base ( SO ) i hardware per centrar-se en el desenvolupament, la implementació o l’administració. 

Exemples:

* *Google App Engine* : orientat a la publicació d’aplicacions web online. El client se centra en crear i configurar la seua aplicació mentre Google aprovisiona els recursos necessaris. 

    Disposa d’un anivellador de càrrega que augmenta el recursos quan cal. És a dir, proporciona escalabilitat de forma transparent i automàtica per a l’usuari 

*    *Bungee Connect*:  similar a l’anterior, ofereix un entorn adient per al desenvolupament, testeig i execució d’aplicacions web.

 
## SaaS 

Finalment, en esta última capa, allotjarem el software i dades de l’empresa ( o particular ). De forma que l’usuari pot accedir i fer-n ús des de qualsevol lloc.  

El hardware, els sistemes operatius, les bases de dades i altres serveis... deixen de ser una preocupació per a l’empresa, el professionals o particular.

Exemples de SaaS:
* Microsoft Office 365: plataforma de MS Office 
* WordPress:  WordPress és un software que se està executant en un servidor remot l’usuari interactua sense entendre’s de la infraestructura necessària per al seu funcionament. 

# Azure entre d’altres.

Microsoft, Amazon o Google son exemples d’empreses que han llançat els seus productes oferint el Cloud Computing. Nosaltres, a les tutories i a casa farem un introducció sobre la solució de Microsoft ( AZURE ) gràcies a l’opció que des de la **Conselleria d’Educació, cultura i esport** s’ha posat en marxa per al curs 2022-2023 i que tindrem accés mitjançant el compte *n.cognoms@edu.gva.es*

### AZURE, AWS  i GCP...

* Amazon Web Services: El servici central Amazon EC2 permet llogar servidors virtuals per instal·larr les aplicacions que necessite l’empresa o el particular. La configuració de HW  contractada s’anomena instància.  

* Microsoft Azure: Similar a AWS, destaca per oferir una varietat ampla de recursos. És el que veurem.

* GCP. Google Cloud Platform. S'incorpora més tard i ofereix millors servicis per a sectors el Machine Learning, Big Data o IA.Aporta molta fiabilitat i seguretat en les transmissions i restauració ràpida de dades.

No obstant, les característiques i diferències poden anar variant.


**Glossari**

* Middleware: software de capes que permet  comunicar una aplicació amb altres aplicacions, xarxes o HW 

* CMS: Content Management System. Sistema de gestió de continguts per a disseny de pàgines web 

* Balancejadors de càrrega: de carga: dispositius que actuen com proxies inversos per tal de distribuir el tràfic cap a altres servidors. 
* Machine Learning. Capacitat d'aprenentatge( auto aprenentatge ) de les computadores.
* IA. Intel·ligència Artificial. Part de la ciència de la computació que intenta replicar i desenvolupar la el procés racional de la intel·ligència.

![ccbyncsa](../IMATGES/cco.png){width=20%}

