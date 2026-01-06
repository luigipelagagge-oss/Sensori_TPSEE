# U.D. 2.2 - Sensori di Posizione e Spostamento

## Obiettivi
In questa unità analizzeremo come trasdurre una posizione fisica in segnale elettrico, utilizzando simulatori per verificare la teoria.
Argomenti:
1.  **Potenziometri** (Resistivi)
2.  **LVDT** (Induttivi)
3.  **Encoder** (Digitali)

---

## 1. Il Potenziometro come Sensore
Già utilizzato in **Elettrotecnica** come regolatore, in sensoristica il potenziometro è il trasduttore di posizione angolare o lineare più comune ed economico.

### Il richiamo ai Sistemi Automatici
Il potenziometro agisce come un **trasduttore di posizione a uscita analogica**.
Lo schema equivalente è un partitore di tensione. La funzione di trasferimento è lineare:

$$V_{out} = V_{cc} \cdot \alpha$$

Dove $\alpha$ (alfa) è la percentuale di rotazione dell'albero (da 0 a 1).

---

## 2. Laboratorio Virtuale: Tinkercad
*Prerequisiti: Account Autodesk Tinkercad, conoscenze base Arduino.*

Poiché conoscete già Arduino dai corsi di Robotica, utilizzeremo il simulatore per creare un sistema di lettura posizione.

### Esercitazione: "Dalla posizione alla variabile"

**Obiettivo:** Leggere la posizione di un potenziometro (ingresso) e muovere un servomotore (uscita) nella stessa posizione.

**Componenti necessari su Tinkercad:**
* Arduino Uno R3
* Potenziometro (collegato al pin A0)
* Micro Servo (collegato al pin 9 PWM)

**Schema logico:**
Il convertitore ADC di Arduino legge una tensione 0-5V e restituisce un numero intero **0-1023** (10 bit).
Il Servo accetta un comando in gradi **0-180**.

Dobbiamo "mappare" questi due intervalli.

### Codice Sorgente (C++)
Copia questo codice nella sezione "Codice -> Testo" di Tinkercad:

```cpp
#include <Servo.h>

Servo mioServo;  // Oggetto Servo (concetto di Robotica)

const int potPin = A0; // Pin analogico input
int potValue = 0;      // Valore letto (0-1023)
int angle = 0;         // Angolo calcolato (0-180)

void setup() {
  mioServo.attach(9); 
  Serial.begin(9600);
}

void loop() {
  // 1. Acquisizione (Sensore di posizione)
  potValue = analogRead(potPin);
  
  // 2. Elaborazione (Condizionamento segnale)
  // La funzione map() è fondamentale nei sistemi di controllo
  // Sintassi: map(valore, min_in, max_in, min_out, max_out)
  angle = map(potValue, 0, 1023, 0, 180);
  
  // 3. Attuazione
  mioServo.write(angle);
  
  // Debug seriale
  Serial.print("ADC: ");
  Serial.print(potValue);
  Serial.print(" | Gradi: ");
  Serial.println(angle);
  
  delay(15); // Piccola pausa per stabilità meccanica
}
