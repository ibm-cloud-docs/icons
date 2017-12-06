---



copyright:

  years: 2015, 2017
lastupdated: "2017-05-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Collegamento dei tuoi account Bluemix e SoftLayer
{: #unifyingaccounts}

Puoi collegare i tuoi account {{site.data.keyword.Bluemix_notm}} e SoftLayer per utilizzare risorse combinate. Quando colleghi gli account {{site.data.keyword.Bluemix_notm}} e Softlayer, riceverai un'unica fattura {{site.data.keyword.Bluemix_notm}}. Se hai un account {{site.data.keyword.Bluemix_notm}} esistente, la fatturazione tramite {{site.data.keyword.Bluemix_notm}} per le risorse SoftLayer parte dal nuovo ciclo di fatturazione che inizia dopo il collegamento degli account.

**Importante:** tutti gli account collegati in {{site.data.keyword.Bluemix_notm}} devono essere del tipo Pagamento a consumo. Puoi creare un nuovo account Pagamento a consumo, collegare un account Pagamento a consumo esistente o collegare un account di prova esistente (che verrà poi aggiornato a un account Pagamento a consumo). Non puoi collegare gli account {{site.data.keyword.Bluemix_notm}} di sottoscrizione.

Per collegare gli account, devi essere un utente master dell'account SoftLayer.

Quando i tuoi account vengono collegati:

* Devi utilizzare le credenziali dell'ID IBM per accedere a entrambi gli account SoftLayer e {{site.data.keyword.Bluemix_notm}}.
* Eventuali sconti SoftLayer esistenti vengono applicati agli addebiti {{site.data.keyword.Bluemix_notm}}.
* Riceverai un'unica fattura in dollari americani (USD).
* Puoi monitorare l'utilizzo delle tue risorse {{site.data.keyword.BluSoftlayer}} nella console {{site.data.keyword.Bluemix_notm}}.

**Attenzione:** una volta collegati, gli account non possono più essere scollegati.  

Come utente master, completa la seguente procedura per collegare i tuoi account {{site.data.keyword.Bluemix_notm}} e SoftLayer:

 1. Dal {{site.data.keyword.slportal}}, fai clic su **Collega un account {{site.data.keyword.Bluemix_notm}}**.
 2. Leggi e accetta le condizioni di collegamento degli account SoftLayer e {{site.data.keyword.Bluemix_notm}}.
 3. Quando richiesto, fornisci l'indirizzo e-mail associato al tuo account {{site.data.keyword.Bluemix_notm}}. Se non hai un account {{site.data.keyword.Bluemix_notm}}, fornisci l'indirizzo e-mail che desideri utilizzare, quindi segui le istruzioni per ricevere l'invito a {{site.data.keyword.Bluemix_notm}} e crea un account.

Dopo aver collegato i tuoi account, l'opzione **Vai a {{site.data.keyword.Bluemix_notm}}** sarà disponibile nella barra dei menu della console SoftLayer. Facendo clic su questo link, arrivi alla pagina di accesso {{site.data.keyword.Bluemix_notm}}.

## Fatturazione per l'utilizzo di {{site.data.keyword.Bluemix_notm}} con gli account collegati
{: #bill_usage}

Una volta collegati i tuoi account di fatturazione {{site.data.keyword.Bluemix_notm}} e SoftLayer, il successivo ciclo di fatturazione verrà addebitato in un'unica fattura {{site.data.keyword.Bluemix_notm}}.
{:shortdesc}

Il tuo ciclo di utilizzo di {{site.data.keyword.Bluemix_notm}} si basa sul mese di calendario, perciò l'addebito per il tuo account viene effettuato con cadenza mensile il giorno di fatturazione stabilito nel tuo accordo di addebito. Con SoftLayer, il ciclo di utilizzo inizia nel momento in cui viene avviato e viene pertanto addebitato con cadenza mensile lo stesso giorno del mese in cui hai sottoscritto l'account SoftLayer. 

Quando gli account sono collegati, l'utilizzo di {{site.data.keyword.Bluemix_notm}} continua a essere misurato per il ciclo del mese corrente e viene fatturato con una fattura {{site.data.keyword.Bluemix_notm}}. Dal primo giorno del mese successivo, gli addebiti {{site.data.keyword.Bluemix_notm}} e SoftLayer verranno combinati nella tua fattura {{site.data.keyword.Bluemix_notm}}.

Ad esempio, se hai collegato gli account il 16 aprile 2017, riceverai una fattura Bluemix per l'utilizzo nel mese di aprile. A seconda di quando hai collegato i tuoi account, potresti ricevere una fattura separata per l'utilizzo di SoftLayer. Il tuo utilizzo nel mese di maggio per SoftLayer e {{site.data.keyword.Bluemix_notm}} verrà fatturato tramite il tuo account {{site.data.keyword.Bluemix_notm}}.

![Riepilogo del collegamento degli account Bluemix e SoftLayer](BluemixSoftLayerBill.svg)

Una volta collegate le fatture, la tua fattura {{site.data.keyword.Bluemix_notm}} elencherà i diversi addebiti per ogni risorsa che hai utilizzato.

## Servizi Bluemix basati su API
{: #api_based_bluemix_services}

Il seguente elenco contiene i servizi che puoi configurare per l'esecuzione con il tuo codice applicativo.
{:shortdesc}

Non tutti i piani per questi servizi sono disponibili per l'utilizzo con gli account {{site.data.keyword.Bluemix_notm}} e SoftLayer collegati. Solo i piani abilitati per gli account Pagamento a consumo possono essere utilizzati con gli account collegati. Tuttavia, se hai un account {{site.data.keyword.Bluemix_notm}} che viene fatturato separatamente, puoi utilizzare qualsiasi piano per tutti questi servizi.

* {{site.data.keyword.alchemyapishort}}
* {{site.data.keyword.alertnotificationshort}}
* {{site.data.keyword.sparks}}
* {{site.data.keyword.appseccloudshort}}
* {{site.data.keyword.blockchain}}
* {{site.data.keyword.cloudant}}
* {{site.data.keyword.conceptinsightsshort}}
* {{site.data.keyword.iotmapinsights_short}}
* {{site.data.keyword.dashdbshort}}
* {{site.data.keyword.dialogshort}}
* {{site.data.keyword.documentconversionshort}}
* {{site.data.keyword.twittershort}}
* {{site.data.keyword.weather_short}}
* {{site.data.keyword.iotdriverinsights_short}}
* {{site.data.keyword.geospatialshort_Geospatial}}
* {{site.data.keyword.graphshort}}
* {{site.data.keyword.iotelectronics}}
* {{site.data.keyword.languagetranslationshort}}
* {{site.data.keyword.messagehub}}
* {{site.data.keyword.mqa}}
* {{site.data.keyword.mobileappbuilder_short}}
* {{site.data.keyword.mql}}
* {{site.data.keyword.nlclassifiershort}}
* {{site.data.keyword.objectstorageshort}}
* {{site.data.keyword.personalityinsightsshort}}
* {{site.data.keyword.presenceinsightsshort}}
* {{site.data.keyword.relationshipextractionshort}}
* {{site.data.keyword.retrieveandrankshort}}
* {{site.data.keyword.servicediscoveryshort}}
* {{site.data.keyword.speechtotextshort}}
* {{site.data.keyword.sqldb}}
* {{site.data.keyword.streaminganalyticsshort}}
* {{site.data.keyword.texttospeechshort}}
* {{site.data.keyword.toneanalyzershort}}
* {{site.data.keyword.tradeoffanalyticsshort}}
* {{site.data.keyword.visualinsightsshort}}
* {{site.data.keyword.visualrecognitionshort}}
* {{site.data.keyword.workflow}}
* {{site.data.keyword.workloadscheduler}}
