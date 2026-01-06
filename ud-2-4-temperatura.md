# U.D. 2.4 - Sensori di Temperatura

## Obiettivi (TPSEE)
Analizzare le diverse tecnologie di trasduzione termica per effettuare la scelta ottimale del componente in base a:
1.  **Linearità** (NTC vs LM35).
2.  **Range operativo** (Semiconduttori vs Termocoppie).
3.  **Condizionamento del segnale** (Partitori vs Amplificatori).

---

## 1. I Termistori (NTC e PTC)
Sono resistori termosensibili realizzati con ossidi metallici sinterizzati. Sono sensori **passivi** (richiedono alimentazione).

* **NTC (Negative Temperature Coefficient):** La resistenza diminuisce all'aumentare della temperatura.
* **PTC (Positive Temperature Coefficient):** La resistenza aumenta all'aumentare della temperatura.

### La curva caratteristica
Il problema principale dell'NTC in fase di progettazione è la sua forte **non-linearità**.

![Curva Caratteristica NTC](curva-ntc.jpg)
*Figura 1: Risposta esponenziale di un NTC. A basse temperature la sensibilità è alta, ad alte temperature si appiattisce.*

La legge matematica semplificata (modello $\beta$) è:
$$R(T) = R_0 \cdot e^{\beta (\frac{1}{T} - \frac{1}{T_0})}$$

Dove $T$ è la temperatura in Kelvin.

---

## 2. Sensori Integrati (LM35)
Per semplificare il design elettronico, si utilizzano sensori a semiconduttore che integrano al loro interno il circuito di linearizzazione.

![Pinout LM35](lm35-pinout.jpg)
*Figura 2: L'LM35 è calibrato in gradi Celsius e ha un'uscita lineare.*

* **Vantaggio:** Uscita lineare di **10 mV/°C**.
* **Formula:** $V_{out} = 0.01 \cdot T(°C)$.
* **Esempio:** A 25°C leggiamo esattamente 250mV (0.25V). Non servono calcoli complessi.

---

## 3. Le Termocoppie (Per alte temperature)
Quando dobbiamo misurare temperature sopra i 150°C (forni, motori), i semiconduttori bruciano. Si usano le termocoppie.

### Effetto Seebeck
Se uniamo due metalli diversi (es. Chromel e Alumel per la Tipo K) e scaldiamo la giunzione, si genera una piccolissima differenza di potenziale.

![Effetto Seebeck Schema](termocoppia-schema.jpg)
*Figura 3: Principio fisico della termocoppia.*

> **Nota di Progetto:** Il segnale è dell'ordine dei microvolt ($\mu V$). È obbligatorio usare un amplificatore di precisione (strumentale) prima di collegarlo a un microcontrollore.

---

## 4. Laboratorio: Linearizzazione Software NTC
*Obiettivo: Acquisire un sensore non lineare (NTC) e renderlo leggibile tramite software.*

**Schema Elettrico:** Partitore di tensione con NTC verso massa e Resistenza da 10k$\Omega$ verso i 5V.

**Codice Arduino:**
Utilizzeremo l'equazione di Steinhart-Hart semplificata (Parametro Beta).

```cpp
const int sensorPin = A0;
const float beta = 3950; // Valore tipico dal datasheet NTC
const float R_serie = 10000; // Resistenza del partitore (10k)

void setup() {
  Serial.begin(9600);
}

void loop() {
  int valADC = analogRead(sensorPin);
  
  // 1. Calcolo della Resistenza attuale dell'NTC (Legge di Ohm sul partitore)
  // V_out = V_in * R_ntc / (R_serie + R_ntc) -> Formula inversa:
  float R_ntc = R_serie / (1023.0 / valADC - 1);
  
  // 2. Linearizzazione (Formula del parametro Beta)
  float temperaturaK = 1 / (log(R_ntc / 10000.0) / beta + 1.0 / 298.15);
  float temperaturaC = temperaturaK - 273.15;
  
  Serial.print("Temp: ");
  Serial.print(temperaturaC);
  Serial.println(" C");
  
  delay(500);
}
