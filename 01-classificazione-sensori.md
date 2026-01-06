<link rel="stylesheet" href="./style.css">

<div class="btn-container">
  <button class="btn btn-print" onclick="window.print()">🖨️ STAMPA PDF</button>
  <a href="./index.html" class="btn btn-nav">🏠 MENU</a>
</div>

# 1. Teoria e Classificazione dei Sensori

<div class="box">
  <h2>SENSORE vs TRASDUTTORE</h2>
  <p>Prima di classificare, distinguiamo i componenti:</p>
  <ul>
    <li><strong>Sensore:</strong> L'elemento sensibile che interagisce con la grandezza (es. la membrana di un microfono).</li>
    <li><strong>Trasduttore:</strong> Il sistema completo che trasforma l'energia fisica in segnale elettrico.</li>
  </ul>
</div>

<div class="box">
  <h2>1. LA CATENA DI MISURA</h2>
  <p>Lo schema che porta dalla realtà fisica al dato numerico:</p>
  
  <img src="./misura-generica.png" alt="Schema Catena di Misura" onerror="this.style.display='none';">
  <div class="caption">FIG. 1 - Blocchi funzionali: Sensore -> Condizionamento -> ADC</div>
</div>

<div class="box">
  <h2>2. CLASSIFICAZIONE PER SEGNALE IN USCITA</h2>
  <table>
    <tr>
      <th>TIPO</th>
      <th>DESCRIZIONE</th>
      <th>ESEMPI PRATICI</th>
    </tr>
    <tr>
      <td><strong>ANALOGICI</strong></td>
      <td>Segnale continuo (V o mA) proporzionale alla grandezza.</td>
      <td>Potenziometro, LM35 (Temp).</td>
    </tr>
    <tr>
      <td><strong>DIGITALI</strong></td>
      <td>Segnale discreto (livelli logici 0-1 o codice binario).</td>
      <td>Encoder rotativo, Sensore Hall.</td>
    </tr>
  </table>
  
  <img src="./analogico-vs-digitale.png" alt="Segnale Analogico vs Digitale">
  <div class="caption">FIG. 2 - Differenza tra segnale continuo e discreto</div>
</div>

<div class="box">
  <h2>3. CLASSIFICAZIONE PER ALIMENTAZIONE (Energetica)</h2>
  
  <h3 style="color:#27ae60">⚡ SENSORI ATTIVI (Generatori)</h3>
  <p>Non richiedono alimentazione esterna. Generano tensione sfruttando fenomeni fisici.</p>
  <ul>
    <li><strong>Esempi:</strong> Termocoppie (Effetto Seebeck), Piezoelettrici (Effetto piezo).</li>
  </ul>

  <h3 style="color:#c0392b">🔋 SENSORI PASSIVI (Modulatori)</h3>
  <p>Richiedono alimentazione esterna. Variano una caratteristica elettrica (R, L, C).</p>
  <ul>
    <li><strong>Esempi:</strong> Fotoresistenze (LDR), Estensimetri, Termistori (NTC/PTC).</li>
  </ul>
  
  <img src="./cella-di-carico-ld5.jpg" alt="Esempio Sensore Passivo">
  <div class="caption">FIG. 3 - Cella di Carico: necessita di alimentazione per leggere la variazione di R</div>
</div>

<div class="box">
  <h2>4. MODALITÀ DI CONTATTO</h2>
  <ul>
    <li><strong>A CONTATTO:</strong> Il sensore deve toccare l'oggetto (es. sonda di temperatura a immersione, estensimetro).</li>
    <li><strong>SENZA CONTATTO (Prossimità):</strong> Rilevamento a distanza (es. Ultrasuoni, Infrarossi, Radar).</li>
  </ul>
  
  
</div>

<div class="box">
  <h2>5. PRINCIPI FISICI DI FUNZIONAMENTO</h2>
  <p>In base a cosa cambia all'interno del sensore:</p>
  <ul>
    <li><strong>Resistivi:</strong> Varia la Resistenza (R). <em>Es: potenziometro, LDR.</em></li>
    <li><strong>Capacitivi:</strong> Varia la Capacità (C). <em>Es: sensori di umidità.</em></li>
    <li><strong>Induttivi:</strong> Varia l'Induttanza (L). <em>Es: sensori di posizione metallici.</em></li>
    <li><strong>Termoelettrici:</strong> Generano tensione per calore. <em>Es: Termocoppie.</em></li>
  </ul>
</div>

<br>
<center>
  <a href="./index.html" class="btn btn-nav">⬅ TORNA AL MENU PRINCIPALE</a>
</center>
<br>
