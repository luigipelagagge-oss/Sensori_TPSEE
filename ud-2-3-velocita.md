# U.D. 2.3 - Sensori di Velocità

## Obiettivi (Linee Guida TPSEE)
Analisi della **scelta dei dispositivi** in base alle specifiche tecniche e **condizionamento del segnale** (analogico vs digitale).

---

## 1. La Dinamo Tachimetrica (Soluzione Analogica)
La dinamo tachimetrica è un generatore DC: ruotando l'albero, genera una tensione proporzionale alla velocità.

### Caratteristica di Trasferimento
Il grafico mostra la risposta del sensore: è una retta, quindi il sensore è **lineare**.

![Grafico tensione-velocità dinamo tachimetrica](grafico-dinamo.png)
*Figura 1: Relazione lineare tra giri (rpm) e tensione (V).*

La legge fisica è: $V_{out} = K \cdot n$

---

## 2. L'Encoder Ottico (Soluzione Digitale)
L'encoder non genera tensione variabile, ma impulsi digitali (onda quadra). La velocità si calcola misurando la frequenza di questi impulsi.

![Confronto treni di impulsi](impulsi-encoder.png)
*Figura 2: Bassa velocità = impulsi radi (sinistra). Alta velocità = impulsi frequenti (destra).*

### Metodi di Acquisizione
1.  **Misura di Frequenza:** Conto gli impulsi in un tempo fisso (es. 1 secondo). Ideale per alte velocità.
2.  **Misura di Periodo:** Misuro il tempo tra due impulsi. Ideale per basse velocità.

---

## 3. Laboratorio Virtuale
Codice di esempio per contare gli impulsi (Frequenzimetro):

```cpp
volatile int impulsi = 0;
void setup() {
  Serial.begin(9600);
  attachInterrupt(digitalPinToInterrupt(2), conta, RISING);
}
void loop() {
  delay(1000); // Aspetta 1 secondo
  Serial.print("Impulsi al secondo: ");
  Serial.println(impulsi);
  impulsi = 0; // Reset
}
void conta() {
  impulsi++;
}
