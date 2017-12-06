---

copyright:
  years: 2015, 2017
  
lastupdated: "2017-06-01"

---

{:tsSymptoms: .tsSymptoms} 
{:tsCauses: .tsCauses} 
{:tsResolve: .tsResolve} 
{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}
{:codeblock: .codeblock} 


# Risoluzione dei problemi relativi alla gestione degli account
{: #managingaccounts}

I problemi generali con la gestione del tuo account potrebbero riguardare applicazioni diverse che condividono lo stesso nome dominio o amministratori che non riescono a visualizzare tutte le organizzazioni. In molti casi, puoi risolvere questi problemi seguendo pochi semplici passi.
{:shortdesc}

## Impossibile accedere a una regione {{site.data.keyword.Bluemix_notm}} differente
{: #nosecondreg}

Ricevi un messaggio di errore quando provi a creare una nuova regione {{site.data.keyword.Bluemix_notm}}. 
{: tsSymptoms}

Ciò è probabilmente dovuto al fatto che stai utilizzando un account Standard, che supporta lo sviluppo solo in una regione pubblica. Selezioni la regione pubblica di {{site.data.keyword.Bluemix_notm}} in cui vuoi lavorare durante la configurazione iniziale dell'account. 
{: tsCauses}

Se hai un account Standard, puoi eseguire l'upgrade a un account fatturabile per accedere a ulteriori regioni. Vai alla pagina **Gestisci > Fatturazione e utilizzo > Fatturazione** nella console e fai clic su **Aggiungi carta di credito**. Nella pagina **Fatturazione**, puoi anche controllare se hai un account Standard.
{: tsResolve}

## Impossibile creare la nuova organizzazione
{: #nosecondorg}
 
Ricevi un messaggio di errore quando provi a creare una nuova organizzazione. 
{: tsSymptoms}

Ciò è probabilmente dovuto al fatto che stai utilizzando un account Standard, che supporta lo sviluppo solo in una singola organizzazione. Crei l'organizzazione durante la configurazione iniziale del tuo account. 
{: tsCauses}

Se hai un account Standard, puoi eseguire l'upgrade a un account fatturabile per accedere a ulteriori organizzazioni. Vai alla pagina **Gestisci > Fatturazione e utilizzo > Fatturazione** nella console e fai clic su **Aggiungi carta di credito**. Nella pagina **Fatturazione**, puoi anche controllare se hai un account Standard.
{: tsResolve}

## Impossibile creare la nuova istanza del piano Lite
{: #nosecondlite}

Viene visualizzato il seguente messaggio di errore quando provi a creare una nuova istanza del piano Lite:
{: tsSymptoms}

`Unable to provision new Lite instance`

Esiste un limite di una singola istanza per istanza del piano Lite per consentirci di continuare a offrire tali piani gratuitamente. 
{: tsCauses}

Puoi creare delle istanze aggiuntive del servizio selezionando uno dei piani del servizio fatturabili, disponibili negli account fatturabili. Per eseguire l'upgrade a un account fatturabile dalla console, vai alla pagina **Gestisci > Fatturazione e utilizzo > Fatturazione** e fai clic su **Aggiungi carta di credito**.
{: tsResolve}

Se non vuoi eseguire l'upgrade da un account Standard e non stai più utilizzando la tua istanza del servizio Lite esistente, puoi eliminare l'istanza del piano Lite esistente dal dashboard Servizi e creare quindi una nuova istanza. 

## È stata superata la franchigia di memoria di runtime
{: #noruntimemem}

Non riesci a distribuire applicazioni e ottieni un errore che indica che hai superato il limite di memoria della tua organizzazione.
{: tsSymptoms}

In un account Standard, le tue applicazioni Cloud Foundry possono utilizzare fino a 256 MB di memoria di runtime istantanea. Negli account fatturabili, esiste un limite di memoria di 2GB.
{: tsCauses}

Se stai utilizzando un account Standard, puoi ottenere della memoria aggiuntiva eseguendo l'upgrade a un account fatturabile. Vai alla pagina **Gestisci > Fatturazione e utilizzo > Fatturazione** nella console e fai clic su **Aggiungi carta di credito**.
{: tsResolve}

Se non vuoi eseguire l'upgrade da un account Standard ma hai delle applicazioni inattive, le puoi eliminare per liberare della memoria di runtime. 

## Account non attivo
{: #ts_accnt_inactive}

Non puoi creare un'applicazione in {{site.data.keyword.Bluemix_notm}} se il tuo account non è attivo. Per risolvere questo problema, devi contattare il team di supporto.

Quando tenti di creare un'applicazione in {{site.data.keyword.Bluemix_notm}}, viene visualizzato il seguente messaggio di errore:
{: tsSymptoms} 

`BXNUI0096E: L'applicazione non è stata creata. Il tuo account non è attivo perché è stato annullato o sospeso.`

Lo stato del tuo account {{site.data.keyword.Bluemix_notm}} diventa inattivo quando l'account viene annullato o sospeso.
{: tsCauses}


Per riattivare il tuo account, contatta il [Supporto {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://ibm.biz/bluemixsupport.com){: new_window}. Includi le seguenti informazioni nell'e-mail:
{: tsResolve}

  * L'ID IBM utilizzato per accedere a {{site.data.keyword.Bluemix_notm}}.
  * Il nome dell'organizzazione in cui verrà creata la tua applicazione. Queste informazioni consentono al team di supporto di determinare se ti sono stati assegnati i ruoli o l'appartenenza appropriati nella tua organizzazione.


## Nessuno spazio associato alla tua organizzazione corrente
{: #ts_no_space}

Non puoi creare un'applicazione se non vi è alcuno spazio associato alla tua organizzazione corrente.

Quando tenti di creare un'applicazione in {{site.data.keyword.Bluemix_notm}}, viene visualizzato il seguente messaggio di errore:
{: tsSymptoms} 

`BXNUI0097E: Prima di poter aggiungere un'applicazione, è necessario associare almeno uno spazio alla tua organizzazione e alla tua regione. Sul Dashboard, fai clic su Crea uno
spazio. Una volta creato lo spazio, prova di nuovo. `

Le applicazioni in {{site.data.keyword.Bluemix_notm}} devono essere create in uno spazio della tua organizzazione.
{: tsCauses} 

Per creare uno spazio, utilizza uno dei seguenti metodi: 
{: tsResolve}
 
  * Sul Dashboard {{site.data.keyword.Bluemix_notm}}, seleziona l'organizzazione in cui vuoi creare lo spazio e fai quindi clic su **Crea uno spazio**.
  * Nell'interfaccia riga di comando cf, immetti `cf create-space <space_name> -o <organization_name>`.

  
## Le applicazioni condividono lo stesso nome di dominio
{: #ts_domain_diff}

Potresti notare che diverse applicazioni condividono lo stesso URL in {{site.data.keyword.Bluemix_notm}}.

Questo problema potrebbe verificarsi se assegni la stessa rotta URL per le diverse applicazioni in uno spazio.
{: tsCauses}

Ad esempio, esegui il push dell'applicazione myApp1 a {{site.data.keyword.Bluemix_notm}} e imposta il dominio su "mynewapp.stage1.mybluemix.net". Esegui quindi il push di un'altra applicazione myApp2 allo stesso spazio e imposta una delle sue rotte URL su "mynewapp.stage1.mybluemix.net". La rotta è ora associata a entrambe le applicazioni.

Questo è il funzionamento supportato da {{site.data.keyword.Bluemix_notm}} e puoi utilizzare questa procedura affinché non si verifichino tempi di inattività per l'aggiornamento della tua applicazione. Per ulteriori informazioni, vedi [Using Blue-Green Deployment to Reduce Downtime and Risk ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://docs.cloudfoundry.org/devguide/deploy-apps/blue-green.html){: new_window}.
{: tsResolve}
  

## Gli amministratori non possono visualizzare tutte le organizzazioni utilizzando l'interfaccia utente {{site.data.keyword.Bluemix_notm}}
{: #ts_ui_org}

In qualità di amministratore, quando utilizzi l'interfaccia utente {{site.data.keyword.Bluemix_notm}}, non riesci a visualizzare tutte le organizzazioni per gestirle. Puoi visualizzare e gestire solo le organizzazioni alle quali appartieni.

In qualità di amministratore, non puoi visualizzare tutte le organizzazioni utilizzando l'interfaccia utente {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Questa è una limitazione dell'interfaccia utente {{site.data.keyword.Bluemix_notm}}.
{: tsCauses}

Puoi utilizzare i comandi come `cf orgs`, `cf create-org` e `cf delete-org` dall'interfaccia riga di comando cf per gestire tutte le organizzazioni. Per un elenco completo dei comandi cf, immetti `cf help`.
{: tsResolve}
	
## Impossibile aggiungere la carta di credito
{: #ts_addcc}

Non puoi inoltrare le informazioni della tua carta di credito per convertire il tuo account di prova in un account con pagamento a consumo.

Il pulsante **Inoltra** nella pagina Aggiungi carta di credito è disabilitato.
{: tsSymptoms}

Questo problema si verifica se non compili correttamente le tue informazioni nella pagina Aggiungi carta di credito.
{: tsCauses}


Completa
la seguente procedura:
{: tsResolve}

  1. Nella pagina Aggiungi carta di credito, compila tutti i campi obbligatori nelle sezioni relative a informazioni di contatto, indirizzo di contatto e indirizzo di fatturazione.
  2. Seleziona **Ho letto e accetto i termini e le condizioni IBM**
e fai clic su **Inoltra**. Viene visualizzata la sezione **Seleziona un
metodo di pagamento**.
  3. Immetti il numero della tua carta di credito, la data di scadenza e il codice di sicurezza indicato sulla carta. Fai quindi clic su **Inoltra**.
