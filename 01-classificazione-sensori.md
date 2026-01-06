<style>
  /* --- STILE ALTA LEGGIBILITÀ (LIM / IPOVISIONE) --- */
  
  body {
    font-family: Arial, Helvetica, sans-serif; /* Font senza grazie, più leggibile */
    font-size: 24px; /* TESTO MOLTO GRANDE */
    line-height: 1.5;
    color: #000000; /* Nero assoluto per massimo contrasto */
    max-width: 100%; /* Usa tutta la larghezza della LIM */
    margin: 0;
    padding: 20px;
    background-color: #ffffff; /* Sfondo bianco puro */
  }

  /* Titoli ad alto contrasto */
  h1 {
    color: #003366; /* Blu Notte scuro */
    font-size: 2em; /* Molto grande */
    border-bottom: 5px solid #003366;
    padding-bottom: 15px;
    margin-bottom: 40px;
    text-transform: uppercase;
  }

  h2 {
    color: #cc0000; /* Rosso Scuro (non acceso) */
    font-size: 1.5em;
    margin-top: 50px;
    border-left: 10px solid #cc0000; /* Banda laterale spessa */
    padding-left: 15px;
    background-color: #fff0f0; /* Sfondo rossino chiarissimo per evidenziare */
  }

  h3 {
    color: #000000;
    font-size: 1.2em;
    font-weight: 900; /* Grassetto pesante */
    margin-top: 30px;
    text-decoration: underline;
  }

  /* Box concettuali con bordi spessi */
  .box {
    border: 4px solid #444; /* Bordo spesso grigio scuro/nero */
    padding: 25px;
    margin-bottom: 40px;
    background-color: #fcfcfc;
    border-radius: 0; /* Angoli vivi si leggono meglio a distanza */
  }

  /* Tabelle ad alto contrasto */
  table {
    width: 100%;
    border-collapse: collapse;
    margin: 30px 0;
    font-size: 0.9em;
  }
  th, td {
    border: 3px solid #000000; /* Griglia nera spessa */
    padding: 15px;
    text-align: left;
  }
  th {
    background-color: #003366; /* Intestazione scura */
    color: #ffffff; /* Testo bianco */
    font-size: 1.1em;
  }
  tr:nth-child(even) {
    background-color: #eeeeee; /* Righe alternate per non perdere il segno */
  }

  /* Immagini ottimizzate */
  img {
    max-width: 90%;
    height: auto;
    display: block;
    margin: 30px auto;
    border: 3px solid #000; /* Cornice nera all'immagine */
  }
  .caption {
    text-align: center;
    font-weight: bold;
    font-size: 0.8em;
    color: #000;
    background: #ffffcc; /* Evidenziatore giallo per le didascalie */
    display: inline-block;
    padding: 5px 10px;
    border: 1px solid #000;
  }

  /* Bottone gigante */
  .btn-nav {
    display: block;
    width: 100%;
    max-width: 400px;
    margin: 50px auto;
    padding: 20px;
    background-color: #003366;
    color: #ffffff;
    text-align: center;
    text-decoration: none;
    font-size: 1.2em;
    font-weight: bold;
    border: 4px solid #000;
  }
  .btn-nav:hover {
    background-color: #000;
    color: #fff;
  }
</style>

# 1. TEORIA DEI TRASDUTTORI

<div class="box">
  <p><strong>OBIETTIVO DELLA LEZIONE:</strong><br>
  Capire come funziona una catena di misura e imparare a classificare i sensori secondo la teoria classica.</p>
</div>

<div class="box">
  <h2>1. LA CATENA DI MISURA</h2>
  <p>Per misurare una grandezza fisica (es. calore, forza) usiamo una serie di blocchi collegati in sequenza.</p>
  
  <p>Lo schema fondamentale è:</p>
  
  <center>
    <img src="./catena-di-misura.png" alt="Schema a blocchi catena di misura">
    <div class="caption">FIG. 1 - Schema a Blocchi della Catena di Misura</div>
  </center>
</div>

<div class="box">
  <h2>2. CLASSIFICAZIONE: PRIMARI vs SECONDARI</h2>
  <p>Questa distinzione riguarda il contatto con la grandezza fisica.</p>

  <table>
    <tr>
      <th>TIPO</th>
      <th>DEFINIZIONE</th>
      <th>ESEMPIO</th>
    </tr>
    <tr>
      <td><strong>PRIMARI</strong></td>
      <td>L'elemento sensibile è a <strong>diretto contatto</strong> con la grandezza fisica. Reagisce subito.</td>
      <td><strong>Termocoppia</strong> (immersa nel liquido).</td>
    </tr>
    <tr>
      <td><strong>SECONDARI</strong></td>
      <td>La grandezza fisica subisce <strong>trasformazioni intermedie</strong> (spesso meccaniche) prima di diventare segnale elettrico.</td>
      <td><strong>Cella di Carico</strong> (Prima si deforma il metallo, poi cambia la resistenza).</td>
    </tr>
  </table>
</div>

<div class="box">
  <h2>3. CLASSIFICA
