<style>
  body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: #333;
    max-width: 800px;
    margin: 0 auto;
    padding: 20px;
    background-color: #f9f9f9;
  }
  h1 {
    color: #2c3e50;
    border-bottom: 2px solid #3498db;
    padding-bottom: 10px;
  }
  h2 {
    color: #2980b9;
    margin-top: 30px;
  }
  img {
    max-width: 100%;
    height: auto;
    display: block;
    margin: 20px auto;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0,0,0,0.2);
    border: 1px solid #ddd;
  }
  .button {
    display: inline-block;
    padding: 10px 20px;
    margin-top: 20px;
    background-color: #3498db;
    color: white;
    text-decoration: none;
    border-radius: 5px;
    font-weight: bold;
    transition: background-color 0.3s;
  }
  .button:hover {
    background-color: #2980b9;
  }
  .caption {
    text-align: center;
    font-size: 0.9em;
    color: #666;
    font-style: italic;
  }
</style>

# 1. Classificazione e Parametri

Benvenuto nella prima sezione del corso. Qui analizzeremo come è composto un sistema di acquisizione dati e le differenze fondamentali tra le tipologie di sensori.

---

## La Catena di Misura
Ogni sistema di acquisizione dati segue uno schema logico preciso: parte dalla grandezza fisica reale e la trasforma in un dato leggibile dal controllore.

Ecco lo schema fondamentale a blocchi:

![Schema Catena di Misura](catena-di-misura.png)
<p class="caption">Fig. 1 - Schema a blocchi tipico di una catena di acquisizione</p>

---

## Classificazione dei Sensori
Per orientarsi nel mondo dei trasduttori, utilizziamo due macro-categorie principali:

### 1. Sensori Attivi vs Passivi
* **⚡ Sensori Attivi:** Generano autonomamente un segnale elettrico (tensione o corrente) sfruttando principi fisici (es. Termocoppie, Dinamo tachimetriche, Piezoelettrici). Non serve alimentazione esterna per il segnale.
* **🔋 Sensori Passivi:** Si comportano come resistenze variabili. Hanno bisogno di una fonte di energia esterna per funzionare (es. Termistori, Potenziometri, Strain Gauge).

### 2. Analogici vs Digitali
* **Analogici:** Forniscono un segnale continuo nel tempo.
* **Digitali:** Forniscono un segnale a stati discreti (On/Off) o un treno di impulsi.

---

## Esempio Reale: Cella di Carico
Un classico esempio di trasduttore che converte una forza (peso) in un segnale elettrico è la **Cella di Carico**. È un sensore *passivo* basato su ponte estensimetrico.

![Cella di Carico](cella-di-carico-ld5.jpg)
<p class="caption">Fig. 2 - Cella di carico industriale modello LD5</p>

---

<br>
<a href="./index.html" class="button">⬅ Torna all'Indice</a>
