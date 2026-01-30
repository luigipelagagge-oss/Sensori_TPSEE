# Sensori Induttivi

## Introduzione
[cite_start]I sensori induttivi sono dispositivi elettronici di prossimità progettati esclusivamente per il rilevamento di oggetti metallici senza nessun contatto fisico[cite: 143]. [cite_start]Vengono utilizzati per determinare la posizione, il movimento, misurare distanze o fungere da contatori e finecorsa affidabili[cite: 144, 145, 146, 147].

## Principio di Funzionamento
Il funzionamento si basa sul principio fisico delle **Correnti di Foucault**. [cite_start]Un oscillatore interno crea un campo elettromagnetico alternato ad alta frequenza che fuoriesce dalla superficie attiva del sensore[cite: 116, 157, 160, 176].

[cite_start]Il ciclo operativo avviene in quattro fasi[cite: 171]:
1.  **Generazione:** L'oscillatore genera il campo elettromagnetico.
2.  [cite_start]**Interazione:** Quando un oggetto metallico entra nel campo, l'energia induce correnti parassite (di Foucault) sulla superficie dell'oggetto[cite: 169].
3.  [cite_start]**Smorzamento:** Le correnti indotte sottraggono energia al campo, riducendone l'ampiezza[cite: 178].
4.  [cite_start]**Commutazione:** L'elettronica interna rileva questa variazione di ampiezza e attiva l'uscita[cite: 179].

## Struttura Interna
[cite_start]Un sensore induttivo è composto da tre stadi principali[cite: 181]:
* [cite_start]**Superficie Attiva:** Il punto di emissione del campo, contenente la bobina[cite: 182].
* [cite_start]**Elettronica di Analisi:** Comprende l'oscillatore e il rilevatore[cite: 184].
* [cite_start]**Stadio di Uscita:** L'interfaccia verso il PLC o il sistema di controllo[cite: 185].

## Classificazione Meccanica
I sensori si dividono in due categorie principali in base al montaggio:
* **Schermati (Flush):** Possono essere montati a filo nel metallo. [cite_start]Sono protetti meccanicamente e ideali per spazi ridotti[cite: 191, 193, 195].
* **Non Schermati (Non-flush):** La superficie attiva deve rimanere libera da metallo circostante. [cite_start]Richiedono più spazio ma offrono una distanza di commutazione maggiore[cite: 197, 201].

## Influenza dei Materiali
[cite_start]La distanza di rilevamento varia in base alla conducibilità del metallo[cite: 204].
* [cite_start]**Acciaio:** Fattore 1.0 (Riferimento)[cite: 210].
* [cite_start]**Alluminio e Rame:** Subiscono una riduzione significativa (Fattore 0.25 - 0.45)[cite: 208, 209].

[cite_start]Esistono sensori speciali detti **"Fattore 1"** che utilizzano doppie bobine in aria (senza nucleo in ferrite) per rilevare tutti i metalli (acciaio, alluminio, rame) alla stessa distanza[cite: 213, 215, 216].

## Applicazioni
Questi sensori sono fondamentali nell'automazione industriale e automotive:
* [cite_start]**Controllo Processi:** Verifica presenza/assenza componenti su nastri trasportatori[cite: 228].
* [cite_start]**Macchine CNC:** Verifica posizionamento utensili[cite: 230].
* [cite_start]**Automotive (ABS):** Monitoraggio della velocità delle ruote tramite ruote foniche per prevenire il bloccaggio in frenata[cite: 237, 238, 240].

## Evoluzione: IO-Link
Con la tecnologia IO-Link, i sensori induttivi evolvono da semplici interruttori a strumenti di dati, permettendo configurazione remota e manutenzione predittiva.

---
[🔙 Torna all'Indice](./index.html)
