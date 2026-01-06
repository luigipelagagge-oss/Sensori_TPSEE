<link rel="stylesheet" href="./style.css">

<div class="btn-container">
  <button class="btn btn-print" onclick="window.print()">🖨️ STAMPA PDF</button>
  <a href="./index.html" class="btn btn-nav">🏠 MENU</a>
</div>

# 1. Teoria e Classificazione

<div class="box">
  <h2>SENSORE vs TRASDUTTORE: Facciamo chiarezza</h2>
  <p>Spesso usati come sinonimi, hanno in realtà ruoli distinti nella catena:</p>
  <ul>
    <li><strong>Sensore:</strong> È l'elemento primario che "sente" la variazione della grandezza fisica (es. la lamina che si scalda).</li>
    <li><strong>Trasduttore:</strong> È il dispositivo completo che <strong>converte</strong> l'energia della grandezza misurata in un'altra forma (solitamente un segnale elettrico).</li>
  </ul>
  <p><em>In breve: Il sensore è il "naso", il trasduttore è l'intero sistema che traduce l'odore in un segnale elettrico per il computer.</em></p>
</div>

<div class="box">
  <h2>1. LA CATENA DI MISURA</h2>
  <p>Lo schema a blocchi universale che trasforma una grandezza fisica in un segnale interpretabile:</p>

  <img src="./misura-generica.png" alt="Schema Catena di Misura" onerror="this.style.display='none';">
  <div class="caption">FIG. 1 - Struttura di una Catena di Acquisizione Dati</div>
</div>

<div class="box">
  <h2>2. CLASSIFICAZIONE PER SEGNALE IN USCITA</h2>
  <p>Questo criterio riguarda la natura del segnale che inviamo al sistema di controllo.</p>

  <table>
    <tr>
      <th>TIPO</th>
      <th>DESCRIZIONE</th>
      <th>CARATTERISTICHE</th>
    </tr>
    <tr>
      <td><strong>I) ANALOGICI</strong></td>
      <td>Il segnale di uscita varia con <strong>continuità</strong> seguendo fedelmente la variabile fisica.</td>
      <td>Tensione (V) o Corrente (mA) variabili nel tempo.</td>
    </tr>
    <tr>
      <td><strong>II) DIGITALI</strong></td>
      <td>Forniscono il valore tramite un <strong>codice binario</strong> a n bit.</td>
      <td>Segnale discreto, immune ai disturbi (es. <strong>Encoder</strong>).</td>
    </tr>
  </table>
</div>

<div class="box">
  <h2>3. SENSORI PRIMARI E SECONDARI</h2>
  <p>Dipende dal numero di conversioni interne.</p>
  <ul>
    <li><strong>PRIMARI:</strong> Unica conversione (es. Termocoppia: Calore &rarr; Tensione).</li>
    <li><strong>SECONDARI:</strong> Conversioni intermedie (es. Cella di Carico: Forza &rarr; Deformazione &rarr; Resistenza).</li>
  </ul>
</div>

<div class="box">
  <h2>4. SENSORI ATTIVI E PASSIVI</h2>
  
  <h3 style="color:#27ae60">⚡ SENSORI ATTIVI (Generatori)</h3>
  <p>Generano energia elettrica direttamente dalla grandezza fisica. Non serve alimentazione esterna.</p>
  <p><em>Esempi: Piezoelettrici, Dinamo, Termocoppie.</em></p>

  <hr>

  <h3 style="color:#c0392b">🔋 SENSORI PASSIVI (Modulatori)</h3>
  <p>Richiedono una sorgente di energia esterna (alimentazione). Variano un parametro elettrico.</p>
  <p><em>Esempi: Potenziometri, NTC/PTC, Estensimetri.</em></p>

  <img src="./cella-di-carico-ld5.jpg" alt="Esempio Cella di Carico">
  <div class="caption">FIG. 2 - La Cella di Carico è un esempio di trasduttore Passivo</div>
</div>

<div class="box">
  <h2>5. METODI DI MISURA</h2>
  <p><strong>Deflessione:</strong> Lettura rapida su scala (meno preciso).</p>
  <p><strong>Azzeramento:</strong> Confronto con campione noto (massima precisione, es. Ponte di Wheatstone).</p>
</div>

<br>
<center>
  <a href="./index.html" class="btn btn-nav">⬅ TORNA AL MENU PRINCIPALE</a>
</center>
<br>
