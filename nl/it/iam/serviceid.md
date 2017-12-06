---

copyright:

  years: 2017
lastupdated: "2017-10-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Creazione e gestione degli ID servizio
{: #serviceids}

Un ID servizio identifica un servizio o un'applicazione analogamente a come un ID utente identifica un utente. Un ID servizio da te creato può essere utilizzato per abilitare un'applicazione esterna a {{site.data.keyword.Bluemix_notm}} ad accedere ai tuoi servizi {{site.data.keyword.Bluemix_notm}}. Puoi assegnare delle specifiche politiche di accesso all'ID servizio che limitano le autorizzazioni per l'utilizzo di specifici servizi o anche combinare le autorizzazioni per l'accesso a servizi differenti. Poiché gli ID servizio non sono collegati a uno specifico utente, se capita che un utente lasci un'organizzazione e venga eliminato dall'account, l'ID servizio rimane, garantendo che la tua applicazione o il tuo servizio continuino a essere attivi e in esecuzione.

Quando crei un ID servizio, crei un nome univoco e una descrizione per te facili da identificare e gestire nell'IU. Dopo che hai creato il tuo ID servizio, puoi creare delle chiavi API specifiche per ciascun ID servizio che la tua applicazione può utilizzare per l'autenticazione presso i tuoi servizi {{site.data.keyword.Bluemix_notm}}. Per garantire che la tua applicazione disponga dell'accesso appropriato per eseguire l'autenticazione presso i tuoi servizi {{site.data.keyword.Bluemix_notm}}, utilizzi le politiche di servizio assegnate a ciascun ID servizio che crei. 

Le politiche di accesso associate a un ID servizio abilitano delle specifiche azioni che possono essere eseguite quando tale ID servizio viene utilizzato per accedere a uno specifico servizio. Un singolo ID servizio può avere più politiche assegnate che definiscono il livello di accesso consentito quando si accede a più servizi di identità e abilitati all'accesso e anche a diverse istanze di un singolo servizio. Ad esempio, hai due servizi con due istanze del servizio ciascuno. Puoi ad esempio assegnare il ruolo `Visualizzatore` per tutte le istanze disponibili di un servizio e assegnare il ruolo `Editor` per una sola istanza di un secondo servizio. In questo modo, puoi personalizzare l'accesso a più servizi ma utilizzare una singola chiave API per l'autenticazione per tutti.


## Creazione di un ID servizio

Per creare un ID servizio, vai a **Gestisci** &gt; **Sicurezza** &gt; **Identità e accesso** e quindi seleziona **ID servizio** dal pannello laterale. Attieniti alla procedura per creare un nome e una descrizione per il tuo ID servizio. Usa quindi il menu **Azioni** per gestire il tuo ID servizio. Puoi iniziare assegnando una politica e creando le chiavi API. Per ulteriori informazioni sulla gestione delle chiavi API, consulta [Gestione delle chiavi API di un ID servizio](/docs/iam/serviceid_keys.html#serviceidapikeys). Per i dettagli sui comandi della CLI utilizzati per gestire un ID servizio, consulta il documento relativo ai [comandi per la gestione di politiche e chiavi API](https://console-regional.ng.bluemix.net/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_iam). 

## Aggiornamento di un ID servizio

Puoi aggiornare un ID servizio modificando il nome e la descrizione in qualsiasi momento. Puoi anche eliminare e creare nuove chiavi API come necessario oppure aggiornare le politiche di accesso assegnate. Tuttavia, qualsiasi modifica da te apportata a un ID servizio esistente, quali la modifica delle politiche assegnate o l'eliminazione di una chiave API attualmente utilizzata, potrebbe causare delle interruzioni del servizio per le applicazioni che utilizzano tale ID servizio.


