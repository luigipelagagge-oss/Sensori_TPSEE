# U.D. 2.2 - Sensori di Posizione e Spostamento

## Obiettivi
In questa unità imparerai a distinguere e utilizzare i principali sensori per rilevare la posizione di un oggetto:
1.  **Potenziometri** (Resistivi)
2.  **LVDT** (Induttivi)
3.  **Encoder Ottici** (Digitali)

---

## 1. Potenziometri (Sensori Resistivi)
È la soluzione più semplice ed economica. Un cursore striscia su una pista resistiva variando la resistenza in base alla posizione.

### Principio di funzionamento
Il potenziometro agisce come un **partitore di tensione variabile**.

Se applichiamo una tensione $V_{in}$ ai capi della resistenza totale $R_{tot}$, la tensione in uscita $V_{out}$ prelevata dal cursore dipende dallo spostamento $x$:

$$V_{out} = V_{in} \cdot \frac{x}{L}$$

Dove:
* $x$ = spostamento del cursore.
* $L$ = lunghezza totale della pista resistiva.

> **Nota:** Il problema principale dei potenziometri è l'usura meccanica dovuta all'attrito del cursore.

---

## 2. LVDT (Trasformatore Differenziale Variabile Lineare)
L'LVDT (*Linear Variable Differential Transformer*) è un sensore **induttivo** molto preciso e privo di attrito (non c'è contatto elettrico strisciante).



### Come funziona
È composto da:
* Un avvolgimento primario (alimentato in AC).
* Due avvolgimenti secondari collegati in opposizione serie.
* Un nucleo ferromagnetico mobile.

Quando il nucleo è al centro, le tensioni indotte si annullano ($V_{out} = 0$). Spostando il nucleo, si crea uno squilibrio che genera una tensione proporzionale allo spostamento.

**Vantaggi:** Vita operativa quasi infinita, altissima risoluzione.

---

## 3. Encoder Ottici (Sensori Digitali)
Gli encoder convertono un movimento angolare in impulsi digitali. Sono fondamentali nella robotica moderna.



Esistono due famiglie principali:

| Caratteristica | Encoder Incrementale | Encoder Assoluto |
| :--- | :--- | :--- |
| **Uscita** | Treni di impulsi (Onda quadra) | Codice binario (es. Gray) |
| **Memoria** | Perde la posizione se manca corrente | Mantiene la posizione assoluta |
| **Costo** | Basso | Alto |
| **Utilizzo** | Velocità motori, mouse, manopole volume | Bracci robotici, CNC |

---

## 4. Laboratorio Interattivo: Encoder Incrementale
Proviamo a gestire un Encoder rotativo standard (KY-040) con un microcontrollore. L'encoder ha due uscite, **CLK (A)** e **DT (B)**, sfasate di 90°.

### Logica di lettura
Per capire la direzione:
* Se l'uscita A cambia stato e B è uguale ad A -> **Senso Orario**.
* Se l'uscita A cambia stato e B è diverso da A -> **Senso Antiorario**.

### Codice Arduino (Interrupt)
L'uso degli *interrupt* garantisce di non perdere passi anche se il microcontrollore è occupato.

```cpp
#define CLK 2  // Pin Interrupt
#define DT  3

volatile int contatore = 0;
int statoCorrenteCLK;
int ultimoStatoCLK;

void setup() {
  pinMode(CLK, INPUT);
  pinMode(DT, INPUT);
  Serial.begin(9600);
  
  // Legge lo stato iniziale
  ultimoStatoCLK = digitalRead(CLK);
  
  // Attiva l'interrupt sul pin 2 (CLK) al cambio di stato
  attachInterrupt(digitalPinToInterrupt(CLK), aggiornaEncoder, CHANGE);
}

void loop() {
  Serial.print("Posizione: ");
  Serial.println(contatore);
  delay(100);
}

void aggiornaEncoder() {
  statoCorrenteCLK = digitalRead(CLK);
  
  // Se lo stato è cambiato, c'è stato un movimento
  if (statoCorrenteCLK != ultimoStatoCLK  && statoCorrenteCLK == 1){
    // Se DT è diverso da CLK, ruota in senso orario
    if (digitalRead(DT) != statoCorrenteCLK) {
      contatore++;
    } else {
      contatore--;
    }
  }
  ultimoStatoCLK = statoCorrenteCLK;
}
