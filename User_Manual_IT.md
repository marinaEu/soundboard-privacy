# [cite_start]Liutalab - Manuale d'uso [cite: 1]

## Introduzione
[cite_start]L'app che stai utilizzando ha lo scopo di definire correttamente dimensioni, forma e numero di catene, ovverosia dei rinforzi incollati sotto la tavola armonica della chitarra[cite: 8]. [cite_start]Il sistema calcola inoltre lo spessore della tavola armonica considerando i legni utilizzati ed eventuali rinforzi in fibra di carbonio o altri materiali[cite: 8].

All'interno di Liutalab troverai due componenti fondamentali:
* [cite_start]Una sezione relativa alla progettazione delle parti che compongono la soundboard[cite: 9].
* [cite_start]Una parte dedicata alla verifica strumentale della soundboard prima di essere incollata alle fasce, che permette di effettuare gli ultimi ritocchi sulle catene strutturali[cite: 9].

> [cite_start]**Nota:** Nel testo seguente si utilizzerà il nome "chitarra" per descrivere lo strumento deputato all'uso di questo applicativo[cite: 10]. [cite_start]Considera questa semplificazione un modo per identificare tutti gli strumenti acustici con piano armonico piatto e corde in tensione[cite: 10].

---

## Cenni di statica dello strumento
[cite_start]Prima di descrivere il programma, è utile un ripasso relativo alla statica dello strumento in relazione alle tensioni meccaniche impartite dalle corde alla soundboard[cite: 16].

[cite_start]Esistono principalmente due tipi di chitarra[cite: 17]:
* [cite_start]**Chitarra classica (corde di nylon):** Sottoposta a sollecitazioni dell'ordine di 25-35kgf[cite: 17, 18].
* [cite_start]**Chitarra acustica (corde in metallo):** Sottoposta a sollecitazioni di 40-80kgf[cite: 17, 18].
* [cite_start]**Altri strumenti (es. ukulele):** Prima di procedere, bisogna evincere il carico di sollecitazione in base al numero di corde, materiale e lunghezza del diapason[cite: 19].

[cite_start]La resistenza meccanica di qualsiasi struttura tensionata dipende dalla geometria della sezione e dalle caratteristiche dei materiali[cite: 25]. [cite_start]La chitarra non deve collassare sotto il carico delle corde, ma deve avere una massa mobile dell'insieme tavola-catene la più bassa possibile: tanto più leggera e mobile è la tavola, tanto più forte e bene suona[cite: 26].

[cite_start]Le grandezze strutturali di riferimento sono[cite: 31, 32]:
* [cite_start]**Modulo di elasticità (E)** o modulo di Young[cite: 31].
* [cite_start]**Momento di inerzia di area (I)**[cite: 31].
* [cite_start]**Rigidezza flessionale (E*I):** Il prodotto di E e I, ed è il riferimento più importante nel dimensionamento della soundboard[cite: 32].

[cite_start]La condizione staticamente migliore per l'acustica prevede una rotazione del ponte di circa 1,5-2° in avanti sotto la trazione delle corde[cite: 33, 34]. [cite_start]Per ottenere ciò, la *flexural rigidity* dovrebbe essere circa 15 per le classiche e 50 per le acustiche, proporzionata al carico delle corde[cite: 37]. 
[cite_start]Lo scopo di Liutalab è proprio il corretto dimensionamento in merito a questo valore[cite: 38].

---

## [cite_start]Utilizzo di Liutalab [cite: 39]
[cite_start]Il programma è strutturato in quattro sottomenu[cite: 47]:
1.  [cite_start]**Overall** [cite: 47]
2.  [cite_start]**Braces** [cite: 47]
3.  [cite_start]**Carbon fiber** [cite: 47]
4.  [cite_start]**Results** [cite: 47]

[cite_start]I primi tre menù definiscono le variabili necessarie al calcolo del valore E*I[cite: 48]. Modificando i valori (spessori, catene, materiali) si punta a raggiungere il valore di rigidezza obiettivo[cite: 49]. 
*Attenzione: Questo strumento di aiuto al liutaio deve essere utilizzato con criterio e in linea con le buone pratiche[cite: 50]. [cite_start]Fai attenzione alle unità di misura (metri, centimetri, millimetri o pollici)[cite: 51].*

---

### [cite_start]Impostazioni Generali (Settings) [cite: 55]
[cite_start]Il menù si trova in ogni pagina cliccando sui tre punti in alto a destra[cite: 57].

* [cite_start]**Length units:** Consigliamo di utilizzare il millimetro come unità principale per avere più precisione dopo il punto decimale[cite: 59].
* **Theme:** Riguarda l'aspetto della grafica, chiara o scura[cite: 69].

![Menu Settings e Length Units](images/settings_menu.png)

---

### OVERALL [cite: 81]
Definisce le proprietà generali della soundboard.

* [cite_start]**Board width:** Larghezza della soundboard in mm misurata 50mm sopra il ponticello[cite: 83].
* [cite_start]**Board thickness:** Spessore della tavola armonica in mm (precisione al decimo di mm)[cite: 92].
* **Board material:** Scegliendo il materiale, il programma applica il modulo elastico tabellare[cite: 95]. È possibile inserire il valore "by measure" se misurato sperimentalmente o evinto dalla certificazione[cite: 96].

#### Double Top con Honeycomb
Selezionando "Yes" alla voce "Would you like to craft Double Top with honeycomb?", si attiva una seconda parte del menù[cite: 99, 102].
* [cite_start]**Honeycomb Thickness:** Spessore in mm (al decimo di mm) del materiale (tipicamente aramidico) posto tra la tavola superiore e la *inner soundboard*[cite: 104].
* [cite_start]**Inner soundboard thickness:** Spessore della tavola incollata sotto la board e l'honeycomb[cite: 122].
* **Boards ratio:** Rapporto tra la larghezza della inner soundboard e la larghezza della board[cite: 125]. Tipicamente impostato a un valore inferiore a 1 per considerare la riduzione dello spessore dell'honeycomb ai bordi[cite: 126].
* **Inner soundboard material:** Il legno usato può essere diverso da quello superiore. [cite_start]Scegli dalla lista o inserisci "by measure"[cite: 129, 130].

![Menu Overall UI](images/overall_menu.png)

---

### [cite_start]BRACES [cite: 151]
Configurazione dello schema di incatenatura.

* **Braces number:** Numero di catene con scopo strutturale (es. Xbracing = 2; Vented = 5 o 7; V type = 2; Lattice = intersezioni a 50mm sopra il ponte, tipicamente 8)[cite: 158, 159, 160].
* [cite_start]**Average braces orientation:** Angolo di inclinazione medio rispetto alle corde (es. Xbracing 35-45°, vented 5-10°)[cite: 168, 169, 170].
* [cite_start]**Transverse braces shape:** Il programma ammette forma trapezia e parabolica[cite: 175]. [cite_start]La forma trapezia copre anche forme rettangolari, quadrate e triangolari, a seconda della base minore[cite: 176, 179].
    * [cite_start]**Base max (B):** Dimensione della base incollata sulla tavola[cite: 182].
    * **Base min (b):** Dimensione della base minore[cite: 186]. Se impostata a "1", la catena è pressoché triangolare; se uguale alla *Base max*, la sezione è rettangolare o quadrata[cite: 187, 188, 199].
    * [cite_start]**Height (H):** Altezza in mm delle catene trapezie[cite: 200].
* [cite_start]**Braces Material:** Il materiale delle catene può essere diverso da quello della soundboard, garantendo massima flessibilità[cite: 207, 210, 211].

![Diagramma Forma Catene](images/braces_shape.png)
![Menu Braces UI](images/braces_menu.png)

---

### [cite_start]CARBON FIBER [cite: 225]
[cite_start]Questo menù permette di gestire l'aggiunta di rinforzi (in fibra di carbonio o altri materiali resistenti) per aumentare la rigidezza flessionale senza appesantire troppo la struttura[cite: 225]. [cite_start]I rinforzi si intendono ricavati da laminati incollati alle catene[cite: 225].

* [cite_start]**Brace reinforcement material:** Scegli il materiale dalla lista o inserisci un valore "by measure" dal datasheet[cite: 225].
* **Reinforcement thickness on max base:** Spessore applicato tra soundboard e base delle catene (su tutte le catene)[cite: 225].
* [cite_start]**Reinforcement thickness on min base:** Spessore incollato sopra la base minore[cite: 225]. [cite_start]*Nota: Incollare lo spessore sulla base minore è una modalità decisamente più efficace per aumentare la rigidezza[cite: 225].*
* **Reinforcement thickness on each slope side:** Spessore applicato su entrambi i bordi delle catene trapezie (calcolato automaticamente due volte)[cite: 225].

![Menu Carbon Fiber UI](images/carbon_fiber_menu.png)

---

### RESULTS [cite: 226]

* [cite_start]**Flexural rigidity:** Mostra i risultati di rigidezza flessionale della soundboard con catene e, se configurata, della variante double top[cite: 231]. [cite_start]Se il valore è superiore o inferiore al target, modifica i dati di progetto (spessori, materiali, dimensioni catene) per avvicinarti al valore desiderato[cite: 232, 233]. [cite_start]Il calcolo si aggiorna in automatico[cite: 234].
* [cite_start]**Suggested flexural rigidity:** Mostra numeri di riferimento basati sullo strumento[cite: 248]. [cite_start]Non esiste un numero univocamente corretto, poiché varia a seconda dello spessore delle corde utilizzate[cite: 249].

#### [cite_start]Deflection-based stiffness check [cite: 235]
[cite_start]Sezione utile per la verifica strumentale della soundboard provvista di catene[cite: 241]. 
[cite_start]Si procede appoggiando la soundboard su due supporti a distanza fissa (*Span length* o "L"), applicando un carico (*Load applied*) al centro, e misurando la deflessione (*Measured deflection*)[cite: 242, 244]. 

[cite_start]Il numero risultante è il valore di rigidezza flessionale effettivo[cite: 245]:
* [cite_start]**Se è superiore all'obiettivo:** Riduci la sezione delle catene strutturali[cite: 245].
* **Se è inferiore:** Aggiungi ulteriori rinforzi[cite: 245].

![Diagramma Deflection Check](images/deflection_check.png)
![Menu Results UI](images/results_menu.png)