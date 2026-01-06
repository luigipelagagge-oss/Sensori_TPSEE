 <link rel="stylesheet" href="./style.css">

<div class="btn-container">
  <button class="btn btn-print" onclick="window.print()">🖨️ STAMPA PDF</button>
  <a href="./index.html" class="btn btn-nav">🏠 MENU</a>
</div>

# 1. Teoria e Classificazione dei Sensori

<div class="box">
  <h2>SENSORE vs TRASDUTTORE</h2>
  <ul>
    <li><strong>Sensore:</strong> L'elemento sensibile che interagisce con la grandezza (il "naso").</li>
    <li><strong>Trasduttore:</strong> Il sistema completo che converte l'energia in segnale elettrico.</li>
  </ul>
</div>

<div class="box">
  <h2>1. LA CATENA DI MISURA</h2>
  <img src="./misura-generica.png" alt="Schema Catena di Misura" onerror="this.style.display='none';">
  <div class="caption">FIG. 1 - Blocchi funzionali: dalla Grandezza Fisica al Dato Digitale</div>
</div>

<div class="box">
  <h2>2. CLASSIFICAZIONE PER SEGNALE</h2>
  <table>
    <tr>
      <th>TIPO</th>
      <th>DESCRIZIONE</th>
      <th>ESEMPI</th>
    </tr>
    <tr>
      <td><strong>ANALOGICI</strong></td>
      <td>Segnale continuo proporzionale alla misura.</td>
      <td>Potenziometro, LM35.</td>
    </tr>
    <tr>
      <td><strong>DIGITALI</strong></td>
      <td>Segnale discreto (codice binario o impulsi).</td>
      <td>Encoder, Sensore Hall.</td>
    </tr>
  </table>
  
  <img src="./analogico-vs-digitale.png" alt="Segnale Analogico vs Digitale">
  <div class="caption">FIG. 2 - Differenza tra segnale continuo (Analogue) e discreto (Digital)</div>
</div>

<div class="box">
  <h2>3. MODALITÀ DI CONTATTO</h2>
  <p>Fondamentale per la scelta del sensore in base all'ambiente di lavoro:</p>
  <ul>
    <li><strong>A CONTATTO:</strong> Richiedono un legame fisico (es. Termocoppia, Finecorsa meccanico).</li>
    <li><strong>SENZA CONTATTO:</strong> Rilevano a distanza (es. Sensori a Ultrasuoni, Infrarossi, Induttivi).</li>
  </ul>
  
  <img src="./contatto-vs-prossimita.png" alt="Sensori a contatto vs prossimità">
  <div class="caption">FIG. 3 - Sinistra: Finecorsa (Contatto) | Destra: Sensore Ultrasuoni (Prossimità)</div>
</div>

<div class="box">
  <h2>4. ALIMENTAZIONE E PRINCIPI</h2>
  <h3 style="color:#27ae60">⚡ ATTIVI (Generatori)</h3>
  <p>Producono segnale senza batteria esterna (es. Termocoppia).</p>

  <h3 style="color:#c0392b">🔋 PASSIVI (Modulatori)</h3>
  <p>Devono essere alimentati per funzionare (es. NTC, LDR).</p>
</div>

<div class="box">
  <h2>5. SIMBOLI DA DATASHEET</h2>
  <p>Ecco come riconoscerli negli schemi tecnici:</p>
  <table>
    <tr>
      <th>Sensore</th>
      <th>Simbolo Grafico</th>
      <th>Grandezza</th>
    </tr>
    <tr>
      <td>Potenziometro</td>
      <td>Resistenza con freccia</td>
      <td>Posizione</td>
    </tr>
    <tr>
      <td>NTC / PTC</td>
      <td>Resistenza con (t°)</td>
      <td>Temperatura</td>
    </tr>
    <tr>
      <td>Encoder</td>
      <td>Cerchio con segnale quadra</td>
      <td>Angolo/Giri</td>
    </tr>
  </table>
</div>

<br>
<center>
  <a href="./index.html" class="btn btn-nav">⬅ TORNA AL MENU PRINCIPALE</a>
</center>
<br>
