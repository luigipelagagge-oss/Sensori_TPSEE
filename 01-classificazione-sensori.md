<link rel="stylesheet" href="./style.css">

<div class="btn-container">
  <button class="btn btn-print" onclick="window.print()">🖨️ STAMPA PDF</button>
  <a href="./index.html" class="btn btn-nav">🏠 MENU</a>
</div>

# 1. Teoria e Classificazione dei Sensori

<div class="box">
  <h2>1. SENSORE vs TRASDUTTORE</h2>
  <ul>
    <li><strong>Sensore:</strong> L'elemento sensibile che interagisce con la grandezza (il "naso").</li>
    <li><strong>Trasduttore:</strong> Il sistema completo che converte l'energia in segnale elettrico.</li>
  </ul>
</div>

<div class="box">
  <h2>2. TRASDUTTORI PRIMARI E SECONDARI</h2>
  <p>Questa classificazione riguarda il numero di conversioni interne al dispositivo:</p>
  
  <p><strong>I) TRASDUTTORI PRIMARI:</strong> Convertono <strong>direttamente</strong> la grandezza fisica in ingresso in una grandezza elettrica.<br>
  <em>Esempio: Una termocoppia trasforma il calore direttamente in tensione.</em></p>

  <p><strong>II) TRASDUTTORI SECONDARI:</strong> Trasformano preventivamente la grandezza in un'altra grandezza fisica, rilevabile poi da un trasduttore primario.<br>
  <em>Esempio: Nella Cella di Carico, la Forza deforma il metallo (grandezza meccanica), e solo allora la resistenza elettrica cambia.</em></p>
  
  
  <div class="caption">FIG. 1 - Esempio di trasduttore secondario (Cella di Carico)</div>
</div>

<div class="box">
  <h2>3. LA CATENA DI MISURA</h2>
  <img src="./misura-generica.png" alt="Schema Catena di Misura" onerror="this.style.display='none';">
  <div class="caption">FIG. 2 - Blocchi funzionali: dalla Grandezza Fisica al Dato Digitale</div>
</div>

<div class="box">
  <h2>4. CLASSIFICAZIONE PER SEGNALE</h2>
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
  
  
  <div class="caption">FIG. 3 - Segnale continuo (Analogico) vs Segnale a gradini (Digitale)</div>
</div>

<div class="box">
  <h2>5. MODALITÀ DI CONTATTO</h2>
  <ul>
    <li><strong>A CONTATTO:</strong> Richiedono un legame fisico (es. Termocoppia, Finecorsa).</li>
    <li><strong>SENZA CONTATTO:</strong> Rilevano a distanza (es. Ultrasuoni, Infrarossi).</li>
  </ul>
  
  <img src="./contatto-vs-prossimita.png" alt="Sensori a contatto vs prossimità">
  <div class="caption">FIG. 4 - Finecorsa meccanico vs Sensore a ultrasuoni</div>
</div>

<div class="box">
  <h2>6. ALIMENTAZIONE</h2>
  <h3 style="color:#27ae60">⚡ ATTIVI (Generatori)</h3>
  <p>Producono segnale senza batteria esterna (es. Termocoppie, Piezoelettrici).</p>

  <h3 style="color:#c0392b">🔋 PASSIVI (Modulatori)</h3>
  <p>Devono essere alimentati per funzionare (es. Potenziometri, NTC, LDR).</p>
</div>

<br>
<center>
  <a href="./index.html" class="btn btn-nav">⬅ TORNA AL MENU PRINCIPALE</a>
</center>
<br>
