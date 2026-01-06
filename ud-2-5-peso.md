# U.D. 2.5 - Sensori di Peso e Deformazione

## Obiettivi (TPSEE)
In questa unità affronteremo una sfida tipica della progettazione elettronica: come misurare una variazione di resistenza microscopica.
Analizzeremo:
1.  **L'Estensimetro:** Il sensore base.
2.  **Il Ponte di Wheatstone:** Il circuito di condizionamento obbligatorio.
3.  **La Cella di Carico:** Il componente industriale finito.

---

## 1. L'Estensimetro (Strain Gauge)
L'estensimetro è un sensore resistivo che cambia la sua resistenza quando viene deformato (stirato o compresso).

### Principio Fisico
Si basa sulla seconda legge di Ohm: $R = \rho \frac{L}{S}$.
Se tiro un filo metallico, la sua lunghezza $L$ aumenta e la sua sezione $S$ diminuisce. Entrambi i fenomeni causano un **aumento della resistenza**.

![Estensimetro a resistenza](estensimetro.png)
*Figura 1: La classica forma a serpentina serve a massimizzare la lunghezza del conduttore sensibile nella direzione della deformazione.*

> **Il Problema Tecnico:** La variazione di resistenza ($\Delta R$) è piccolissima, nell'ordine dei millesimi di Ohm su una resistenza base di 120Ω o 350Ω. Un normale multimetro o un partitore di tensione con Arduino non riuscirebbe a misurarla con precisione.

---

## 2. Il Condizionamento: Ponte di Wheatstone
Per misurare variazioni così piccole, non si misura la resistenza direttamente, ma si usa un circuito a ponte che converte la differenza di resistenza in una differenza di potenziale (Tensione).

![Schema del Ponte di Wheatstone](ponte-wheatstone.png)
*Figura 2: Schema a rombo. Se il ponte è bilanciato ($R_1=R_2=R_3=R_x$), la tensione $V_{out}$ è zero.*

### Funzionamento per il Progetto
Quando l'estensimetro ($R_x$) si deforma, il ponte si sbilancia e genera una tensione $V_{out}$ proporzionale alla deformazione.

Per un ponte con un solo sensore attivo (quarto di ponte), la formula approssimata è:
$$V_{out} \approx \frac{V_{in}}{4} \cdot \frac{\Delta R}{R}$$

Anche con questo circuito, il segnale $V_{out}$ è dell'ordine dei **millivolt (mV)**. È troppo basso per l'ADC di Arduino (che legge step di circa 5mV).

> **Soluzione TPSEE:** È obbligatorio usare un **amplificatore differenziale da strumentazione** (Instrumentation Amplifier) o un ADC ad alta risoluzione (es. 24-bit HX711) subito dopo il ponte.

---

## 3. La Cella di Carico (Componente Industriale)
Negli impianti reali non si incollano i singoli estensimetri a mano. Si comprano le **Celle di Carico**, che sono blocchi metallici (alluminio o acciaio) con già 4 estensimetri incollati e collegati a ponte intero al loro interno.

![Cella di carico industriale](cella-carico.png)
*Figura 3: Una tipica cella di carico "beam". Si fissa un lato e si applica il peso sull'altro.*

### Cablaggio Standard
Le celle di carico hanno solitamente 4 fili:
* **Rosso/Nero:** Alimentazione del ponte (E+ / E-), es. 5V e GND.
* **Verde/Bianco:** Uscita del segnale differenziale (S+ / S-), nell'ordine dei mV.

---

## 4. Verifica delle Competenze (TPSEE)
<details>
<summary><strong>Domanda: Perché non posso collegare direttamente una cella di carico (fili verde/bianco) ai pin A0 e GND di Arduino?</strong></summary>
<br>
<strong>Risposta:</strong> Perché il segnale in uscita dalla cella è troppo piccolo (pochi millivolt). L'ADC a 10-bit di Arduino Uno non ha abbastanza risoluzione per leggerlo. Vedresti sempre 0 o valori casuali dovuti al rumore. Serve un amplificatore intermedio (come il modulo HX711).
</details>
