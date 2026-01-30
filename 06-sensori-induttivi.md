# Sensori Induttivi

## Documento Completo
Consulta il documento originale scorrendo la finestra qui sotto oppure scaricalo.

<div style="text-align: center; margin-bottom: 30px;">
    <embed src="./Sensori_Induttivi_Tecnologia_e_Applicazioni.pdf" type="application/pdf" width="100%" height="600px" />
    <br>
    <a href="./Sensori_Induttivi_Tecnologia_e_Applicazioni.pdf" target="_blank" style="display: inline-block; margin-top: 15px; background-color: #007bff; color: white; padding: 10px 20px; text-decoration: none; border-radius: 5px; font-weight: bold;">
        📥 Scarica / Apri PDF a schermo intero
    </a>
</div>

---

## Lezione Testuale Illustrata

### 1. Introduzione
I sensori induttivi sono dispositivi elettronici di prossimità progettati esclusivamente per il rilevamento di oggetti metallici senza nessun contatto fisico. Sono essenziali per determinare posizione, movimento e conteggio in ambienti industriali.

### 2. Principio di Funzionamento
Il funzionamento si basa sul principio fisico delle **Correnti di Foucault** (Eddy Currents).

![Schema Principio di Funzionamento](./img/principio-induttivo.png)
*Fig. 1: Generazione del campo elettromagnetico e induzione sul metallo.*

Il ciclo avviene in fasi:
1.  **Generazione:** Un oscillatore (circuito LC) alimenta la bobina creando un campo magnetico alternato che fuoriesce dalla "faccia attiva".
2.  **Smorzamento:** Quando il metallo entra nel campo, si generano correnti parassite che sottraggono energia al sistema.
3.  **Rilevamento:** Il circuito rileva il calo di ampiezza dell'oscillazione e commuta l'uscita (ON/OFF).

### 3. Struttura Interna
Il sensore non è solo una bobina, ma un sistema complesso.

![Diagramma a Blocchi Sensore](./img/struttura-interna.png)
*Fig. 2: Schema a blocchi: Oscillatore, Demodulatore, Trigger di Schmitt e Stadio di Uscita.*

### 4. Classificazione Meccanica: Flush vs Non-Flush
Una distinzione critica per l'installazione è il tipo di schermatura.

![Montaggio Flush vs Non Flush](./img/montaggio-flush.png)
*Fig. 3: A sinistra sensore Schermato (annegabile nel metallo), a destra Non Schermato (richiede area libera).*

* **Schermati (Flush):** Il campo è direzionato solo frontalmente. Possono essere montati "a filo" nel metallo. Distanza di rilevamento minore, ma meccanicamente protetti.
* **Non Schermati (Non-flush):** Il campo esce anche lateralmente. Richiedono una "zona libera" (clearance) attorno alla testina, ma offrono una distanza di rilevamento maggiore.

### 5. Il Problema dei Materiali (Fattore di Riduzione)
Non tutti i metalli vengono "visti" allo stesso modo. L'acciaio è il riferimento (100%).

![Grafico Fattori di Riduzione](./img/fattore-riduzione.png)
*Fig. 4: Riduzione della distanza di lettura per Alluminio e Rame rispetto all'Acciaio.*

Per risolvere questo problema esistono i sensori **Fattore 1**, che utilizzano bobine speciali (senza nucleo in ferrite) per leggere tutti i metalli alla stessa distanza massima.

### 6. Applicazioni Tipiche
Dall'automazione generica al settore automotive.

![Esempi Applicativi](./img/applicazioni.png)
*Fig. 5: Controllo rotazione ingranaggi e posizionamento su nastri trasportatori.*

* **Rilevamento Ingranaggi:** Per contare i giri o misurare la velocità.
* **Controllo Presenza:** Verifica se un pezzo è presente sul nastro.
* **Automotive (ABS):** I sensori induttivi leggono le ruote foniche per i sistemi di sicurezza attiva.

---
[🔙 Torna all'Indice](./index.html)
