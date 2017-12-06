---

copyright:

  years: 2015, 2017
lastupdated: "2017-10-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Invito di utenti e assegnazione dell'accesso
{: #iamuserinv}

Puoi invitare gli utenti con le applicazioni, i servizi {{site.data.keyword.Bluemix_notm}} e l'infrastruttura {{site.data.keyword.Bluemix_notm}} da una sola ubicazione. Per invitare gli utenti e gestire gli inviti in sospeso, devi essere un proprietario dell'account, un gestore dell'organizzazione o devi avere la autorizzazioni dell'infrastruttura per aggiungere gli utenti. Puoi invitare gli utenti, annullare gli inviti e reinviare un invito in sospeso a un utente invitato. Puoi invitare un solo utente o, se stai fornendo lo stesso accesso a tutti i membri in un gruppo di utenti, puoi invitare più utenti contemporaneamente.  
{:shortdesc}

## Invito di utenti

Per invitare gli utenti o per gestire gli inviti utente nel tuo account, completa la seguente procedura: 

1. Dalla barra dei menu, fai clic su **Gestisci** &gt; **Sicurezza** &gt; **Identità e accesso** &gt; **Utenti**. La finestra Utenti visualizza un elenco di utenti con i rispettivi indirizzi email e lo stato corrente nell'account attualmente selezionato.
2. Fai clic su **Invita utenti**.
3. Specifica l'indirizzo e-mail o l'ID IBM dell'utente. Se stai fornendo a più utenti lo stesso accesso, immetti più indirizzi email o id IBM separando le voci di ID utente con virgole, spazi o interruzioni di riga.
4. Aggiungi una o più delle opzioni di accesso che gestisci. Devi assegnare almeno un'opzione di accesso e configurare le impostazioni per l'utente in ogni opzione di accesso che assegni. Per tutte le ulteriori opzioni di accesso che non aggiungi e configuri, viene assegnato il valore predefinito *nessun accesso*. Potresti visualizzare una o tutte le seguenti opzioni di accesso, a seconda delle opzioni che sei autorizzato a gestire: **Servizi abilitati per l'accesso e l'identità**, **Accesso Cloud Foundry**, **Accesso infrastruttura**. Per ulteriori informazioni, vedi [Assegnazione dell'accesso utente](/docs/iam/iamuserinv.html#assignaccess).

Se determini che un utente non ha bisogno dell'accesso, puoi annullare un invito per tutti gli utenti visualizzati in uno stato **Elaborazione** o **In sospeso** nella colonna **Stato**. Se un utente invitato non riceve un invito, puoi reinviare l'invito a tutti gli utenti nello stato **In sospeso**.

Se vuoi invitare gli utenti utilizzando la CLI, vedi il comando [bluemix iam account-user-invite](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_iam_account_user_invite).

## Assegnazione dell'accesso utente
{: #assignaccess}

Assegni l'accesso per gli utenti nel momento in cui li inviti, assegnando autorizzazioni all'infrastruttura, politiche e ruoli Cloud Foundry. A seconda delle opzioni di accesso che sei autorizzato a gestire, puoi invitare e fornire l'accesso agli utenti tra le istanze di servizio, spazio, organizzazione e account. Le seguenti sezioni descrivono i tre tipi di accesso che possono essere assegnati a un utente invitato.

### Servizi abilitati per l'accesso e l'identità

Quando inviti un nuovo utente, puoi assegnare una singola politica di servizio. Una volta che l'utente ha accettato l'invito, puoi aggiungere ulteriori politiche. Consulta [Politiche di accesso a servizi abilitati all'accesso e identità](/docs/iam/iamusermanage.html#iammanidaccser) per i dettagli sulla modifica delle politiche per aggiungere ulteriori ruoli, aggiungere ulteriori politiche di servizio o rimuovere una politica per un utente.

**Nota**: a seconda del servizio che selezioni quando assegni la politica, potresti non vedere tutti i campi descritti nella seguente procedura.

1. Dalla schermata **Invita utenti**, espandi la sezione **Servizi abilitati per l'accesso e l'identità**.
2. Seleziona un servizio.
3. Seleziona **Tutte le regioni correnti** su una specifica regione, se ti viene richiesto. 
**Nota**: non tutti i servizi richiedono la selezione di una regione.
4. Seleziona **Tutte le istanze del servizio correnti** o una specifica istanza del servizio.
5. A seconda del servizio che hai selezionato, potresti visualizzare i seguente campi. Se non immetti valori per questi campi, la politica viene assegnata a livello dell'istanza del servizio anziché a livello del bucket. 
    * **Tipo di risorsa**: immetti **bucket**.
    * **Risorsa**: immetti il nome del tuo bucket.
6. Seleziona un ruolo per definire l'ambito di accesso per la politica.
7. Facoltativo: seleziona **Aggiungi ruolo** per specificare un ruolo aggiuntivo per la politica.


Consulta [Politiche e ruoli per la gestione di identità e accesso](/docs/iam/users_roles.html#iamusermanpol) per informazioni più specifiche sui ruoli quando si impostano le politiche di servizio.

### Accesso Cloud Foundry

Quando inviti un nuovo utente, puoi scegliere di aggiungerlo a un'organizzazione nell'account. Se aggiungi l'utente a un'organizzazione, puoi assegnare all'utente un ruolo dell'organizzazione. Quindi, scegli di dare all'utente invitato l'accesso a qualsiasi spazio (o anche a tutti) nell'organizzazione selezionata con un ruolo dello spazio assegnato.

1. Dalla schermata **Invita utenti**, espandi la sezione **Accesso Cloud Foundry**.
2. Seleziona un'organizzazione a cui aggiungere l'utente.
3. Seleziona un ruolo organizzazione per definire il livello di accesso all'organizzazione selezionata.
4. Facoltativo: seleziona **Aggiungi ruolo** per specificare un ruolo aggiuntivo.
5. Seleziona **Tutte le regioni correnti** o una regione specifica.
6. Seleziona **Tutti gli spazi correnti** o uno specifico spazio.
7. Seleziona un ruolo spazio per definire il livello di accesso agli spazi selezionati.
8. Facoltativo: seleziona **Aggiungi ruolo** per specificare un ruolo aggiuntivo.

Consulta [Ruoli Cloud Foundry](/docs/iam/users_roles.html#cfroles) per informazioni più specifiche su questi ruoli.

**Nota**: puoi aggiungere un ruolo Cloud Foundry utilizzando il comando CLI[bluemix iam account-user-invite](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_iam_account_user_invite) ma per assegnare altro accesso o altre autorizzazioni è necessario utilizzare l'interfaccia utente.

### Accesso infrastruttura

Le autorizzazioni effettive assegnate vengono automaticamente limitate al sottoinsieme delle autorizzazioni di cui disponi. Per ulteriori informazioni sulle autorizzazioni e sulle azioni che l'utente può eseguire con ognuna di esse, vedi [Autorizzazioni dell'infrastruttura](/docs/iam/users_roles.html#infrapermissions).

1. Dalla schermata **Invita utenti**, espandi la sezione **Accesso infrastruttura**.
2. Seleziona un'autorizzazione per definire l'ambito di accesso.

Per informazioni sulla configurazione dell'accesso per gli utenti dopo che sono stati aggiunti al tuo account, vedi [Gestione di utenti e accesso](/docs/iam/iamusermanage.html).
