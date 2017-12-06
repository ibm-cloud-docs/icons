---

copyright:

  years: 2015, 2017
lastupdated: "2017-08-01"

---

{:new_window: target="_blank"}  
{:shortdesc: .shortdesc}


# Aggiunta di una nuova credenziale del servizio
{: #service_credentials}

Puoi generare una nuova serie di credenziali del servizio per i casi in cui vuoi collegare manualmente un cliente esterno a un servizio Bluemix. Ad esempio, se stai tentando di associare un'applicazione AWS a un servizio Watson, dovrai generare una nuova credenziale del servizio che può essere utilizzata per associare questi due servizi tra loro.

I servizi Cloud Foundry possono generare una chiave del servizio, conosciuta anche come una credenziale del servizio. Le credenziali del servizio sono specifiche per il servizio e variano in base a come ogni servizio definisce le credenziali che deve generare. Una credenziale del servizio può contenere un nome utente, una password, un nome host, una porta e un URL. Tuttavia, i contenuti di ogni credenziale del servizio sono univoci per il servizio che la genera. Alcuni servizi possono generare ulteriori dati che richiedono la trasmissione di parametri. Ad esempio, un servizio potrebbe richiederti di immettere una parametro lingua per impostare la lingua predefinita restituita nella chiave del servizio generata. 

Completa la seguente procedura per aggiungere una nuova credenziale del servizio:

1. Dalla pagina dei dettagli del servizio, seleziona la scheda delle credenziali del servizio e fai clic su **Nuova credenziale + **.
2. Dalla finestra di dialogo dell'aggiunta della nuova credenziale, fornisci un **Nome**.
3. Facoltativamente, puoi fornire ulteriori parametri come un oggetto JSON valido che contiene i parametri di configurazione specifici per il servizio, forniti sia incorporati che in un file.

  **Nota**. Molti servizi non richiedono ulteriori parametri e per i servizi che li richiedono, ognuno di essi definisce il proprio elenco di parametri univoco. Per un elenco di parametri di configurazione supportati, consulta la documentazione per l'offerta del servizio in particolare.
4. Fai clic su **Aggiungi** per generare la nuova credenziale del servizio.
