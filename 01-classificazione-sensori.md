<style>
  /* --- STILE ALTO CONTRASTO (PER LIM e PROIEZIONE) --- */
  
  body {
    font-family: Arial, Helvetica, sans-serif;
    font-size: 24px; /* Testo grande per leggere dal fondo */
    line-height: 1.5;
    color: #000000; /* Nero assoluto */
    max-width: 100%;
    margin: 0 auto;
    padding: 20px;
    background-color: #ffffff; /* Sfondo bianco puro */
  }

  /* Titoli visibili anche con luce forte */
  h1 {
    color: #003366; /* Blu notte */
    font-size: 2.2em;
    border-bottom: 5px solid #003366;
    padding-bottom: 15px;
    margin-bottom: 40px;
    text-transform: uppercase;
  }

  h2 {
    color: #cc0000; /* Rosso scuro */
    font-size: 1.6em;
    margin-top: 60px;
    border-left: 15px solid #cc0000; /* Banda laterale molto visibile */
    padding-left: 20px;
    background-color: #fff0f0;
    padding-top: 10px;
    padding-bottom: 10px;
  }

  h3 {
    color: #000;
    font-size: 1.3em;
    font-weight: 900;
    margin-top: 40px;
    text-decoration: underline;
  }

  /* Riquadri per i concetti chiave */
  .box {
    border: 4px solid #000; /* Cornice nera spessa */
    padding: 30px;
    margin-bottom: 40px;
    background-color: #f8f8f8;
  }

  /* Tabelle ad alta leggibilità */
  table {
    width: 100%;
    border-collapse: collapse;
    margin: 30px 0;
    font-size: 1em;
    page-break-inside: avoid;
  }
  th, td {
    border: 3px solid #000; /* Griglia nera marcata */
    padding: 15px;
    text-align: left;
  }
  th {
    background-color: #003366;
    color: #ffffff;
    font-size: 1.1em;
  }
  tr:nth-child(even) {
    background-color: #eeeeee;
  }

  /* Immagini e didascalie */
  img {
    max-width: 80%;
    height: auto;
    display: block;
    margin: 30px auto;
    border: 4px solid #000;
  }
  .caption {
    text-align: center;
    font-weight: bold;
    font-size: 0.9em;
    color: #000;
    background: #ffffcc; /* Evidenziatore giallo */
    border: 2px solid #000;
    display: table;
    margin: 0 auto;
    padding: 10px;
  }

  /* --- PULSANTI (NON visibili in stampa) --- */
  .btn-container {
    text-align: right;
    margin-bottom: 30px;
    border-bottom: 2px solid #ccc;
    padding-bottom: 15px;
  }
  .btn {
    display: inline-block;
    padding: 15px 30px;
    color: #fff;
    text-decoration: none;
    font-weight: bold;
    font-size: 20px;
    border: 3px solid #000;
    margin-left: 15px;
    cursor: pointer;
  }
  .btn-print { background-color: #ff9900; color: #000; } /* Arancione */
  .btn-nav { background-color: #003366; } /* Blu */
  .btn:hover { background-color: #000; color: #fff; }

  /* --- STAMPA PDF (Nasconde menu e adatta colori) --- */
  @media print {
    .btn-container, .btn, .btn-nav { display: none !important; }
    body { font-size: 14pt; }
    h2 { background-color: transparent !important; }
    .box { page-break-inside: avoid; }
  }
</style>

<div class="btn-container">
  <button class="btn btn-print" onclick="window.print()">🖨️ STAMPA PDF</button>
  <a href="./index.html" class="btn btn-nav">🏠 MENU</a>
</div>

# 1. TEORIA E CLASSIFICAZIONE

<div class="box">
  <p><strong>OBIETTIVO:</strong> Comprendere la struttura di una catena di misura e le differenze tra sensori primari/secondari e attivi/passivi.</p>
</div>

<div class="box">
  <h2>1. LA CATENA DI MISURA</h2>
  <p>Ogni sistema di acquisizione dati trasforma una grandezza fisica in un numero.</p>
  <p>Lo schema a blocchi fondamentale è:</p>

  <center>
    <img src="./catena-di-misura.png" alt="Schema a Blocchi">
    <div class="caption">FIG. 1 - Schema della Catena di Misura</div>
  </center>
</div>

<div class="box">
  <h2>2. PRIMARI vs SECONDARI</h2>
  <p>Classificazione basata sulla conversione fisica.</p>
  
  <table>
    <tr>
      <th>TIPO</th>
      <th>DESCRIZIONE</th>
      <th>ESEMPIO</th>
    </tr>
    <tr>
      <td><strong>PRIMARI</strong></td>
      <td>L'elemento sensibile tocca direttamente la grandezza fisica. Reazione immediata.</td>
      <td><strong>Termocoppia</strong> (due fili immersi nel calore).</td>
    </tr>
    <tr>
      <td><strong>SECONDARI</strong></td>
      <td>La grandezza fisica subisce <strong>trasformazioni intermedie</strong> prima di diventare segnale elettrico.</td>
      <td><strong>Cella di Carico</strong> (Forza &rarr; Deformazione &rarr; Variazione Resistenza).</td>
    </tr>
  </table>
</div>

<div class="box">
  <h2>3. ATTIVI vs PASSIVI</h2>
  <p>Classificazione basata sull'energia elettrica.</p>

  <h3>⚡ SENSORI ATTIVI (Generatori)</h3>
  <ul>
    <li><strong>Non richiedono alimentazione esterna.</strong></li>
    <li>Convertono direttamente l'energia fisica in elettricità.</li>
    <li><em>Esempi: Termocoppie, Piezoelettrici, Dinamo Tachimetrica.</em></li>
  </ul>

  <hr style="border: 2px dashed #000; margin: 30px 0;">

  <h3>🔋 SENSORI PASSIVI (Modulatori)</h3>
  <ul>
    <li><strong>Richiedono alimentazione esterna (Batteria/Alimentatore).</strong></li>
    <li>Il sensore varia la sua Resistenza (R), Capacità (C) o Induttanza (L).</li>
    <li><em>Esempi: Termistori, Potenziometri, Strain Gauge.</em></li>
  </ul>

  <center>
    <img src="./cella-di-carico-ld5.jpg" alt="Cella di Carico">
    <div class="caption">FIG. 2 - Cella di Carico (Passivo e Secondario)</div>
  </center>
</div>

<div class="box">
  <h2>4. METODI DI MISURA</h2>
  
  <h3>A. Metodo per DEFLESSIONE</h3>
  <p>L'indice dello strumento si sposta su una scala.</p>
  <ul>
    <li><strong>Vantaggio:</strong> Lettura immediata.</li>
    <li><strong>Svantaggio:</strong> Assorbe energia dal sistema (meno preciso).</li>
    <li><em>Esempio: Multimetro analogico.</em></li>
  </ul>

  <h3>B. Metodo per AZZERAMENTO (Null)</h3>
  <p>Si bilancia il sistema finché la differenza è ZERO.</p>
  <ul>
    <li><strong>Vantaggio:</strong> Altissima precisione (errore nullo all'equilibrio).</li>
    <li><strong>Svantaggio:</strong> Lento, serve tempo per bilanciare.</li>
    <li><em>Esempio: Ponte di Wheatstone.</em></li>
  </ul>
</div>

<br><br>
<a href="./index.html" class="btn btn-nav" style="display:block; text-align:center;">⬅ TORNA AL MENU</a>
