# U.D. 2.3 - Sensori di Velocità

## Obiettivi (Linee Guida TPSEE)
In conformità con le competenze richieste per il quinto anno, questa unità analizza la **scelta dei dispositivi** in base alle specifiche tecniche e il **condizionamento del segnale** necessario per l'interfacciamento con i controllori.

---

## 1. La Dinamo Tachimetrica (Soluzione Analogica)
La dinamo tachimetrica è un trasduttore attivo reversibile: tecnicamente è un motore DC a magneti permanenti usato come generatore.

### Caratteristica di Trasferimento
Per il dimensionamento di un sistema di controllo, è fondamentale analizzare la caratteristica statica $V_{out} / n$.

![Grafico tensione-velocità dinamo tachimetrica](grafico-dinamo.jpg)
*Figura 1: La linearità della risposta permette un controllo analogico semplice.*

La legge fisica è:
$$V_{out}(t) = K_E \cdot \omega(t)$$

Dove:
* $V_{out}$: Tensione ai morsetti (Volt).
* $K_E$: Costante di tensione (specificata nel datasheet, es. $10V / 1000rpm$).
* $\omega$: Velocità angolare.

> **Nota per il progetto:** La dinamo fornisce una tensione che può essere positiva o negativa (bipolarità) a seconda del senso di rotazione. Per interfacciarla con Arduino (che legge solo 0-5V), è necessario un circuito di condizionamento (partitore + offset) o un ADC esterno bipolare.

---

## 2. L'Encoder Ottico (Soluzione Digitale)
Nei moderni azionamenti digitali (brushless, stepper), la velocità non viene misurata in tensione, ma nel **dominio del tempo**.

### Dall'impulso alla velocità
L'encoder genera un treno di impulsi digitali (onda quadra). La velocità è proporzionale alla frequenza di questi impulsi.

![Confronto treni di impulsi a diverse velocità](impulsi-encoder.jpg)
*Figura 2: A sinistra bassa velocità (frequenza minore), a destra alta velocità (frequenza maggiore).*

### Algoritmi di Acquisizione (TPSEE)
La scelta dell'algoritmo dipende dalla velocità del processo:

1.  **Misura di Frequenza (Frequency Counting):**
    * *Metodo:* Conto gli impulsi $N$ in una finestra temporale fissa $T$ (es. 100ms).
    * *Formula:* $\omega \propto N/T$.
    * *Utilizzo:* **Alte velocità** (molti impulsi da contare).

2.  **Misura di Periodo (Period Measurement):**
    * *Metodo:* Misuro il tempo $\Delta t$ tra due fronti di salita consecutivi.
    * *Formula:* $\omega \propto 1/\Delta t$.
    * *Utilizzo:* **Basse velocità** (per evitare ritardi nell'aggiornamento del dato).

---

## 3. Laboratorio Virtuale: Simulazione Tachimetro
*Ambiente: Tinkercad / Arduino*

In questo esercizio simuleremo un sensore di velocità utilizzando un generatore di onda quadra (o un pulsante premuto molto velocemente).

**Codice di acquisizione (Snippet "Frequency Counting"):**

```cpp
// Pin collegato all'uscita dell'encoder (Canale A)
const int encoderPin = 2; 
volatile unsigned long impulsi = 0;
unsigned long t_precedente = 0;
const int intervallo = 1000; // Finestra di campionamento 1000ms

void setup() {
  Serial.begin(9600);
  pinMode(encoderPin, INPUT);
  // Interrupt: conta ogni volta che il segnale sale (RISING)
  attachInterrupt(digitalPinToInterrupt(encoderPin), conta, RISING);
}

void loop() {
  // Ogni secondo calcolo e stampo la velocità
  if (millis() - t_precedente >= intervallo) {
    t_precedente = millis();
    
    // Esempio: Encoder da 20 impulsi/giro
    float giri_al_secondo = (float)impulsi / 20.0;
    float rpm = giri_al_secondo * 60;
    
    Serial.print("Velocita': ");
    Serial.print(rpm);
    Serial.println(" RPM");
    
    impulsi = 0; // Reset per la prossima finestra
  }
}

void conta() {
  impulsi++;
}
