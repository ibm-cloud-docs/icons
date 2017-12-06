---

copyright:

  year: 2015, 2016

lastupdated: "2017-10-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Ruoli utente e autorizzazioni
{: #userroles}

Puoi gestire gli utenti attraverso i servizi della piattaforma e dell'infrastruttura {{site.data.keyword.Bluemix_notm}} dalla pagina **Utenti** relativa al tuo account. Per accedere alla pagina Utenti, dal menu {{site.data.keyword.Bluemix_notm}}, fai clic su **Gestione** &gt; **Account** &gt; **Utenti**. I proprietari di account possono eseguire tutte le operazioni per gestire utenti, autorizzazioni, organizzazioni e spazi. I gestori dell'organizzazione e i gestori spazio Cloud Foundry hanno anche accesso alla gestione delle autorizzazioni per gli utenti aggiunti a ogni organizzazione e spazio da essi gestiti.
{:shortdesc}

Se sei un utente aggiunto all'account di un'altra persona e vuoi visualizzare i tuoi ruoli assegnati e le tue autorizzazioni, vai a **Gestisci** &gt; **Sicurezza** &gt; **Identità e accesso** &gt; **Utenti** e fai clic sul tuo nome.

## Ruoli dell'account
{: #userrolesinfo}

A livello di account, esistono due ruoli che abilitano l'accesso a funzioni di gestione dell'account differenti:

| Ruolo dell'account | Autorizzazioni |
|----------------|---------|
|Proprietario | Un proprietario per l'account ha accesso al suo profilo, al dashboard di utilizzo e agli utenti, alle informazioni di fatturazione e alle notifiche di spesa. Dalla pagina Utenti, il proprietario può invitare nuovi utenti e regolare i ruoli. Il proprietario può anche aggiungere dei crediti promozionali, impostare o modificare il limite di fatturazione, impostare l'accesso al servizio e gestire organizzazioni e spazi. |
|Membro | Un membro ha accesso al suo profilo e alla pagina Utenti che visualizza gli utenti attivi nell'account, i crediti dell'account e i limiti di fatturazione nell'intestazione {{site.data.keyword.Bluemix_notm}}.  |
{:caption="Tabella 1. Ruoli e autorizzazioni dell'account" caption-side="top"}

Tutti i nuovi utenti vengono aggiunti come membri dell'account. Puoi assegnare i ruoli organizzazione e spazio agli invitati per abilitare specifiche viste e autorizzazioni in {{site.data.keyword.Bluemix_notm}}. Dopo che gli invitati hanno accettato l'invito e si sono uniti a {{site.data.keyword.Bluemix_notm}}, puoi modificarne i ruoli nella pagina Utenti.

## Ruoli Cloud Foundry
{: #cfroles}

I ruoli Cloud Foundry includono le autorizzazioni di accesso per le organizzazioni e gli spazi definiti nell'account. I ruoli Cloud Foundry non abilitano le autorizzazioni utente per completare le azioni nel contesto di un servizio. I seguenti ruoli possono essere assegnati a livello dell'organizzazione:

| Ruolo organizzazione | Autorizzazioni |
|-------------------|-------------|
|Gestore | I gestori dell'organizzazione possono creare, visualizzare, modificare o eliminare gli spazi nell'organizzazione, visualizzare l'utilizzo e la quota dell'organizzazione, invitare utenti all'organizzazione, gestire chi ha accesso all'organizzazione e i loro ruoli al suo interno e gestire i domini personalizzati per l'organizzazione. |
|Gestore fatturazione | I gestori fatturazione possono visualizzare le informazioni sull'utilizzo di runtime e servizi per l'organizzazione nella pagina Dashboard di utilizzo.  |
|Revisore | I revisori organizzazione possono visualizzare il contenuto di applicazioni e servizi nell'organizzazione. I revisori possono anche visualizzare gli utenti nell'organizzazione e i ruoli ad essi assegnati, nonché la quota per l'organizzazione. |
{:caption="Tabella 2. Ruoli e autorizzazioni dell'organizzazione" caption-side="top"}

I seguenti ruoli possono essere assegnati a livello dello spazio:

| Ruolo spazio | Autorizzazioni |
|------------|-------------|
|Gestore | I gestori spazio possono aggiungere utenti esistenti e gestire i ruoli nello spazio. Il gestore spazio può anche visualizzare il numero di istanze, i bind di servizio e l'utilizzo delle risorse per ciascuna applicazione nello spazio. |
|Sviluppatore | Gli sviluppatori spazio possono creare, eliminare e gestire applicazioni e servizi nello spazio. Alcune delle attività di gestione includono la distribuzione di applicazioni, l'avvio e l'arresto di applicazioni, la rinominazione di un'applicazione, l'eliminazione di un'applicazione, la rinominazione di uno spazio, il bind o l'annullamento del bind di un servizio a un'applicazione, la visualizzazione del numero di istanze, i bind di servizi e l'utilizzo di risorse per ciascuna applicazione nello spazio. Inoltre, lo sviluppatore spazio può associare un URL interno o esterno a un'applicazione nello spazio.   |
|Revisore | I revisori spazio hanno un accesso in sola lettura a tutte le informazioni sullo spazio, quali le informazioni sul numero di istanze, i bind di servizio e l'utilizzo di risorse per ciascuna applicazione nello spazio. |
{:caption="Tabella 3. Ruoli e autorizzazioni dello spazio" caption-side="top"}

**Nota**: gli utenti a cui nello spazio è assegnato il ruolo di gestore o sviluppatore possono accedere alla variabile di ambiente VCAP_SERVICES. Tuttavia, un utente a cui è assegnato il ruolo di revisore non può accedere a VCAP_SERVICES.

## Politiche e ruoli per la gestione di identità e accesso
{: #iamusermanpol}

Ai proprietari dell'account viene assegnato automaticamente il ruolo di amministratore di account per IAM (Identity and Access Management) che ti consente di assegnare e gestire le politiche di servizio. Le politiche di servizio possono essere assegnate a singoli utenti o a ID servizio e la politica assegnata può definire l'accesso per un intero servizio oppure a livello della singola istanza.

### Politiche di servizio

Una politica assegna a un utente o a un ID servizio uno o più ruoli a un insieme di risorse utilizzando una combinazione di attributi per definire l'insieme applicabile di risorse. Quando assegni una politica, devi prima specificare il servizio. Puoi quindi selezionare un ruolo o i ruoli da assegnare. Potrebbero essere disponibili ulteriori opzioni di configurazione, a seconda del servizio che selezioni.

Puoi assegnare e gestire le politiche se hai il ruolo appropriato. La seguente tabella mostra le attività di gestione della politica e il ruolo richiesto per ognuna di esse.

| Azione | Ruolo richiesto |
|----------|---------|
| Creare politiche su un account per tutti i servizi e tutte le istanze | Amministratore dell'account |
| Creare una politica su un servizio in un account | Amministratore dell'account o amministratore sul servizio nell'account |
| Creare un'istanza del servizio | Amministratore dell'account o amministratore o editor sul servizio nell'account |
| Creare una politica su un'istanza del servizio | Amministratore dell'account o amministratore sul servizio nell'account o amministratore dell'istanza del servizio |
{: caption="Tabella 4. Attività amministrative per la gestione delle politiche dei servizi abilitati a IAM" caption-side="top"}

### Ruoli delle politiche di servizio
{: #iamusermanrol}

IAM ti consente di gestire e definire l'accesso per gli utenti e le risorse nel tuo account. Se il servizio che utilizzi può essere gestito utilizzando IAM per il controllo dell'accesso degli utenti, esistono due tipi di ruoli che consentono azioni diverse all'interno del tuo account: i ruoli di gestione della piattaforma e di accesso al servizio.

<dl>
<dt>Ruoli di gestione della piattaforma</dt>
<dd>Ruoli disponibili per tutti i servizi che possono essere gestiti utilizzando IAM per il controllo dell'accesso degli utenti, tra cui i ruoli di amministratore, editor, operatore, visualizzatore e amministratore fatturazione. Questi ruoli sono associati ad azioni utente che possono essere eseguite sulle risorse {{site.data.keyword.Bluemix_notm}} a livello della piattaforma. Ad esempio, alcune di queste azioni includono la capacità di creare istanze, collegare istanze a un'applicazione, gestire gli ID di servizio, gestire gli utenti e le autorizzazioni e gestire la fatturazione e le quote per l'account. </dd>
<dt>Ruoli di accesso al servizio</dt>
<dd>Questi ruoli sono specifici per il servizio. I ruoli di gestore, scrittore e lettore definiscono la capacità dell'utente di utilizzare il servizio e di eseguire chiamate API ai servizi. Poiché ogni servizio definisce le azioni che un utente con un determinato ruolo può eseguire, è possibile che un servizio non utilizzi tutti i ruoli disponibili descritti in questa documentazione. </dd>
</dl>

**Nota**: potresti non visualizzare tutti i ruoli elencati come opzioni durante l'assegnazione delle politiche nell'interfaccia utente perché vengono visualizzati solo i ruoli applicabili al servizio selezionato nella politica. Per informazioni specifiche su quali ruoli sono abilitati e quali azioni sono consentite da ciascun ruolo di accesso per ogni servizio, fai riferimento alla documentazione di quel servizio.


#### Ruoli di gestione della piattaforma

I ruoli di gestione della piattaforma consentono di assegnare agli utenti diversi livelli di autorizzazione per eseguire azioni di piattaforma. Oltre alle descrizioni dei ruoli fornite nella console, le seguenti tabelle forniscono esempi di alcune delle azioni di gestione della piattaforma che gli utenti assegnati ad ogni ruolo possono eseguire.

| Ruolo di gestione della piattaforma  | Azioni che un utente può eseguire sui servizi dell'account | Azioni per gli ID di servizio |
|:-----------------|:--------------|:---------------|
| Visualizzatore | Visualizzare istanze | Visualizzare ID e chiavi API |
| Operatore |  Visualizzare e associare istanze del servizio | Non applicabile |
| Editor |  Creare, eliminare, modificare, sospendere, riprendere, visualizzare e associare istanze del servizio | Eliminare ID e creare ed eliminare chiavi API |
| Amministratore |  Tutte le azioni di gestione per i servizi | Creare ed eliminare ID e chiavi API, assegnare politiche agli ID |
{: caption="Tabella 5. Ruoli e azioni di esempio per la gestione della piattaforma" caption-side="top"}

Alcuni servizi potrebbero associare specifiche azioni ai ruoli di gestione della piattaforma correlati alla gestione del servizio piuttosto che all'accesso del servizio. Come esempio, consulta la seguente tabella che descrive le azioni del servizio {{site.data.keyword.containershort_notm}} associate a questi ruoli.


| Ruolo di gestione della piattaforma | Descrizione delle azioni | Azioni di esempio per il servizio {{site.data.keyword.containershort_notm}} |
|:-----------------|:-----------------|:-----------------|
| Visualizzatore | Può visualizzare le istanze del servizio ma non può modificarle  | <ul><li>Elencare i cluster</li><li>Visualizzare i dettagli per un cluster</li></ul>|
| Editor | Eseguire tutte le azioni di piattaforma eccetto la gestione dell'account e l'assegnazione delle politiche di accesso |<ul><li>Eseguire il bind di un servizio a un cluster</li><li>Crea un webhook</li></ul> |
| Operatore | Eseguire le azioni di piattaforma necessarie per configurare e gestire le istanze del servizio, come ad esempio visualizzare il dashboard di un servizio. | <ul><li>Aggiungere o rimuovere i nodi di lavoro</li><li>Riavviare o ricaricare i nodi di lavoro</li><li>Eseguire il bind di un servizio a un cluster</li></ul> |
| Amministratore | Esegue tutte le azioni di piattaforma in base alla risorsa assegnata a questo ruolo, inclusa l'assegnazione di politiche di accesso ad altri utenti. |<ul><li>Rimuovere un cluster</li><li>Creare un cluster</li><li>Aggiorna le politiche di accesso utente</li><li>Tutte le azioni che possono essere eseguite da un visualizzatore, un operatore e un editor</li></ul>|
{: caption="Tabella 6. Ruoli e azioni di esempio per la gestione della piattaforma" caption-side="top"}


#### Ruoli di accesso al servizio

I ruoli di accesso al servizio consentono di assegnare agli utenti diversi livelli di autorizzazione per richiamare l'API del servizio. La seguente tabella descrive le azioni di esempio che possono essere eseguite a seconda dei ruoli di accesso al servizio assegnati in base all'utilizzo del servizio {{site.data.keyword.objectstorageshort}}.

**Nota**: le azioni che possono essere eseguite per ogni ruolo assegnato variano in base al servizio selezionato per la politica.

| Ruolo di accesso al servizio | Descrizione delle azioni | Azioni di esempio per il servizio {{site.data.keyword.objectstorageshort}} |
|:-----------------|:-----------------|:-----------------|
|  Lettore | Eseguire azioni di sola lettura all'interno di un servizio, ad esempio visualizzare le risorse specifiche del servizio | Elencare e scaricare oggetti |
| Scrittore | Gli scrittori dispongono di autorizzazioni al di sopra del ruolo di lettore, incluse la creazione e la modifica di risorse specifiche del servizio. | Creare ed eliminare bucket e oggetti |
| Gestore | I gestori dispongono di autorizzazioni al di sopra del ruolo di scrittore per completare le azioni privilegiate definite dal servizio. Inoltre, puoi creare e modificare le risorse specifiche del servizio. | Gestire tutti gli aspetti dell'archiviazione dati, creare ed eliminare bucket e oggetti |
{: caption="Tabella 7. Ruoli utente e azioni di esempio per l'accesso al servizio" caption-side="top"}


## Autorizzazioni dell'infrastruttura
{: #infrapermissions}

Quando inviti un utente, puoi impostare le seguenti autorizzazioni iniziali:

| Autorizzazione impostata | Descrizione delle azioni |
|---------------------------|------------------------|
|Solo visualizzazione | Gli utenti con questa autorizzazione possono soltanto visualizzare gli elementi nel sistema.|
|Utente base | Gli utenti con questa autorizzazione possono eseguire le azioni di base nel sistema, come aggiungere un ticket e gestire i dispositivi. |
|Super utente | Gli utenti con questa autorizzazione possono eseguire tutte le azioni disponibili nel sistema. |
{:caption="Tabella 8. Autorizzazioni dell'infrastruttura" caption-side="top"}

Ulteriori autorizzazioni possono essere impostate dopo che l'utente ha accettato l'invito. L'autorizzazione iniziale impostata al momento dell'invito non concede l'accesso ai dispositivi; devi pertanto concedere l'accesso ai dispositivi nel portale di controllo dopo che l'utente ha accettato l'invito.
