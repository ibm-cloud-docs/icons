---

copyright:
  years: 2015, 2017

lastupdated: "2017-07-31"

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:screen: .screen}
{:pre: .pre}

# Panoramica
{: #monitoringandlogging}

{{site.data.keyword.Bluemix}} offre funzionalità integrate di registrazione e di monitoraggio attraverso diversi servizi, come Cloud Foundry e {{site.data.keyword.containershort}}. Puoi anche utilizzare il servizio {{site.data.keyword.loganalysisfull}} e {{site.data.keyword.monitoringlong}} per le funzionalità di monitoraggio e registrazione estesa.
{:shortdesc}

## Registrazione in Bluemix
{: #logging}

Per impostazione predefinita, {{site.data.keyword.Bluemix_notm}} raccoglie e visualizza i log per le tue applicazioni, i runtime delle applicazioni e i runtime di calcolo in cui queste applicazioni vengono eseguite. Le funzionalità di registrazione {{site.data.keyword.Bluemix_notm}} sono integrate nella piattaforma e la raccolta dei dati è abilitata automaticamente per le risorse cloud. 

Il servizio {{site.data.keyword.loganalysisfull}} fornisce i servizi di raccolta e ricerca dei log per la piattaforma {{site.data.keyword.Bluemix_notm}}, raccogliendo in automatico l'applicazione e i dati dei servizi {{site.data.keyword.Bluemix_notm}} dai servizi {{site.data.keyword.Bluemix_notm}} selezionati. Utilizza il servizio {{site.data.keyword.loganalysisshort}} per espandere le tue funzionalità di raccolta, conservazione e ricerca dei log quando utilizzi i log:

* Impieghi meno tempo a strumentare la tua applicazione e più tempo a migliorarne la qualità

    {{site.data.keyword.loganalysislong_notm}} raccoglie automaticamente i dati dai servizi cloud {{site.data.keyword.IBM_notm}} selezionati, nessuna instrumentazione necessaria.
	
* Conservi i tuoi dati di log vicino ai tuoi carichi di lavoro dell'applicazione e proteggi le soluzioni di archiviazione economiche della classe cloud

    Raccogli e archivi i dati di log dalle applicazioni guidate del microservizio e tradizionale in esecuzione nel  cloud {{site.data.keyword.IBM_notm}} in un log centralizzato. Conservi i dati di log per tutto il tempo necessario.
	
	I log vengono archiviati nell'archivio cloud {{site.data.keyword.IBM_notm}}. Puoi scaricare i log quando ne hai bisogno.

* Ottieni informazioni approfondite sul tuo ambiente per individuare, diagnosticare e identificare velocemente i problemi

    Visualizzi, analizzi e interagisci con i tuoi dati tramite dashboard personalizzabili. Basate sulla piattaforma stack Elastic, le funzioni di ricerca dei log ti offrono la flessibilità e la familiarità di Kibana per creare velocemente i tuoi dashboard per i bisogni della tua applicazione.

* Integrazione solida con le API

    Integra i tuoi dati di log nelle tue applicazioni e operazioni tramite le API del servizio. Utilizza l'API del servizio {{site.data.keyword.loganalysisshort}} per gestire i tuoi log conservati e per inviare i dati di log al di fuori del cloud {{site.data.keyword.IBM_notm}}.
	
* Scegli il piano del servizio che risponde ai tuoi bisogni.

     Puoi scegliere il piano del servizio Lite o Premium a seconda dei tuoi bisogni di utilizzo.
	 
	 Scegli la quantità di log che puoi ricercare al giorno. Sono disponibili diversi piani che puoi utilizzare per ricercare fino a 500MB,  2GB, 5GB e 10GB di log al giorno.
	 
	 **Nota:** le funzioni che ottieni tramite il piano Lite sono le stesse funzionalità di registrazione integrate offerte per impostazione predefinita in {{site.data.keyword.Bluemix_notm}}.

Aggiungi al tuo team DevOps funzioni come l'aggregazione dell'applicazione e dei log dell'ambiente per l'applicazione consolidata o le informazioni approfondite sull'ambiente, la codifica dei log, la conservazione dei dati di log per il tempo necessario e il rapido rilevamento e risoluzione dei problemi. 

Per ulteriori informazioni, vedi [Registrazione in Bluemix](/docs/services/CloudLogAnalysis/log_analysis_ov.html#log_analysis_ov).


## Monitoraggio in Bluemix
{: #monitoring}

{{site.data.keyword.Bluemix_notm}}, per impostazione predefinita, raccoglie e visualizza le metriche per l'utilizzo della CPU, l'utilizzo della memoria e l'I/O di rete per {{site.data.keyword.containershort}}. 

Puoi utilizzare il servizio {{site.data.keyword.monitoringlong}} in {{site.data.keyword.Bluemix_notm}} per raccogliere e misurare automaticamente le metriche chiave dal tuo ambiente e dalle tue applicazioni. Non è richiesta alcuna strumentazione speciale per raccogliere le metriche. Ad esempio, puoi utilizzare le informazioni fornite dalle metriche delle prestazioni per monitorare in che modo un servizio viene eseguito nel cloud, per individuare colli di bottiglia delle risorse e per controllare lo SLA (service level agreement). Quando analizzi i dati delle prestazioni di un servizio, puoi rilevare delle situazioni che possono causare un collo di bottiglia delle risorse e di conseguenza influire sullo SLA del servizio per i tuoi clienti. Adottando delle azioni tempestive, puoi prevenire situazioni che possono compromettere il tuo business. 

Utilizza il servizio {{site.data.keyword.monitoringlong}} per espandere le tue funzionalità di raccolta, conservazione e analisi in {{site.data.keyword.Bluemix_notm}} quando utilizzi le metriche:

* Avviso in azione! 

    {{site.data.keyword.monitoringlong}} offre una chiave API che puoi utilizzare per configurare le soglie delle prestazioni e per ricevere una notifica quando queste soglie vengono superate. Definisci le regole di avviso per una sola istanza del servizio o dell'applicazione e le regole di avviso riportate per una serie di istanze. Quando viene attivato un avviso, ricevi una notifica tramite email, un evento PagerDuty, una notifica webhook o una loro qualsiasi combinazione.

* Aggiungi metriche personalizzate. 

    Il piano Premium di {{site.data.keyword.monitoringlong}} offre API che puoi utilizzare per aggiungere l'applicazione pertinente e le metriche di business ai tuoi dati Cloud Monitoring. Puoi anche utilizzarle per inviare i dati della metrica al di fuori del cloud {{site.data.keyword.IBM_notm}} nel servizio {{site.data.keyword.monitoringlong}}.

* Crea dashboard riutilizzabili e rendili interattivi. 

    Grafana ospitato di {{site.data.keyword.monitoringlong}} offre supporto per la creazione di dashboard personalizzati con una grande offerta di opzioni di visualizzazione.  Rendi i tuoi dashboard dinamici con i modelli utilizzando le query delle metriche con le variabili.

* Accedi al tuo servizio tramite il catalogo {{site.data.keyword.Bluemix_notm}}. 

    {{site.data.keyword.monitoringlong}} è disponibile come tile del servizio nella sezione DevOps del catalogo {{site.data.keyword.Bluemix_notm}}.  Per il servizio {{site.data.keyword.containershort}} con contenitori singoli o a gruppi, puoi accedere al servizio dalla IU {{site.data.keyword.Bluemix_notm}}.

* Scegli il piano del servizio che risponde ai tuoi bisogni. 

    Puoi scegliere il piano del servizio Lite o Premium a seconda dei tuoi bisogni di utilizzo. Il piano Lite offre la raccolta delle metriche una volta al minuto, la conservazione per 15 giorni e avvisi complementari. In alternativa, puoi selezionare il piano Premium per abilitare un maggiore consumo, una conservazione delle metriche più lunga e per ottenere l'accesso alle API del servizio, ad esempio, per inviare o richiamare le metriche dal servizio {{site.data.keyword.monitoringlong}}. {{site.data.keyword.monitoringlong}} offre la raccolta delle metriche una volta al minuto.  Il piano Lite conserva le metriche alla piena risoluzione per 15 giorni. Il piano Premium conserva le metriche alla piena risoluzione per 45 giorni.

    **Nota:** le funzioni che ottieni tramite il piano Lite sono le stesse funzionalità di monitoraggio integrate offerte per impostazione predefinita in {{site.data.keyword.Bluemix_notm}}.

Per ulteriori informazioni, vedi [Monitoraggio in Bluemix](/docs/services/cloud-monitoring/monitoring_ov.html#monitoring_ov).

{{site.data.keyword.Bluemix_notm}} offre anche il monitoraggio dell'infrastruttura, disponibile per tutti i server, e dei report facilmente leggibili. Per ulteriori informazioni, vedi [Infrastructure Monitoring & Reporting ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/cloud-computing/bluemix/infrastructure-monitoring){: new_window}.
