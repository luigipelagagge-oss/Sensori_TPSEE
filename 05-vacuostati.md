 <link rel="stylesheet" href="./style.css">

<div class="btn-container">
  <button class="btn btn-print" onclick="window.print()">🖨️ STAMPA PDF</button>
  <a href="./index.html" class="btn btn-nav">🏠 MENU</a>
</div>

# 5. Vacuostati e Sensori di Vuoto

<div class="box">
  <h2>1. DEFINIZIONE E PRINCIPIO</h2>
  <p>Il <strong>Vacuostato</strong> è un dispositivo progettato per rilevare un livello di pressione negativa (vuoto) in un impianto. Quando il vuoto raggiunge una soglia preimpostata, il dispositivo commuta un segnale elettrico.</p>
  
  <p>Secondo la classificazione studiata:</p>
  <ul>
    <li><strong>Sensore vs Trasduttore:</strong> È generalmente un <em>Trasduttore</em> poiché converte l'energia pneumatica in un segnale elettrico utile al controllo.</li>
    <li><strong>Primario/Secondario:</strong> È un <strong>Trasduttore Secondario</strong>. 
      <br><em>Catena di misura:</em> Vuoto $\rightarrow$ Deformazione Membrana (Grandezza intermedia) $\rightarrow$ Chiusura Contatto (Segnale Elettrico).</li>
  </ul>
</div>

<div class="box">
  <h2>2. CLASSIFICAZIONE E SEGNALE</h2>
  <p>In base al tipo di uscita (vedi Cap. 1 - Classificazione per Segnale), distinguiamo:</p>
  
  <h3>A) VACUOSTATO (Uscita Digitale ON/OFF)</h3>
  <p>Funziona come un interruttore. Fornisce un segnale discreto (1 o 0) quando la pressione scende sotto la soglia di taratura.</p>
  
  <h3>B) TRASDUTTORE DI VUOTO (Uscita Analogica)</h3>
  <p>Fornisce un segnale continuo (es. 0-10V o 4-20mA) proporzionale al livello di vuoto istantaneo.</p>

  <hr>
  
  <h3>Alimentazione</h3>
  <ul>
    <li><strong>Passivi:</strong> I modelli elettromeccanici semplici (contatto pulito) sono passivi (modulatori).</li>
    <li><strong>Attivi:</strong> I moderni vacuostati digitali con display richiedono alimentazione esterna per far funzionare l'elettronica di bordo.</li>
  </ul>
</div>

<div class="box">
  <h2>3. PARAMETRI CARATTERISTICI</h2>
  <p>Analizziamo le specifiche commerciali tipiche in base alla teoria delle caratteristiche statiche:</p>
  
  <ul>
    <li><strong>Campo di Misura (Range):</strong> Solitamente varia da <strong>0 bar a -1 bar</strong> (vuoto relativo).</li>
    <li><strong>Isteresi:</strong> È la differenza tra il punto di commutazione all'attivazione e quello al rilascio. È fondamentale per evitare "rimbalzi" del segnale quando il vuoto è vicino alla soglia.</li>
    <li><strong>Soglia di Intervento:</strong> Il valore regolabile (tramite vite o display) a cui il sensore scatta.</li>
  </ul>
</div>

<div class="box">
  <h2>4. COMPONENTI COMMERCIALI DI RIFERIMENTO</h2>
  
  <h3>I) Vacuostato Elettromeccanico (Es. Serie Festo VPEV o generici)</h3>
  <p>Utilizza una membrana che, deformandosi per la depressione, spinge un microswitch meccanico.</p>
  <ul>
    <li><strong>Vantaggi:</strong> Economico, semplice, nessuna alimentazione richiesta per il sensore (solo per il carico).</li>
    <li><strong>Regolazione:</strong> Tramite vite che precarica una molla antagonista.</li>
  </ul>
  <img src="https://via.placeholder.com/600x300?text=Vacuostato+Elettromeccanico+(Vite+di+regolazione)" alt="Vacuostato Elettromeccanico">

  <h3>II) Vacuostato Elettronico/Digitale (Es. SMC serie ZSE o IFM)</h3>
  <p>Utilizza un sensore piezoresistivo interno e un circuito a microprocessore.</p>
  <ul>
    <li><strong>Caratteristiche:</strong> Display digitale per leggere il valore attuale (monitoraggio).</li>
    <li><strong>Uscite:</strong> Spesso ha sia uscite digitali (PNP/NPN) che uscite analogiche.</li>
    <li><strong>Precisione:</strong> Molto più elevata rispetto ai modelli a membrana.</li>
  </ul>
  <img src="https://via.placeholder.com/600x300?text=Sensore+Digitale+con+Display+(SMC/Festo)" alt="Vacuostato Digitale">
</div>

<br>
<center>
  <a href="./index.html" class="btn btn-nav">⬅ TORNA AL MENU PRINCIPALE</a>
</center>
<br>
