---

copyright:

  years: 2015, 2017

lastupdated: "2017-10-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Gestione di utenti e politiche di accesso
{: #iamusermanage}

A seconda delle opzioni di accesso che sei autorizzato a gestire, puoi visualizzare e gestire gli utenti nell'account o nell'organizzazione. Come proprietario di un account, puoi gestire gli utenti in tutte le opzioni di accesso che gestisci e alle quali è assegnato l'accesso dell'utente nell'account corrente.
{:shortdesc}

## Gestione degli utenti

Per gestire gli utenti nel tuo account, completa la seguente procedura:

1. Dalla barra dei menu, fai clic su **Gestisci ** &gt; **Account** &gt; **Utenti**. La finestra Utenti visualizza un elenco di utenti con i rispettivi indirizzi email per l'account attualmente selezionato.
2. Seleziona il nome utente o fai clic su **Gestisci utente** dal menu **Azioni**.
3. Quindi, a seconda dell'azione che devi eseguire, puoi scegliere di rimuovere l'utente, assegnare una nuova politica o gestire l'accesso esistente dell'utente.

Consulta le seguenti sezioni per ulteriori informazioni sulla gestione di ciascun tipo di accesso.

Se devi controllare il tuo accesso assegnato in un account a cui sei stato aggiunto, completa la seguente procedura:

1. Dalla barra dei menu, fai clic su **Gestisci** &gt; **Sicurezza** &gt; **Identità e accesso** &gt; **Utenti**.
2. Seleziona il tuo nome.
3. Controlla i tuoi ruoli assegnati.

Se hai bisogno di privilegi aggiuntivi, devi contattare il gestore dell'organizzazione o il proprietario dell'account per aggiornare il ruolo Cloud Foundry oppure devi contattare l'amministratore per il servizio o l'istanza del servizio per aggiornare la politica di servizio.

Per informazioni dettagliate sui comandi CLI utilizzati per gestire account, organizzazioni e spazi, vedi [Comandi per gestire account, organizzazioni e ruoli](/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_acctorg).

## Accesso Cloud Foundry
{: #iammancfser}

Per gestire l'accesso alle organizzazioni e agli spazi dell'account, devi essere il proprietario dell'account, il gestore organizzazione o il gestore spazio:

1. Dalla barra dei menu, fai clic su **Gestisci** &gt; **Sicurezza** &gt; **Identità e accesso** &gt; **Utenti**.
2. Seleziona il nome utente per il quale vuoi modificare i ruoli.
3. Dal menu **Azioni** nella sezione Cloud Foundry, puoi:

  * Rimuovere l'utente dall'organizzazione
  * Modificare il ruolo organizzazione
  * Modificare il ruolo spazio

Se sei il gestore di un'organizzazione di cui l'utente non è ancora membro, puoi anche aggiungere un utente a un'altra organizzazione facendo clic su **Assegna organizzazione**.


## Politiche di accesso a servizi abilitati all'accesso e identità
{: #iammanidaccser}

Per gestire le politiche di servizio o assegnare nuove politiche di servizio per gli utenti, devi essere l'amministratore di accesso account o l'amministratore assegnato per il servizio o l'istanza del servizio particolare. Per ulteriori informazioni sulle politiche di servizio e sui ruoli, vedi [Politiche e ruoli per la gestione di identità e accesso](/docs/iam/users_roles.html#iamusermanpol). Per i dettagli sui comandi CLI utilizzati per gestire le politiche, consulta [Comandi per la gestione di politiche e chiavi API](/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_iam).

### Modifica una politica esistente

1. Dalla barra dei menu, fai clic su **Gestisci** &gt; **Sicurezza** &gt; **Identità e accesso** &gt; **Utenti**.
2. Seleziona il nome utente per il quale vuoi assegnare le politiche di servizio.
3. Dalla riga per la politica che vuoi modificare, seleziona il menu **Azioni** e fai quindi clic su **Modifica politica**.
4. Modifica la politica.
5. Fai clic su **Salva politica**.

### Aggiunta di una nuova politica

1. Dalla barra dei menu, fai clic su **Gestisci** &gt; **Sicurezza** &gt; **Identità e accesso** &gt; **Utenti**.
2. Seleziona il nome utente per il quale vuoi assegnare le politiche di servizio.
3. Seleziona **Assegna politiche**.
4. Seleziona un servizio.
5. Seleziona **Tutte le regioni correnti** su una specifica regione, se ti viene richiesto. 
**Nota**: non tutti i servizi richiedono la selezione di una regione.
6. Seleziona **Tutte le istanze del servizio correnti** o una specifica istanza del servizio.
7. A seconda del servizio che hai selezionato, potresti visualizzare i seguente campi. Se non immetti valori per questi campi, la politica viene assegnata a livello dell'istanza del servizio anziché a livello del bucket. 
    * **Tipo di risorsa**: immetti **bucket**.
    * **Risorsa**: immetti il nome del tuo bucket.
8. Seleziona un ruolo per definire l'ambito di accesso per la politica.
9. Facoltativo: seleziona **Aggiungi ruolo** per specificare un ruolo aggiuntivo per la politica.

### Rimozione di una politica

1. Dalla barra dei menu, fai clic su **Gestisci** &gt; **Sicurezza** &gt; **Identità e accesso** &gt; **Utenti**.
2. Seleziona il nome utente per il quale vuoi assegnare le politiche di servizio.
3. Dalla riga per la politica che vuoi rimuovere, seleziona il menu **Azioni** e fai quindi clic su **Rimuovi politica**.
4. Esamina i dettagli della politica utente che stai per rimuovere e conferma quindi facendo clic su **Rimuovi politica**.
  

## Autorizzazione dei servizi infrastruttura

Per assegnare o aggiornare autorizzazioni dell'infrastruttura, fai clic sul link **Assegna accesso infrastruttura**.

