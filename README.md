Modalità operative
==================

Installazione Git
-----------------

All’indirizzo https://git-scm.com/ scaricare l’ultima versione
disponibile di Git per Windows.

|image0|

Seguire la procedura di installazione (wizard) fino al suo
completamento.

+-------------------+
| **Step 01 di 11** |
+===================+
| |image1|          |
+-------------------+
|                   |
+-------------------+

+-------------------+
| **Step 02 di 11** |
+===================+
| |image2|          |
+-------------------+
|                   |
+-------------------+

+-------------------+
| **Step 03 di 11** |
+===================+
| |image3|          |
+-------------------+
|                   |
+-------------------+

+-------------------+
| **Step 04 di 11** |
+===================+
| |image4|          |
+-------------------+
|                   |
+-------------------+

+-------------------+
| **Step 05 di 11** |
+===================+
| |image5|          |
+-------------------+
|                   |
+-------------------+

+-------------------+
| **Step 06 di 11** |
+===================+
| |image6|          |
+-------------------+
|                   |
+-------------------+

+-------------------+
| **Step 07 di 11** |
+===================+
| |image7|          |
+-------------------+
|                   |
+-------------------+

+-------------------+
| **Step 08 di 11** |
+===================+
| |image8|          |
+-------------------+
|                   |
+-------------------+

+-------------------+
| **Step 09 di 11** |
+===================+
| |image9|          |
+-------------------+
|                   |
+-------------------+

+-------------------+
| **Step 10 di 11** |
+===================+
| |image10|         |
+-------------------+
|                   |
+-------------------+

+-------------------+
| **Step 11 di 11** |
+===================+
| |image11|         |
+-------------------+
|                   |
+-------------------+

Al termine avviare Git CMD.

**Abilitazione e accesso GIT tramite account aziendale**
--------------------------------------------------------

Git è un sistema di gestione delle versioni che consente a una o più
persone di contribuire alla creazione e aggiornamento dei diversi file
di un progetto.

All’indirizzo https://git.intranet.sardegnait.it/ è disponibile il git
aziendale, basato sulla piattaforma open source **GitLab**
https://docs.gitlab.com/ . Per accedere al Git aziendale tramite è
necessario avere una email aziendale e una apposita password che verrà
inviata all’indirizzo di posta elettronica personale aziendale.

Nel caso l’account non sia stato ancora creato, è necessario chiedere
l’abilitazione all’Area Sistemi dell’azienda o al proprio Responsabile.

Una volta scaricato **Git** da https://git-scm.com/ e ricevuta l’email
di corretta attivazione dell’account aziendale, si può procedere con il
primo accesso che può avvenire tramite browser o tramite riga di
comando.

**Accesso tramite browser**
===========================

1. Accedere a https://git.intranet.sardegnait.it/

|image12|

2. Nel campo “username or email” inserire la propria email personale

3. Nel campo “password” inserire la password ricevuta per email

4. Completata la fase di login, modificare la password avendo cura di
   segnare quella nuova in un posto sicuro e riservato

NB. Se durante gli accessi successivi si dovesse smarrire o dimenticare
la password è possibile seguire il percorso “Forgot your password?” per
recuperarla. Verrà inviato un link all’indirizzo email aziendale
autorizzato e utilizzato come username.

5. Completato l’accesso a Git:

   a. se l’account non è stato autorizzato a progetti già esistenti,
      sarà possibile creare un nuovo progetto o un nuovo gruppo

   b. se è necessario accedere a progetti già esistenti chiedere
      l’abilitazione al proprio Responsabile

   c. se l’account è autorizzato a progetti già esistenti, sarà
      possibile accedere alla lista progetti oppure crearne nuovi

**Accesso tramite linea di comando**
====================================

Oltre l’accesso tramite browser, Git può essere utilizzato da linea di
comando per trasferire i file dal repository aziendale al proprio
computer e viceversa.

Tale accesso da linea di comando può avvenire:

-  Tramite email/password

-  Tramite chiave ssh

L’accesso tramite chiave ssh consente di evitare l’inserimento di
email/password ad ogni comando, ma richiede come ulteriore passo la
generazione (nel GIT locale) una chiave ssh che, dopo esser stata
salvata sul GIT aziendale, consenta al repository aziendale di
riconoscere ed accettare files o aggiornamenti di versione eseguiti con
l’account in uso.

**Git – Stati e sezioni di progetto**
-------------------------------------

I file in Git possono essere in tre stati: *committed* (committati),
*modified* (modificati) e *staged* (in stage).

-  Committato significa che il file è al sicuro nel database locale.

-  Modificato significa che il file è stato modificato, ma non è ancora
   stato committato nel database.

-  Staged significa che hai contrassegnato un file, modificato nella
   versione corrente, perché venga inserito nel prossimo commit.

Questo ci porta alle tre sezioni principali di un progetto Git: la
directory di lavoro, l'area di stage e la directory di Git (repository).

4. .. rubric:: **Sequenza dei comandi git**
      :name: sequenza-dei-comandi-git

   a. .. rubric:: **Clone**
         :name: clone

| Per poter iniziare ad operare su un progetto esistente sul repository
  aziendale è necessario effettuare una copia locale tramite il comando
  **git clone [url]**.
| L’esecuzione del comando git clone consente di scaricare le versioni
  di ciascun file associato al progetto.
| Il comando va eseguito nella Powershell, che va cercata tra le app di Windows.

Il comando

**git clone** **git@git.intranet.sardegnait.it:user/progetto.git**

**git**. Corrisponde al proprio user Git. Il proprio utente è riportato
nella sezione profilo di solito corrisponde a @ncognome

|image13|

**use**\ r. Corrisponde allo user del creatore del progetto

**progetto** Corrisponde al nome del progetto

NB. La stringa git@git.intranet.sardegnait.it:user/progetto.git è
recuperabile anche dalla pagina del progetto su
`https://git.intranet.sardegnait.it <https://git.intranet.sardegnait.it/>`__

Questo comando, eseguito in ambiente locale, creerà una directory
“progetto” in cui verranno scaricati dal repository aziendale tutti i
dati di progetto ed un file **.git** attraverso il quale si effettuerà
il controllo dell’ultima versione scaricata.

**Clone in una directory diversa**
----------------------------------

Una ulteriore possibilità consiste nel definire un nome diverso alla
directory di destinazione (locale). Questo è possibile eseguendo il
comando

**git@git.intranet.sardegnait.it:user/progetto.git altro_nome_progetto**

**altro_nome_progetto**. Corrisponde al nome della directory che si
vuole creare

**Init**
--------

Attraverso il comando **git init** si potrà tenere traccia di un
progetto locale e trasformare la directory che ospita il nostro codice
in un repository per il versioning.

Dalla directory locale del progetto l’esecuzione del comando git init
creerà una nuova sottodirectory .git che conterrà i file del repository.

Per poter, successivamente, inserire il progetto nel repository
aziendale si dovrà eseguire il comando:

**git remote add origin
git@git.intranet.sardegnait.it:user/progetto.git**

**Add**
~~~~~~~

Il tracciamento dei file avviene attraverso il comando **git add**.

Dalla directory di progetto l’esecuzione del comando git add \*
consentirà di aggiungere all’area di stage i file che si intende
monitorare (nel caso git add sia seguito da un \* verranno aggiunti
tutti i file).

**Commit**
~~~~~~~~~~

Il comando **git commit** consente di completare il monitoraggio dei
file nel repository locale.

Dopo l’esecuzione del comando git add si procede con il comando **git
commit –m** **‘descrizione operazione’**.

L’opzione –m ‘….’ Consente di inserire un testo descrittivo delle
modifiche eseguite.

**Push**
~~~~~~~~

Attraverso il comando git push quanto monitorato in locale può essere
riportato sul repository aziendale.

In sintesi, nel caso di progetto locale preesistente (punto 3.3.2), si
riportano i comandi da eseguire per l’aggiornamento del repository
aziendale:

*git init*

*git remote add origin
git@git.intranet.sardegnait.it:scasu/ILA-SUP-02.git*

*git add .*

*git commit –m ‘descrizione operazione’*

*git push -u origin master*

**Controllo dello stato dei file**
----------------------------------

Il controllo dello stato dei file avviene attraverso il comando **git
status**. Tale comando permette di verificare la situazione dei file nel
repository locale, evidenziando eventuali aggiornamenti dei file
tracciati o anche la presenza di possibili file “untracked” non ancora
versionati.

-  Nel caso in cui nessuno dei file tracciati abbia subito modifiche
   l’esecuzione del comando git status restituirebbe una situazione del
   tipo:

*$ git status*

*# On branch master*

*nothing to commit, working directory clean*

-  Nel caso in cui, invece, al progetto in locale sia stato aggiunto un
   nuovo file (es. analisi.txt) il comando git status restituirebbe una
   situazione del tipo:

*$ git status*

*On branch master*

*Untracked files:*

*(use "git add <file>..." to include in what will be committed)*

*analisi.txt*

*nothing added to commit but untracked files present (use "git add" to
track)*

In questa situazione è emersa la presenza di un nuovo file non ancora
tracciato e la necessità di eseguire il comando git add nel caso lo si
voglia ricomprendere tra i file da sottoporre a versionamento.

-  Un ulteriore caso può essere quello in cui un file in precedenza già
   tracciato viene modificato (es. il file documentazione.txt).
   L’esecuzione del comando git status successivamente alla modifica del
   file restituirebbe una situazione del tipo:

*$ git status*

*On branch master*

*Changes to be committed:*

*(use "git reset HEAD <file>..." to unstage)*

*new file: analisi.txt*

*Changes not staged for commit:*

*(use "git add <file>..." to update what will be committed)*

*(use "git checkout -- <file>..." to discard changes in working
directory)*

*modified: documentazione.txt*

La situazione rappresentata espone sia il nuovo file aggiunto (vedi
esempio precedente) sia il file documentazione.txt sottoposto a
modifica.

Come si può notare il primo appare nella sezione *Changes to be
committed* e può quindi essere committato attraverso il comando git
commit, mentre il secondo appare nella sezione *Changes not staged for
commit* e per esso sarà necessario eseguire il comando *git add
documentazione.txt* al fine di poter eseguire un successivo *git commit
–m ‘…….’*.

Visualizzare le differenze
==========================

Git status consente di individuare i file che hanno subito delle
modifiche ma non consente di capire quali cambiamenti siano stati
apportati agli stessi file.

Tale esigenza è soddisfatta dal comando **git diff** che può essere
eseguito con o senza il suffisso **--cached**.

**git diff** permette di visualizzare le eventuali modifiche non ancora
ricomprese nello stage.

**git diff --cached** permette di visualizzare le eventuali modifiche
ricomprese nello stage.

Branch
------

Con il termine branch si fa riferimento a una linea di sviluppo
collegata ma indipendente dalla linea di sviluppo principale vale a dire
il branch master. Attraverso il comando git branch è possibile creare
delle “diramazioni” nelle quali è possibile effettuare modifiche ed
aggiornamenti di file senza che le stesse modifiche interferiscano con i
file o il codice ricompreso nel branch master.

| I branch (e quindi i file ad esso collegati) possono poi essere in
  qualche modo ricondotti al master attraverso una apposita procedura di
  merging.
| I comandi principali sono git branch per la creazione della
  diramazione e git checkout per il posizionamento sulla stessa.
| Ad esempio:

*$ git branch area_svi (creazione diramazione)*

*$ git checkout area_svi (posizionamento nel ramo creato)*

*$ vim test.txt (creazione di un nuovo file)*

*$ git commit -a -m 'nuovo doc' (add e commit relativo al nuovo file
creato nel nuova branch area_svi)*

| Il file creato, attraverso il commit, viene “attribuito” al branch e
  non risulta facente parte dei file attribuiti al master o radice
  principale memorizzata nel repository locale. In tal modo è possibile
  isolare eventuali sviluppi che non si desidera immediatamente
  attribuire al master.
| Nel caso, infine, si voglia ricomprendere quanto realizzato nel branch
  all’interno del master:

*$ git checkout master*

*$ git merge* *area_svi*

Controllo dello stato dei Branch
--------------------------------

Si fa presente che il generico comando **git branch** consente di
ottenere la lista dei rami correnti, es:

*$ git branch*

*area_svi*

*\* master*

*area_svi_2*

L’asterisco indica in quale branch siamo posizionati.

Un ulteriore controllo può riguardare la verifica di quali branch siano
stati fusi nel ramo master principale. Attraverso il comando **git
branch –merged**, es:

*$ git branch --merged*

*area_svi*

*\* master*

Al contrario il comando **git branch –no-merged** permette di
visualizzare i branch non ancora fusi nel master principale, es:

*$ git branch –no-merged*

*area_svi_2*

Rimuovere un file
-----------------

Nel caso in cui si intenda escludere uno specifico file da un successivo
commit (rimozione dall’area di stage) il comando da utilizzare
corrisponde a **git reset HEAD <file>**.

*$ git status*

*On branch master*

*Changes to be committed:*

*(use "git reset HEAD <file>..." to unstage)*

*modified: analisi.txt*

*modified: documentazione.txt*

Nell’esempio si mostra la rimozione del file analisi.txt dalla lista dei
file da committare:

*$*\ **git reset HEAD analisi.txt**

*Unstaged changes after reset:*

*M analisi.txt*

*$ git status*

*On branch master*

*Changes to be committed:*

*(use "git reset HEAD <file>..." to unstage)*

*modified: documentazione.txt*

*Changes not staged for commit:*

*(use "git add <file>..." to update what will be committed)*

*(use "git checkout -- <file>..." to discard changes in working
directory)*

*modified: analisi.txt*

Annullare una modifica
----------------------

| Il precedente esempio ci permette di introdurre una ulteriore funzione
  di modifica, vale a dire il comando **git checkout -- <file>**.
| Attraverso il git status (esempio 3.8) è emerso che il file
  *analisi.txt* risulta modificato e non ricompreso nell’area di stage.
| Il sistema ci informa, inoltre, che è possibile annullare le modifiche
  apportate al file analisi.txt attraverso il comando git checkout --
  <file> rimuovendole dunque dalla directory di lavoro

Nello specifo l’esecuzione del comando porterebbe a\ *:*

*$ git checkout – analisi.txt*

*$ git status*

*On branch master*

*Changes to be committed:*

*(use "git reset HEAD <file>..." to unstage)*

*modified: documentazione.txt*

Fork: lavorare con diversi utenti tramite 
------------------------------------------

Per poter effettuare degli interventi sul repository di un altro utente, è consigliabile operare su un “fork”.
--------------------------------------------------------------------------------------------------------------

Il fork è una copia di un progetto, che viene salvata sul proprio
account, e consente quindi di effettuare su questa copia le modifiche e
quando tali modifiche sono completate, è possibile inviare al
proprietario del progetto originale una richiesta di merge.

Documentazione tecnica
======================

Git è lo strumento previsto dall’AgID per la pubblicazione di documenti
tecnici e amministrativi, come descritto su Docs Italia
https://docs.italia.it/come-pubblicare/

Per una più ampia consultazione e apprendimento si elencano alcuni siti
aventi ad oggetto la materia trattata:

https://git-scm.com/book/it/v1/Per-Iniziare-Basi-di-Git

https://www.html.it/guide/git-la-guida/

https://it.atlassian.com/git/tutorials/learn-git-with-bitbucket-cloud

https://www.01net.it/sette-consigli-git-github/

.. |image0| image:: ./media/image1.png
   :width: 6.0087in
   :height: 6.37133in
.. |image1| image:: ./media/image2.png
   :width: 3.59375in
   :height: 2.79675in
.. |image2| image:: ./media/image3.png
   :width: 5.16602in
   :height: 4.02033in
.. |image3| image:: ./media/image4.png
   :width: 5.17781in
   :height: 4.04223in
.. |image4| image:: ./media/image5.png
   :width: 5.21948in
   :height: 4.03181in
.. |image5| image:: ./media/image6.png
   :width: 5.19864in
   :height: 4.03181in
.. |image6| image:: ./media/image7.png
   :width: 5.17781in
   :height: 4.03181in
.. |image7| image:: ./media/image8.png
   :width: 5.21948in
   :height: 4.02139in
.. |image8| image:: ./media/image9.png
   :width: 5.16739in
   :height: 4.03181in
.. |image9| image:: ./media/image10.png
   :width: 5.19864in
   :height: 4.03181in
.. |image10| image:: ./media/image11.png
   :width: 5.16739in
   :height: 4.02139in
.. |image11| image:: ./media/image12.png
   :width: 5.15561in
   :height: 4.06199in
.. |image12| image:: ./media/image13.png
   :width: 4.7375in
   :height: 1.80151in
.. |image13| image:: ./media/image14.png
   :width: 2.93841in
   :height: 1in
   ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
   
   
Creare un Repository su GitHub
==============================
Per creare un Repository su GitHub è necessario registrarsi su GitHub (o accedervi),
cliccare sul **+** in altro a destra nella barra nera e cliccare su **"New repository"**. 
Nella pagina che segue assegnate un **nome** al repository, una **descrizione** (se volete)
e selezionate **Public**. Infine cliccate su **"Create repository""**.

Creare un Repository su GitLab Aziandale
========================================
Per creare un Repository su GitLab è necessario registrarsi su GitLab (o accedervi) e
cliccare il tasto verde con scritto **"New Project"**. Nella pagina che segue assegnate
un **nome**, una **descrizione** (se volete) e selezionate **Private**. Infine cliccate
su **"Create project""**.
