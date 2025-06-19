#  Analisi del Sentiment sul Bitcoin tramite Tweet

**MarketPulse Analytics**, una società leader nel settore delle ricerche di mercato, ha avviato un progetto per stimare il consenso pubblico verso il **Bitcoin** analizzando milioni di tweet. La tua responsabilità, come **Data Scientist**, è di eseguire un'analisi del sentiment sui dati raccolti e comprendere come le opinioni riguardanti il Bitcoin variano nel tempo. In aggiunta, dovrai rispondere a domande cruciali sull'engagement degli utenti sui social media e valutare eventuali correlazioni con il prezzo del Bitcoin.

Il primo passo è analizzare il **sentiment** dei tweet utilizzando un modello di **sentiment analysis**. Per ciascun tweet estratto, sarà classificato come **positivo**, **negativo** o **neutro**, basandoti su parole chiave, tono e linguaggio utilizzato. Questa classificazione consentirà di misurare il consenso verso il Bitcoin su base giornaliera.

Successivamente, verrà creato un **grafico temporale** che mostri la variazione del sentiment giorno per giorno:
- **Tweet positivi**: Il numero di tweet con sentiment positivo su base giornaliera.
- **Tweet negativi**: Il numero di tweet con sentiment negativo su base giornaliera.
- **Tweet neutrali**: Andamento dei tweet che non presentano un chiaro giudizio di valore.

Il grafico mostrerà l'evoluzione del sentimento pubblico verso il Bitcoin, evidenziando i momenti di picco o declino.

Dopo l'analisi del sentiment, è interessante valutare l'engagement generato dai tweet. In particolare, risponderai a queste due domande:
- **I tweet negativi ricevono più likes rispetto ai tweet positivi?** Verranno calcolate e confrontate le medie di like per i tweet negativi e positivi, analizzando se i tweet con un tono negativo attirano maggiore attenzione o interesse.
- **I tweet negativi ricevono più interazioni (risposte) rispetto ai tweet positivi?** Sarà condotta un'analisi simile confrontando il numero medio di risposte tra tweet positivi e negativi, per vedere quale tipo di sentiment provoca una discussione più accesa.

Per aggiungere ulteriore profondità all'analisi, esplorerai la relazione tra la **variazione del sentiment** e la **variazione del valore del Bitcoin**. A tal fine:
- Reperirai lo **storico del prezzo del Bitcoin (BTC/USD)** da fonti affidabili (es. Yahoo Finance).
- Confronterai le variazioni del sentiment giornaliero con le variazioni del prezzo del Bitcoin, cercando di individuare correlazioni significative.

Questo approccio ti permetterà di rispondere alla domanda: **Il sentiment pubblico verso il Bitcoin ha un'influenza sul prezzo della criptovaluta?** O viceversa, **i cambiamenti di prezzo influenzano il sentiment sui social media?**

### Valore Aggiunto

Attraverso questo progetto, MarketPulse Analytics otterrà insight di grande valore:
- **Comprensione del sentiment** verso il Bitcoin in tempo reale, utile per investitori e professionisti del settore finanziario.
- **Individuazione delle tendenze sociali** legate alla criptovaluta, potenzialmente in grado di anticipare movimenti del mercato.
- **Analisi del comportamento dell’engagement**: Capire se i tweet negativi attirano maggiore attenzione o generano più interazioni rispetto a quelli positivi, utile per le strategie di marketing.
- **Correlazione tra sentiment e prezzo del Bitcoin**: Fornire indicazioni su come i sentimenti pubblici possano influenzare o essere influenzati dal valore di mercato del Bitcoin, offrendo nuove prospettive strategiche per i clienti di MarketPulse Analytics.

Questa analisi fornirà uno strumento utile per decisioni aziendali data-driven, offrendo un vantaggio competitivo nel mercato delle criptovalute.


### [Link al dataset](https://proai-datasets.s3.eu-west-3.amazonaws.com/bitcoin_tweets.csv)

### VINCOLI
Per questo progetto dovrai sfruttare PySpark e i suoi vari strumenti, puoi lavorare con PySpark in cloud gratuitamente utilizzando [DataBricks Community](https://community.cloud.databricks.com/login.html)

Per poter caricare il dataframe e trasformarlo in una table basta eseguire 

---

su Notebook Databricks le seguenti righe di codice:

```python
!wget https://proai-datasets.s3.eu-west-3.amazonaws.com/bitcoin_tweets.csv

import pandas as pd
dataset = pd.read_csv('/databricks/driver/bitcoin_tweets.csv', delimiter=";")

spark_df = spark.createDataFrame(dataset)
spark_df.write.saveAsTable("bitcoin_tweets")
```
