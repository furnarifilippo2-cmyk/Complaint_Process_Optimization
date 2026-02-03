# 📈 Ottimizzazione Processo Reclami & Analisi Performance

## 📋 Panoramica del Progetto
Questo progetto dimostra l'integrazione tra la **modellazione dei processi aziendali (BPMN)** e la **Business Intelligence (Power BI)**. L'obiettivo è trasformare un flusso operativo teorico in un sistema monitorabile basato sui dati per ridurre i tempi di risposta ai clienti.

---

## 🏗️ 1. Modellazione del Processo (BPMN 2.0)
Ho progettato il flusso di gestione reclami utilizzando lo standard **BPMN 2.0**. 

### Punti Chiave del Modello:
* **Gestione SLA:** Inserimento di un *Boundary Timer Event* sull'attività di Analisi Tecnica per far scattare un sollecito automatico dopo 48 ore.
* **Logica Decisionale:** Utilizzo di Gateway Esclusivi per automatizzare lo smistamento tra rimborsi, rifiuti e richieste di integrazione dati.
* **Data Integration:** Identificazione dei punti di scrittura nel database (es. Tabella_Rimborsi_DB).

<img width="3469" height="1719" alt="Workflow" src="https://github.com/user-attachments/assets/e7eeace6-aaa2-4934-94b4-592d7a8dc128" />


---


## 🗄️ 2. Struttura Dati 
Per testare il modello, ho generato un dataset di **100 righe** relativo al mese di Gennaio 2026. I dati simulano:
* **Identificativi Reclamo:** ID univoci per il tracciamento.
* **Indicatori di Allarme:** Una colonna binaria `Alert_SLA` (0/1) che registra quando il Timer del processo BPMN è scattato.
* **Metriche Finanziarie:** Valori dei rimborsi emessi dalla corsia Amministrazione.

---

## 📊 3. Dashboard di Monitoraggio (Power BI)
La dashboard trasforma i dati del processo in insight azionabili e dinamici.



### Metriche Principali:
* **Conteggio Sollecitazioni:** `SUM('ID_Reclamo'[ALert_SLA])` - Conta quante volte il processo è andato fuori tempo massimo.
* **Analisi Temporale:** Visualizzazione dell'andamento giornaliero per Gennaio 2026, identificando i colli di bottiglia settimanali.

### Risultati Analisi:
Dall'analisi di Gennaio è emerso che il **20% dei reclami** ha attivato il sollecito automatico, con una concentrazione maggiore nella seconda settimana del mese.

---

## 🛠️ Tool Utilizzati
* **BPMN.io:** Per la modellazione grafica del processo.
* **Excel:** Per la generazione e strutturazione del dataset.
* **Power BI:** Per la data visualization e il calcolo delle metriche.
