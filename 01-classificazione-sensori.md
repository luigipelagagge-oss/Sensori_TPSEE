<link rel="stylesheet" href="./style.css">

<div class="btn-container">
  <button class="btn btn-print" onclick="window.print()">🖨️ STAMPA PDF</button>
  <a href="./index.html" class="btn btn-nav">🏠 MENU</a>
</div>

# 1. Teoria e Classificazione dei Sensori

<div class="box">
  <h2>1. SENSORE vs TRASDUTTORE</h2>
  <ul>
    <li><strong>Sensore:</strong> L'elemento sensibile che interagisce con la grandezza (es. la membrana).</li>
    <li><strong>Trasduttore:</strong> Il sistema completo che converte l'energia fisica in segnale elettrico.</li>
  </ul>
</div>

<div class="box">
  <h2>2. TRASDUTTORI PRIMARI E SECONDARI</h2>
  <p><strong>I) TRASDUTTORI PRIMARI:</strong> Convertono direttamente la grandezza fisica in ingresso in una elettrica.<br>
  <em>Esempio: <strong>Termocoppia</strong> (Calore &rarr; Tensione).</em></p>

  <p><strong>II) TRASDUTTORI SECONDARI:</strong> Trasformano la grandezza in un'altra fisica (es. meccanica), rilevata poi da un primario.</p>
  
  <img src="./cella-di-carico-ld5.jpg" alt="Cella di Carico">
  <div class="caption">FIG. 1 - La Cella di Carico: Forza (F) &rarr; Deformazione (&Delta;L) &rarr; Variazione Resistenza (&Delta;R)</div>
</div>

<div class="box">
  <h2>3. CARATTERISTICHE FONDAMENTALI (Parametri)</h2>
  <p>Per scegliere un sensore dobbiamo analizzare le sue caratteristiche:</p>
  <ul>
    <li><strong>Campo di misura (Portata):</strong> L'intervallo tra il valore minimo e massimo misurabile.</li>
    <li><strong>Sensibilità:</strong> Il rapporto tra la variazione dell'uscita e la variazione dell'ingresso ($K = \Delta U / \Delta I$).</li>
    <li><strong>Risoluzione:</strong> La minima variazione della grandezza che il sensore riesce a rilevare.</li>
    <li><strong>Precisione:</strong> La capacità di fornire un valore vicino a quello vero.</li>
    <li><strong>Linearità:</strong> Indica quanto la risposta del sensore si avvicina a una retta.</li>
  </ul>
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
      <td>Segnale discreto (Codice binario o impulsi).</td>
      <td>Encoder, Sensore Hall.</td>
    </tr>
  </table>
  <img src="./analogico-vs-digitale.png" alt="Segnale Analogico vs Digitale">
</div>

<div class="box">
  <h2>5. MODALITÀ DI CONTATTO</h2>
  <ul>
    <li><strong>A CONTATTO:</strong> Richiedono legame fisico (es. Termistori, Finecorsa).</li>
    <li><strong>SENZA CONTATTO:</strong> Rilevano a distanza (es. Ultrasuoni, Infrarossi, Magnetici).</li>
  </ul>
  <img src="./contatto-vs-prossimita.png" alt="Esempi di contatto">
</div>

<div class="box">
  <h2>6. ALIMENTAZIONE</h2>
  <h3 style="color:#27ae60">⚡ ATTIVI (Generatori)</h3>
  <p>Generano energia elettrica da soli (es. Termocoppie, Piezoelettrici).</p>

  <h3 style="color:#c0392b">🔋 PASSIVI (Modulatori)</h3>
  <p>Necessitano di alimentazione esterna per funzionare (es. Potenziometri, NTC, LDR).</p>
</div>

<br>
<center>
  <a href="./index.html" class="btn btn-nav">⬅ TORNA AL MENU PRINCIPALE</a>
</center>
<br>
