---

copyright:

  years: 2015, 2017
lastupdated: "2017-07-26"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Assegnazione dell'accesso utente
{: #assignaccess}

Assegni l'accesso per gli utenti nel momento in cui li inviti, assegnando autorizzazioni all'infrastruttura, politiche e ruoli Cloud Foundry. A seconda delle opzioni di accesso che sei autorizzato a gestire, puoi invitare e fornire l'accesso agli utenti tra le istanze di servizio, spazio, organizzazione e account. Le seguenti sezioni descrivono i tre tipi di accesso che possono essere assegnati a un utente invitato.
{:shortdesc}

## Servizi abilitati per l'accesso e l'identità

Quando inviti un nuovo utente, puoi assegnare una singola politica di servizio. Una volta che l'utente ha accettato l'invito, puoi aggiungere ulteriori politiche.

1. Dalla schermata **Invita utenti**, espandi la sezione **Servizi abilitati per l'accesso e l'identità**.
2. Seleziona un servizio.
3. Seleziona **Tutte le regioni correnti** o una regione specifica.
4. Seleziona **Tutte le istanze del servizio correnti** o una specifica istanza del servizio.
5. Seleziona un ruolo per definire l'ambito di accesso per la politica.
6. Facoltativo: seleziona **Aggiungi ruolo** per specificare un ruolo aggiuntivo per la politica.

Consulta [Politiche e ruoli per la gestione di identità e accesso](/docs/iam/users_roles.html#iamusermanpol) per informazioni più specifiche sui ruoli quando si impostano le politiche di servizio.

## Accesso Cloud Foundry

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

## Accesso infrastruttura

Le autorizzazioni effettive assegnate vengono automaticamente limitate al sottoinsieme delle autorizzazioni di cui disponi. Per ulteriori informazioni sulle autorizzazioni e sulle azioni che l'utente può eseguire con ognuna di esse, vedi [Autorizzazioni dell'infrastruttura](/docs/iam/users_roles.html#infrapermissions).

1. Dalla schermata **Invita utenti**, espandi la sezione **Accesso infrastruttura**.
2. Seleziona un'autorizzazione per definire l'ambito di accesso.

Per informazioni sulla configurazione dell'accesso per gli utenti dopo che sono stati aggiunti al tuo account, vedi [Gestione di utenti e accesso](/docs/iam/iamusermanage.html).
