<link rel="stylesheet" href="./style.css">

<div class="btn-container">
  <button class="btn btn-print" onclick="window.print()">🖨️ STAMPA PDF</button>
  <a href="./index.html" class="btn btn-nav">🏠 MENU</a>
</div>

# 1. Teoria e Classificazione dei Sensori

<div class="box">
  <h2>1. SENSORE vs TRASDUTTORE</h2>
  <ul>
    <li><strong>Sensore:</strong> Elemento primario che interagisce con la grandezza (es. la membrana di un microfono).</li>
    <li><strong>Trasduttore:</strong> Dispositivo completo che converte l'energia della grandezza misurata in un segnale elettrico.</li>
  </ul>
</div>

<div class="box">
  <h2>2. TRASDUTTORI PRIMARI E SECONDARI</h2>
  <p><strong>I) TRASDUTTORI PRIMARI:</strong> Convertono direttamente la grandezza fisica in ingresso in una grandezza elettrica.<br>
  <em>Esempio: Una <strong>termocoppia</strong> trasforma il calore direttamente in tensione elettrica.</em></p>

  <p><strong>II) TRASDUTTORI SECONDARI:</strong> Trasformano preventivamente la grandezza fisica in un'altra grandezza fisica, rilevabile poi attraverso un trasduttore primario.</p>
  
  <img src="./cella-di-carico-ld5.jpg" alt="Cella di Carico">
  <div class="caption">FIG. 1 - La Cella di Carico: Forza -> Deformazione Meccanica -> Segnale Elettrico</div>
</div>

<div class="box">
  <h2>3. CARATTERISTICHE STATICHE (Parametri)</h2>
  <ul>
    <li><strong>Campo di misura (Portata):</strong> Intervallo tra valore minimo e massimo misurabile.</li>
    <li><strong>Sensibilità:</strong> Rapporto tra variazione dell'uscita e variazione dell'ingresso ($K = \Delta U / \Delta I$).</li>
    <li><strong>Risoluzione:</strong> La minima variazione della grandezza che il sensore riesce a rilevare.</li>
    <li><strong>Precisione:</strong> Capacità di fornire un valore vicino a quello vero.</li>
  </ul>
</div>

<div class="box">
  <h2>4. MODALITÀ DI CONTATTO</h2>
  <p><strong>A CONTATTO:</strong> Richiedono un legame fisico con l'oggetto (es. termistori, estensimetri, finecorsa meccanici).</p>
  <p><strong>SENZA CONTATTO (PROSSIMITÀ):</strong> Rilevano la grandezza a distanza tramite campi magnetici, onde o luce.</p>
  
  <img src="./prossimita.png" alt="Sensori a contatto vs prossimità">
  <div class="caption">FIG. 2 - Confronto tra rilevamento per contatto e sensori di prossimità</div>
</div>

<div class="box">
  <h2>5. CLASSIFICAZIONE PER SEGNALE</h2>
  <table>
    <tr>
      <th>TIPO</th>
      <th>DESCRIZIONE</th>
      <th>ESEMPIO</th>
    </tr>
    <tr>
      <td><strong>ANALOGICI</strong></td>
      <td>Segnale di uscita continuo che segue le variazioni dell'ingresso.</td>
      <td>Potenziometro, LM35.</td>
    </tr>
    <tr>
      <td><strong>DIGITALI</strong></td>
      <td>Forniscono il valore tramite un codice binario a n bit o impulsi.</td>
      <td>Encoder, Sensore Hall.</td>
    </tr>
  </table>
  
  <img src="./analogico-vs-digitale.png" alt="Segnali Analogico e Digitale">
  <div class="caption">FIG. 3 - Differenza tra segnale continuo e segnale discreto (binario)</div>
</div>

<div class="box">
  <h2>6. ALIMENTAZIONE</h2>
  <h3 style="color:#27ae60">⚡ ATTIVI (Generatori)</h3>
  <p>Generano energia elettrica direttamente dalla grandezza fisica. Non richiedono alimentazione esterna (es. Termocoppie, Piezoelettrici).</p>

  <h3 style="color:#c0392b">🔋 PASSIVI (Modulatori)</h3>
  <p>Richiedono alimentazione esterna per funzionare; il sensore varia una sua proprietà (es. Resistenza in NTC o Potenziometri).</p>
</div>

<br>
<center>
  <a href="./index.html" class="btn btn-nav">⬅ TORNA AL MENU PRINCIPALE</a>
</center>
<br>
