<link rel="stylesheet" href="./style.css">

<div class="btn-container">
  <button class="btn btn-print" onclick="window.print()">🖨️ STAMPA PDF</button>
  <a href="./index.html" class="btn btn-nav">🏠 MENU</a>
</div>

# 1. Teoria e Classificazione dei Sensori

<div class="box">
  <h2>SENSORE vs TRASDUTTORE</h2>
  <ul>
    <li><strong>Sensore:</strong> Elemento primario che "sente" la variazione (es. lamina bimetallica).</li>
    <li><strong>Trasduttore:</strong> Dispositivo completo che converte la grandezza in segnale elettrico.</li>
  </ul>
</div>

<div class="box">
  <h2>1. TRASDUTTORI PRIMARI E SECONDARI</h2>
  <p><strong>I) Primari:</strong> Conversione diretta in elettricità (es. Termocoppia).</p>
  <p><strong>II) Secondari:</strong> La grandezza viene prima trasformata in un'altra forma fisica (spesso meccanica).</p>
  
  <img src="./cella-di-carico-ld5.jpg" alt="Cella di Carico">
  <div class="caption">FIG. 1 - Cella di carico: Esempio di Trasduttore Secondario (Forza -> Deformazione -> Resistenza)</div>
</div>

<div class="box">
  <h2>2. CARATTERISTICHE STATICHE</h2>
  <p>Parametri fondamentali per la scelta del sensore:</p>
  <ul>
    <li><strong>Campo di Misura (Portata):</strong> Valori min/max misurabili senza danni.</li>
    <li><strong>Sensibilità:</strong> Rapporto tra variazione uscita e ingresso ($K = \Delta U / \Delta I$).</li>
    <li><strong>Risoluzione:</strong> La più piccola variazione rilevabile.</li>
    <li><strong>Isteresi:</strong> Differenza di lettura tra valore crescente e decrescente.</li>
  </ul>
</div>

<div class="box">
  <h2>3. MODALITÀ DI CONTATTO</h2>
  <p><strong>A) A CONTATTO:</strong> Richiedono un legame fisico con l'oggetto da misurare.</p>
  <ul>
      <li><em>Esempi:</em> Sonda di temperatura PT100, Finecorsa meccanico, Estensimetri.</li>
  </ul>
  
  <p><strong>B) SENZA CONTATTO (Prossimità):</strong> Rilevano a distanza tramite onde o campi magnetici.</p>
  <ul>
      <li><em>Esempi:</em> Fotocellule, Sensori a ultrasuoni, Sensori capacitivi/induttivi.</li>
  </ul>
  
  <img src="./contatto-vs-prossimita.png" alt="Esempi Contatto e Prossimità">
  <div class="caption">FIG. 2 - Finecorsa (Contatto) vs Sensore Ultrasuoni (Senza Contatto)</div>
</div>

<div class="box">
  <h2>4. NATURA DEL SEGNALE</h2>
  <table>
    <tr>
      <th>TIPO</th>
      <th>DEFINIZIONE</th>
      <th>ESEMPIO</th>
    </tr>
    <tr>
      <td><strong>ANALOGICO</strong></td>
      <td>Segnale continuo che segue le variazioni dell'ingresso.</td>
      <td>LM35, Potenziometro.</td>
    </tr>
    <tr>
      <td><strong>DIGITALE</strong></td>
      <td>Valore fornito tramite codice binario (n bit) o impulsi.</td>
      <td>Encoder, Sensore Hall.</td>
    </tr>
  </table>
  
  <img src="./analogico-vs-digitale.png" alt="Segnali">
  <div class="caption">FIG. 3 - Segnale continuo vs Segnale digitale (codificato)</div>
</div>

<div class="box">
  <h2>5. ALIMENTAZIONE</h2>
  <h3 style="color:#27ae60">⚡ ATTIVI (Generatori)</h3>
  <p>Non richiedono alimentazione, generano tensione dal fenomeno fisico (es. Piezo, Termocoppie).</p>

  <h3 style="color:#c0392b">🔋 PASSIVI (Modulatori)</h3>
  <p>Richiedono alimentazione esterna per funzionare (es. NTC, LDR, Potenziometri).</p>
</div>

<br>
<center>
  <a href="./index.html" class="btn btn-nav">⬅ TORNA AL MENU PRINCIPALE</a>
</center>
<br>
