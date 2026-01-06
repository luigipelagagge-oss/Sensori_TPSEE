# U.D. 2.4 - Sensori di Temperatura

## Obiettivi della Lezione
In questa unità analizzeremo i trasduttori che convertono una variazione termica in un segnale elettrico.



## 1. Termistori (NTC e PTC)
I termistori sono resistori che variano la loro resistenza con la temperatura.

* **NTC (Negative Temperature Coefficient):** La resistenza diminuisce all'aumentare della temperatura.
* **PTC (Positive Temperature Coefficient):** La resistenza aumenta all'aumentare della temperatura.

### La Legge Fisica (Modello Semplificato)
La relazione approssimata per un NTC vicino alla temperatura di riferimento $T_0$ (solitamente 25°C o 298.15 K) è:

$$R(T) = R_0 \cdot e^{ B \left( \frac{1}{T} - \frac{1}{T_0} \right) }$$

Dove:
* $R(T)$ è la resistenza alla temperatura $T$ (in Kelvin).
* $R_0$ è la resistenza alla temperatura $T_0$.
* $B$ è la costante caratteristica del materiale (es. 3950 K).

---

## 2. Esercitazione Interattiva: Arduino e NTC
Proviamo a leggere un sensore NTC. Ecco lo schema di collegamento del partitore di tensione.



### Codice Sorgente
```cpp
// Esempio lettura NTC su Arduino
const int sensorPin = A0;
const float R_series = 10000.0; // Resistenza serie da 10k

void setup() {
  Serial.begin(9600);
}

void loop() {
  int sensorValue = analogRead(sensorPin);
  // Conversione in tensione e calcolo resistenza...
  Serial.println(sensorValue);
  delay(500);
}
