---

copyright:
  years: 2017
lastupdated: "2017-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:pre: .pre}
{:table: .aria-labeledby="caption"}


# Dettagli dei report in base al tipo

## Accessi firewall
{: #firewalllogins}

Notifica gli eventi correlati all'accesso dell'amministratore ai dispositivi firewall Vyatta.

### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data in cui si è verificato l'evento.</dd>
<dt>Nome evento</dt>
<dd>Il tipo di evento (L'utente non è riuscito ad eseguire l'accesso tramite SSH - password non corretta, Errore di autenticazione, Sessione chiusa, Password accettata per l'utente, Sessione aperta per l'utente).</dd>
<dt>Categoria di livello basso</dt>
<dd>I dettagli dell'evento (Accesso SSH non riuscito, Sessione chiusa, Accesso host riuscito, Sessione aperta).</dd>
<dt>Nome utente</dt> 
<dd>Le credenziali (nome utente) dell'utente che ha avviato la sessione.</dd>
<dt>IP origine</dt>
<dd>L'indirizzo IP dal quale l'utente avvia la sessione.
<dt>IP destinazione</dt>
<dd>La destinazione della sessione.</dd>
<dt>Origine log</dt>
<dd>L'origine dell'evento (il nome host del firewall che ha generato l'evento).</dd>
</dl>

## Accessi firewall negati
{: #firewalldenies}

Notifica gli eventi generati dai dispositivi firewall Vyatta quando una richiesta di accesso viene negata a causa delle regole firewall in vigore.
  
### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data e l'ora in cui si è verificato l'evento.</dd>
<dt>Nome evento</dt>
<dd>Il tipo di evento (L'utente non è riuscito ad eseguire l'accesso tramite SSH - password non corretta, Errore di autenticazione, Sessione chiusa, Password accettata per l'utente, Sessione aperta per l'utente).</dd>
<dt>Categoria di livello basso</dt>
<dd>I dettagli dell'evento di negazione del firewall</dd>
<dt>IP origine</dt> 
<dd>L'indirizzo IP di origine dal quale inizia la connessione di rete e/o l'attacco.</dd>
<dt>Porta di origine</dt>
<dd>La porta di destinazione del protocollo.
<dt>IP destinazione</dt>
<dd>La destinazione della sessione.</dd>
<dt>Porta di destinazione</dt>
<dd>La porta di destinazione del protocollo.</dd>
<dt>Protocollo</dt>
<dd>Il protocollo di comunicazione (tcp/udp).
<dt>Origine log</dt>
<dd>L'origine dell'evento (il nome host del firewall che ha generato l'evento).</dd>
<dt>Conteggio eventi</dt>
<dd>Il numero di eventi di quel tipo.</dd>
</dl>

## Accessi sistema operativo
{: #oslogin}

Notifica gli eventi generati dal sistema operativo quando un amministratore avvia una sessione SSH su un sistema Bluemix.

### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data in cui si è verificato l'evento.</dd>
<dt>Nome evento</dt>
<dd>Il tipo di evento (autenticazione dello spazio utente, errore di autenticazione dello spazio utente)/dd>
<dt>Nome utente</dt> 
<dd>Il nome dell'utente che ha avviato il processo di autenticazione.</dd>
<dt>Indirizzo origine</dt>
<dd>L'indirizzo IP dal quale l'utente avvia la sessione.
<dt>IP destinazione</dt>
<dd>La destinazione della sessione.</dd>
<dt>Origine log</dt>
<dd>L'origine dell'evento (il nome host del server dal quale è stato generato l'evento).</dd>
</dl>

## Accessi al server di login 
{: #loginserverlogins}

Notifica gli eventi generati dal componente di accesso della piattaforma Bluemix quando un utente della piattaforma Bluemix avvia una sessione utilizzando la riga di comando, le API REST oppure la console Bluemix.

### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data in cui si è verificato l'evento.</dd>
<dt>Nome evento</dt>
<dd>Il tipo di evento (Autenticazione dello spazio utente, Errore di autenticazione dello spazio utente)/dd>
<dt>Utente</dt> 
<dd>L'ID dell'utente che ha avviato il processo di autenticazione.</dd>
<dt>Componente_piattaforma_Bluemix</dt>
<dd>Il componente che ha generato l'evento (server_di_login).
<dt>Tipo di messaggio</dt>
<dd>Il tipo di operazione (accesso, disconnessione).</dd>
<dt>Stato</dt>
<dd>Il risultato dell'operazione (riuscito/non riuscito).</dd>
<dt>Origine log</dt>
<dd>L'origine dell'evento.</dd>
</dl>

## Gestione database
{: #dbadmin}

Notifica gli eventi correlati alle operazioni eseguite da un amministratore del database sui database interni Bluemix.

### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data in cui si è verificato l'evento.</dd>
<dt>Tipo_di_evento</dt>
<dd>Il tipo di evento (SECURITY_RUNTIME).
<dt>Utente</dt> 
<dd>Il nome dell'utente che ha eseguito l'operazione. I seguenti sono gli utenti definiti per il database.
<ul>
<li>UAADB: vcap, root, backup_user.
<li>CCDB: vcap, ccadmin, backup_user.
<li>Un utilizzo che non rientra in quanto sopra indicato richiederà delle indagini per appurare chi ha eseguito l'operazione. Tale operazione può essere eseguita utilizzando i report di sicurezza Gestione sistema operativo e Accesso sistema operativo.
</ul>
</dd>
<dt>Origine</dt> 
<dd>L'indirizzo IP dal quale l'utente avvia il comando. I valori previsti sono i seguenti:
<ul>
<li>UAADB – VM uaa e VM nfs_WAL_server.
<li>CCDB – VM api_worker, clock_global, cloud_controller_ng e nsf_WAL_server.
</ul>
</dd>
<dt>Istruzione_DB</dt>
<dd>Il tipo di operazione (tutte le istruzioni di definizione di dati, come CREATE, ALTER e DROP, più quelle che modificano i dati, come INSERT, UPDATE, DELETE, TRUNCATE e COPY FROM)</dd>
<dt>Nome_DB</dt>
<dd>Il nome del DB dove è stata eseguita l'operazione</dd>
</dl>

## Gestione utente della console di gestione
{: #acusermgmt}

Notifica le attività di gestione utente eseguite sulla console di gestione Bluemix.

### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data in cui si è verificato l'evento.</dd>
<dt>Tipo_di_evento</dt>
<dd>Il tipo di evento (SECURITY_RUNTIME).
<ul>
<li>SECURITY_MGMT_REGISTRY: Aggiungi utente [ID utente]
<li>SECURITY_MGMT_REGISTRY: Elimina utente [ID utente]
<li>SECURITY_AUTHN_CREDS_MODIFY: Aggiungi autorizzazione [autorizzazioni] agli utenti [ID utente].
<li>SECURITY_AUTHN_CREDS_MODIFY: Rimuovi autorizzazione [autorizzazioni] dagli utenti [ID utente].
<li>SECURITY_MGMT_CONFIG: Crea organizzazione [nome].
<li>SECURITY_MGMT_CONFIG: Modifica gestori organizzazione, [id].
<li>SECURITY_MGMT_CONFIG: Rinomina ID organizzazione [id] al nuovo nome [nome].
<li>SECURITY_MGMT_CONFIG: Elimina l'ID organizzazione [id].
<li>SECURITY_MGMT_CONFIG: Aggiorna quota per l'organizzazione [id] alla quota [pianoQuota].
</ul>
</dd>
<dt>Utente</dt> 
<dd>L'utente che ha avviato l'operazione (ID LDAP).
<dt>Messaggio</dt> 
<dd>Comando eseguito.
<ul>
<li>Aggiungi utente [ID utente] - Aggiunge un utente con l'ID specificato.
<li>Elimina utente [ID utente] - Elimina un utente con l'ID specificato.
<li>Aggiungi autorizzazione [autorizzazioni] agli utenti [ID utente] - Aggiunge le autorizzazioni agli utenti specificati. Le autorizzazioni possono includere:
ops.admin, ops.login, ops.reports.read, ops.reports.write, ops.catalog.read, ops.catalog.write, ops.users.read e ops.user.write.
<li>Rimuovi autorizzazione [autorizzazioni] dagli utenti [ID utente] - Rimuove l'autorizzazione. Rimuovi le autorizzazioni dagli utenti specificati. Le autorizzazioni possono includere- ops.admin, ops.login, ops.reports.read, ops.reports.write, ops.catalog.read, ops.catalog.write, ops.users.read e ops.users.write.
<li>Crea organizzazione [nome] - Crea un'organizzazione con il nome specificato.
<li>Modifica i gestori dell'organizzazione [id] - Configura i gestori di un'organizzazione in modo che siano gli utenti specificati.
<li>Rinomina ID organizzazione [id] al nuovo nome [nome] - Rinomina l'organizzazione specificata.
<li>Elimina utente [ID utente] - Elimina un utente con l'ID specificato.
<li>Elimina l'ID organizzazione [id] - Elimina l'organizzazione specificata.
<li>Aggiorna quota per l'organizzazione [id] alla quota [pianoQuota] - Aggiorna il piano della quota per un'organizzazione. I piani possono includere: q2GB, q4GB, q8GB, q16GB, q32GB, q64GB, q128GB, q256GB, q512GB.
</ul>
</dd>
<dt>Origine log</dt>
<dd>L'origine dell'evento (l'indirizzo IP/il nome host del server che ha generato l'evento)</dd>
</dl>

## Gestione catalogo
{: #catalogmgmt}

Notifica gli eventi correlati alle attività di gestione del catalogo dei servizi eseguiti sulla console di gestione Bluemix. 

### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data in cui si è verificato l'evento.</dd>
<dt>SECURITY_MGMT_CONFIG</dt>
<dd>Registra modello [id]. Abilita la visualizzazione di un contenitore tipo o di un runtime con l'ID specificato come un'opzione nel catalogo per tutti gli utenti.</dd>
<dd>Annulla registrazione modello [id]. Fa in modo che un contenitore tipo o un runtime non siano più visualizzati come un'opzione nel catalogo per tutti gli utenti.</dd>
<dd>Aggiorna il piano di servizio [id] a pubblico = [ public ] con le visibilità = [ id ]. Aggiorna la visibilità del piano di servizio specificato. Se public è impostato su true, il piano è visibile per tutte le organizzazioni. Se public è impostato su false, potrebbe essere fornita una serie di ID organizzazione per indicare quali organizzazioni hanno la visibilità per questo piano di servizio.</dd>
<dd>Aggiungi broker dei servizi [nome]. Aggiunge un broker dei servizi con il nome specificato.</dd>
<dd>Elimina broker dei servizi [nome]. Elimina il broker dei servizi con il nome specificato.</dd>
<dd>Aggiorna pacchetto di build [id]. Aggiorna l'ordine per il pacchetto di build con l'ID specificato.</dd>
<dt>Origine log</dt>
<dd>L'origine dell'evento (l'indirizzo IP/il nome host del server che ha generato l'evento)</dd>
</dl>

## Gestione dei report di sicurezza
{: #securityreportsmgmt}

Notifica gli eventi correlati alle attività di gestione dei report di sicurezza eseguite sulla console di gestione.

### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data in cui si è verificato l'evento.</dd>
<dd>Il tipo di evento (SECURITY_RUNTIME).
<ul>
<li>SECURITY_DATA_SYNC: Carica report [nome] alla categoria [nome] data [data].
Elimina report con ID [id]
<li>SECURITY_RESOURCE_ACCESS: Scarica report [nome].
</ul>
</dd>
<dt>Utente</dt> 
<dd>L'utente che ha avviato l'operazione.
<dt>Messaggio</dt> 
<dd>Comando eseguito.
<ul>
<li>Carica report [nome] alla categoria [nome] data [data] - Carica. Carica un report con il nome file e la data specificati nella categoria indicata. 
<li>Elimina report con ID [id] - Elimina. Elimina un report con l'ID specificato.
<li>Scarica report [nome] - Scarica. Viene scaricato un report con il nome specificato.
</ul>
</dd>
<dt>Origine log</dt>
<dd>L'origine dell'evento (l'indirizzo IP/il nome host del server che ha generato l'evento)</dd>
</dl>

## Revisioni accesso
{: #accessreviews}

Notifica le richieste per gli accessi privilegiati all'ambiente Bluemix e la loro elaborazione da parte degli amministratori Bluemix. 

### Campi di dati

<dl>
<dt>Nome_azione</dt>
<dd>Indica la richiesta da parte di un utente di fare parte di un gruppo, di rinominare l'id-utente, di essere revocato in caso di destituzione, di essere rimosso da un gruppo (Addp, Rename, Revoke, Delete).</dd>
<dt>Stato</dt>
<dd>Questo campo indica lo stato della richiesta. Il responsabile dell'approvazione accetta la richiesta o la rifiuta. La richiesta è in attesa di approvazione. L'utente annulla la richiesta (Accettato, Rifiutato, In sospeso, Annullato).</dd>
<dt>Utente_ID</dt>
<dd>Nome utente</dd>
<dt>Nome_utente</dt> 
<dd>L'utente che sta effettuando la richiesta.</dd>
<dt>Approvazione_responsabile</dt>
<dd>La data in cui la richiesta è stata approvata dal gestore
<dt>Approvazione_accesso</dt>
<dd>La data in cui la richiesta è stata approvata dal gestore del gruppo.</dd>
</dl>

## Gestione chiavi
{: #keymgmt}

Notifica le operazioni di gestione dei certificati chiave

### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data in cui si è verificato l'evento.</dd>
<dt>Nome_evento</dt>
<dd>Il tipo di evento (Creazione chiave, Creazione certificato, Eliminazione certificato).</dd>
<dt>Nome chiave/certificato</dt>
<dd>Il nome del certificato o quello della chiave utilizzato.</dd>
<dt>Messaggio_gestione_chiave</dt> 
<dd>Comando eseguito (Creazione della chiave "nome chiave", Creazione del certificato "nome certificato", Configurazione certificato "nome certificato" eliminata).</dd>
<dt>IP destinazione</dt>
<dd>La destinazione della sessione.
<dt>Origine log</dt>
<dd>L'origine dell'evento.</dd>
</dl>

## Notifiche di sistema
{: #systemnotifications}

Notifica gli eventi correlati alla configurazione delle finestre di distribuzione degli aggiornamenti software o delle sottoscrizioni di notifica.

### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data in cui si è verificato l'evento.</dd>
<dt>Tipo_di_evento</dt>
<dd>Il tipo di evento (SECURITY_RUNTIME).
<ul>
<li> SECURITY_MGMT_CONFIG: Crea finestra [id].
<li> SECURITY_MGMT_CONFIG: Aggiorna finestra [id].
<li> SECURITY_MGMT_CONFIG: Elimina finestra [id].
<li> SECURITY_MGMT_CONFIG: Crea sottoscrizione [id].
<li> SECURITY_MGMT_CONFIG: Aggiorna sottoscrizione [id].
<li> SECURITY_MGMT_CONFIG: Elimina sottoscrizione [id].
<li> SECURITY_MGMT_CONFIG: Crea risposta argomento [id].
</ul>
</dd>
<dt>Utente</dt> 
<dd>L'utente che ha avviato l'operazione
<dt>Messaggio</dt>
<dd>Comando eseguito.
<ul>
<li>Crea finestra [id] - Crea una finestra per gli aggiornamenti di manutenzione. I log della finestra di aggiornamento vengono generati quando un utente gestisce (crea) le finestre di aggiornamento per un ambiente. Le finestre di aggiornamento sono le finestre di blackout e preferite per le distribuzioni. Indica quando i clienti stanno consentendo/non consentendo l'attuazione di distribuzioni che non comportano interruzioni del servizio senza dovere approvarle e pianificarle.
<li>Aggiorna finestra [id] - Aggiorna una finestra di aggiornamento di manutenzione. Questo evento viene generato quando un utente aggiorna le finestre di aggiornamento di manutenzione per un ambiente.
<li>SECURITY_MGMT_CONFIG - Elimina finestra di aggiornamento - questo evento viene generato quando un utente delega le finestre di aggiornamento per un ambiente.
<li>Crea sottoscrizione [id] - Crea una sottoscrizione evento. I log di controllo della sottoscrizione evento vengono generati quando un utente crea una sottoscrizione per gli eventi di aggiornamento o incidente. Ciò permetterà di essere avvisati quando succede qualcosa nel sistema.
<li>Aggiorna sottoscrizione [id] - Aggiorna una sottoscrizione evento. L'evento viene generato quando un utente aggiorna una sottoscrizione per gli eventi di aggiornamento o incidente.
<li>Elimina sottoscrizione [id] - Elimina una sottoscrizione evento. Questo evento viene generato quando un utente elimina una sottoscrizione per gli eventi di aggiornamento o incidente.
<li>Crea risposta argomento [id] - Risponde a un argomento. I log di controllo della risposta argomento viene generato quando il cliente approva e pianifica un aggiornamento con interruzione del servizio.
</ul>
</dd>
<dt>Origine log</dt>
<dd>L'origine dell'evento (l'indirizzo IP/il nome host del server che ha generato l'evento).</dd>
</dl>

## Gestione piattaforma Bluemix
{: #platformadmin}

Notifica gli eventi correlati alla piattaforma Bluemix utilizzando la riga di comando, le API REST o l'interfaccia utente Bluemix.

### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data in cui si è verificato l'evento.</dd>
<dt>Tipo_di_evento</dt>
<dd>Il tipo di evento (SECURITY_RUNTIME).
<ul>
<li>SECURITY_AUTH_CREDS_MODIFY: eventi correlati alle modifiche di credenziali per una specifica identità utente.
<li>SECURITY_MGMT_RESOURCE: eventi di gestione risorse quali la creazione, l'eliminazione e le modifiche per gli attributi di una risorse.
<li>SECURITY_MGMT_POLICY: evento correlato alla gestione delle politiche di sicurezza quali la creazione di elenchi di controllo accessi.
<li>SECURITY_RUNTIME: eventi di runtime quali l'avvio e l'arresto di server di sicurezza.
<li>SECURITY_RESOURCE_ACCESS: eventi che registrano tutti gli accessi a una risorsa. Degli esempi sono tutti gli accessi a un file, tutte le richieste/risposte HTTP a una specifica pagina web, tutti gli accessi a una tabella database critica.
</ul>
</dd>
<dt>Utente</dt> 
<dd>Chi ha avviato l'operazione
<dt>Destinazione</dt> 
<dd>Dettagli dell'operazione eseguita, quale l'ID dell'entità e i risultati dell'operazione. Esempi:
<ul>
<li>UserCreatedEvent ('["user_id=ca3a811f-1778-4103-9553-537788ed4c4e","username=equaranta"]’). L'utente è stato creato con
(username=equaranta e id = ca3a811f-1778-4103-9553-537788ed4c4e).
<li>GroupModifiedEvent ('{" "group_name":"ops.reports.read","members":["0625ff9a- 8a59-4cca-a80a-8e3b51f3dd21","5005f0f8-e090-4cabb51d- 2ceee70acf0e"}'). Il gruppo con il nome ops.reports.read è stato modificato, con l'appartenenza risultante (id 0625ff9a- 8a59-4ccaa80a- 8e3b51f3dd21","5005f0f8- e090-4cab-b51d- 2ceee70acf0e).
<li>UserDeletedEvent ('["UserDeletedEvent ('["user_id=5cd5f412-4bbb-4c44-b44b- 713a5bc6144d","username=818811853"]'):"]'. L'utente è stato eliminato con il valore id=5cd5f412-4bbb- 4c44-b44b-713a5bc6144.
</ul>
</dd>
<dt>Messaggio</dt>
<dd>Entità su cui è stata eseguita l'operazione (stringa messaggio) o il codice di ritorno http standard dell'operazione (valore numerico). </dd>
<dt>Componente_piattaforma_Bluemix</dt>
<dd>Il nome del componente.</dd>
<dt>Origine log</dt>
<dd>Nome host/indirizzo IP dell'origine dell'evento.</dd>
<dt>Origine</dt>
<dd>L'origine dell'evento; un esempio è l'indirizzo IP.</dd>
<dt>Dati</dt>
<dd>Ulteriori dettagli.</dd>
</dl>

## Gestione sistema operativo
{: #osadmin}

Notifica gli eventi generati da Bluemix che potrebbero aiutare a diagnosticare gli errori (ad esempio la mancata riuscita della distribuzione di un agent Bosh o un servizio che non si avvia).

### Campi di dati

<dl>
<dt>Ora di origine log</dt>
<dd>La data in cui si è verificato l'evento.</dd>
<dt>Nome_evento</dt>
<dd>Il tipo di evento (Creazione chiave, Creazione certificato, Eliminazione certificato).</dd>
<dt>Chiave_BMX</dt>
<dd>Il tipo di operazione (BMX_executed_command, BMX_access_unauthorized, BMX_unsuccessful_delete, BMX_sudoers_folder, BMX_Identity_shadow, BMX_extended_attribute, BMX_sudoers).</dd>
<dt>auid</dt> 
<dd>L'ID utente di origine dell'utente che si è collegato (ad es. auid=0 p root, auid=1000 è vcap, auid= 55044 è un utente ldap.</dd>
<dt>uid</dt>
<dd>L'ID utente di destinazione con cui viene eseguito il comando (ad es. auid=55044 è collegato ed esegue un “sudo su” (root) -> uid=0, prima di eseguire il comando).
<dt>Chiave_exe</dt>
<dd>Il comando eseguito.</dd>
<dt>IP origine</dt>
<dd>L'indirizzo IP dal quale l'utente avvia il comando.</dd>
<dt>Origine log</dt>
<dd>L'origine dell'evento.</dd>
</dl>
