Slido 💻
#### 💡 In UDP e TCP, il checksum: 
1. [ ] Consente il controllo della correttezza dei soli campi dell'header del segmento

2. [ ] Consente il controllo della correttezza sia dei campi dell'header sia del payload di un segmento
3. [ ] Consente il controllo della correttezza del solo payload di un segmento
4. [ ] E' calcolato in modo che il ricevitore abbia certezza che il segmento è ricevuto correttamente quando, sommando tutte le parole di 16 bit del segmento checksum incluso, ottiene una parola di 16 bit tutti a 1

##### risposte:
2 - 4

#### 💡 Con riferimento al livello di trasporto, cosa comportano il multipiexing e il demultiplexing?
1. [ ] Al trasmettitore: l'invio di segmenti provenienti da diverse socket sullo stesso link di rete. <br> Al ricevitore: la separazione dei segmenti a seconda della socket di destinazione, e la  consegna a tali socket

2. [ ] L'inserimento di Protocol Control Information per consentire l'indirizzamento dei segmenti dalla socket mittente alla socket ricevente
3. [ ] In UDP, la trasmissione alla stessa socket di tutti i segmenti riportanti lo stesso indirizzo IP di destinazione e la stessa porta di destinazione
4. [ ] In TCP, la trasmissione alla stessa socket di tutti i segmenti riportanti lo stesso indirizzo IP di sorgente, la stessa porta di sorgente, lo stesso indirizzo IP di destinazione e la stessa porta di destinazione

##### risposte:
1 - 2 - 3 - 4

#### 💡 Perché il pipeling migliora l'utilizzo delle risorse di un link tra due host?
1. [ ] Perché consente al mittente di inviare più pacchetti prima di ricevere i corrispondenti ACK 

2. [ ] Perché non satura il buffer di ricezione del ricevente
3. [ ] Perché non satura il buffer di ricezione del mittente
4. [ ] Perché non rimane in silenzio ad attende di ricevere un ACK per ogni pacchetto inviato

##### risposte:
1 - 4




#### 💡 Quali dei seguenti casi rappresenta una conseguenza della congestione?
1. [ ] Se il router ha un buffer infinito: il ritardo molto elevato che si ottiene quando ci si avvicina al throughput massimo di un link 

2. [ ] Se il router ha un buffer limitato: un ritardo eccessivo potrebbe causare timeout prematuri  al mittente, che reinvia inutilmente pacchetti già consegnati 
3. [ ] Se più connessioni si dividono lo stesso link: ogni connessione osserva esattamente lo stesso throughput 
4. [ ] In situazioni tipiche: vengono scartati i pacchetti che trovano buffer pieni nei router, e w serve più lavoro per consegnare i segmenti -> throughput ridotto 

##### risposte:
1 - 2 - 4


#### 💡 Come fa un host A a chiudere una connessione TCP con l'host B?
1. [ ] A invia un segmento con flag RST a 1

2. [ ] A invia un segmento con flag FIN a 1, B risponde con un segmento con flag FIN e ACK a 1
3. [ ] A invia un segmento con flag FIN a 1, B risponde con un segmento con flag FIN e ACK a 1, B invia ad A i dati rimasti, B invia FIN, A risponde con FIN+ACK 
4. [ ] A invia un segmento con flag FIN a 1, B risponde con un segmento con flag FIN e ACK a 1, B invia FIN, A risponde con FIN+ACK 

##### risposte:
1 - 3 - 4





#### 💡 Cos'è il Fast Recovery in TCP?
1. [ ] Uno stato in cui si entra dopo aver ricevuto 3 ACK duplicati 

2. [ ] Uno stato in cui si entra dopo aver ricevuto 1 ACK duplicato 
3. [ ] Uno stato nel quale ogni ACK duplicato ricevuto permette di aumentare la dimensione della CWND di 1 segmento 
4. [ ] L'operazione per cui dopo il terzo ACK duplicato si ritrasmette immediatamente il segmento puntato da tali AKC duplicati

##### risposte:
1 - 3



#### 💡 Quali affermazioni riguardo al retransimition timeout (RTO) in TCP sono corrette?
1. [ ] Viene calcolato come il doppio dell'RTT istantateno misurato sull'ultimo pacchetto

2. [ ] Viene calcolato usando la media mobile esponenzialmente pesata che tiene conto dell'RTT medio e della deviazione media dell'RTT istantaneo da quello medio
3. [ ] Se è impostato a un valore troppo alto, il mittente reagisce troppo lentamente alle perdite
4. [ ] Se è impostato a un valore troppo basso, innalza il rischio di ritrasmissioni inutili

##### risposte:
2 - 3 - 4

#### 💡 In che modo BBR cerca di migliorare le prestazioni della versione di TCP vista a lezione?
1. [ ] Controllando la coda di trasmissione per vedere quanti segmenti vi si accumulano, e regolare di conseguenza il tasso di trasmissione, sondando poi periodicamente se ci sono cambiamenti di banda

2. [ ] Trasmettendo segmenti a rate ben più alto di quello supportato dal link di collo di bottiglia, trascurando eventuali perdite a prezzo della fairness
3. [ ] Trasmettendo segmenti a rate ben più alto du quello supportato dal link collo di bottiglia, e utilizzando ACK negativi per capire quali pacchetti sono stati persi
4. [ ] Usando una funzione cubica del numero di RTT per allargare o restringere la finestra di trasmissione nel tempo

##### risposta:
1


####
---

Domande Esami 🗂

#### 📌 Dato un collegamento a 100Mbit/s e un ritardo di propagazione di 40ms, calcolare la dimensione della PDU (in byte) di un protocollo stop-and-wait in modo che abbia un throughput di 10Mbit/s.
Un protocollo stop-and-wait prevede di avere un trasmettitore che invia un singolo pacchetto alla volta e attende un ACK prima di inviare la successiva.

Il tempo totale tra la trasmissione di una PDU e l'altra è di 40 ms all'andata e 40 ms al ritorno. Pertanto, la PDU in bytes è data da 10 Mbit/s * (0,04 + 0,04) s = 0,8 Mbit = 800 Kbit
In byte: 800 000 / 8 = 100 000 byte.

#### 📌 Dato un collegamento a 100Mbit/s e un ritardo di propagazione di 40ms, qual'è il throughput massimo di un protocollo stop-and-wait? Spiegare brevemente perché.
La dimensione massima è quella di Ethernet meno i 40 byte di header.

#### 📌 Cosa significa che un servizio di telecomunicazione è "orientato alla connessione"?
Un servizio è orientato alla connessione se viene impostato un setup dedicato di connessione per lo scambio di messaggi in rete. Ad esempio TCP è orientato alla connessione attraverso un processo di three-way-handshake per instaurare la connessione tra mittente e ricevitore.
(A: SYN = 1 - B: ACK = 1, SYN = 1 - A: ACK = 1)

#### 📌 Definire UDP e TCP.
UDP (User Datagram Protocol): protocollo di trasporto best effort, non affidabile e non orientato alla connessione. Non garantisce la ricezione dei pacchetti o l'ordine di arrivo. Molto semplice e per questo con basso overhead e poco ritardo causato per esempio da controllo di errori.
Usato nelle applicazioni multimediali o DNS, dove è più importarte il traffico continuo del flusso dati, rispetto al controllo di errori sui singoli segmenti.

TCP (Transmition Control Protocol): protocollo di trasporto affidabile e orientato alla connessione, garantisce l'ordine e la ricezione dei pacchetti, effettua controllo di flusso e di congestione.
L'header di TCP è più complesso rispoetto a UDP, aggiungendo oltre ai flag, la dimensione della finestra di ricezione, il numero di sequenza (primo byte del flusso) e il numero di ACK (numero di sequenza del prossimo byte atteso).
Prevede un setup di connessione 3-way-handshake. La chiusura di connessione deve essere fatta da entrambe le parti, essendo TCP bidirezionale.

#### 📌 Definire Slow Start e Congestion Avoidance.
Nella fase di Slow Start ad ogni ACK ricevuto si aumenta la CWND di 1 MSS, quindi nel tempo la finestra aumenta esponenzialmente.
Raggiunto il valore della soglia di slow start si entra di Congestion Avoidance, dove, d ogni ACK ricevuto, si aumenta la CWND di MSS * MSS/CWND ovvero di 1/CWND segmenti, aumento che è quindi lineare