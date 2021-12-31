#### 💡 Nella rete Internet, gli host si trovano:
1. [ ] Ai confini della rete

2. [ ] Nel cuore della rete

3. [ ] Sia ai confini che nel cuore della rete

<details><summary>risposta:</summary>
1
</details>

#### 💡 Nella commutazione di circuito, le risorse di rete sono
1. [ ] Condivise

2. [ ] Dedicate per i singoli utenti / flussi di dati
3. [ ] Dedicate solo nella parte di rete di accesso

<details><summary>risposta:</summary>
2
</details>

#### 💡 Tutti i link di una rete a commutazione di circuito hanno capacità pari a 480 kbps, e sono suddivisi in 15 slot/sec. tramite TDM. L'impostazione della chiamata richiede 200ms. Quanto tempo occorre per inviare un file di 320.000 bit dall'host A all'host B?
1. [ ] 1,2 sec.

2. [ ] 10 sec.
3. [ ] 10,2 sec.

<details><summary>risposta:</summary>
3
</details>

#### 💡 Se una rete a commutazione di pacchetto è sottoposta a basso carico, quale dei seguenti componenti del ritardo si può considerare trascurabile?
1. [ ] dproc

2. [ ] dprop
3. [ ] dqueue
4. [ ] dtrans

<details><summary>risposta:</summary>
3
</details>

#### 💡 Il throughput end-to-end è vincolato
1. [ ] dal collegamento con capacità maggiore

2. [ ] dal collegamento con capacità inferiore
3. [ ] dalla capacità media sul percorso

<details><summary>risposta:</summary>
2
</details>

#### 💡 Quale livello della pila TCP/IP fornisce la connessione tra processi applicativi?
1. [ ] Applicazione

2. [ ] Trasporto
3. [ ] Rete
4. [ ] Link

<details><summary>risposta:</summary>
2
</details>

#### 💡 Quale livello della pila TCP/IP fornisce l'instradamento dei pacchetti attraverso la rete?
1. [ ] Applicazione

2. [ ] Trasporto
3. [ ] Rete
4. [ ] Link

<details><summary>risposta:</summary>
3
</details>

#### 💡 La rete Internet si basa su
1. [ ] Commutazione di pacchetto a datagrammi

2. [ ] Commutazione di pacchetto a circuiti virtuali
3. [ ] Commutazione di circuito

<details><summary>risposta:</summary>
1
</details>

---

#### 📌 Definire un protocollo
definizione di regole di comunicazione, modalità e ordine per lo scambio di messaggi tra due o più entità in comunicazione

#### 📌 Si spieghi la differenza tra una rete a commutazione di circuito e una a commutazione di pacchetto
Nelle reti a commutazione di circuito si stabilisce un circuito dedicato per l'intera sessione, le risorse sono dedicate punto a punto, non sono condivise e si garantiscono prestazioni.
Nelle reti a commutazione di pacchetto non è necessario impostare una chiamata, ogni messaggio di una sessione usa le risorse su richiesta, c'è contesa delle risorse che sono condivise (multiplexing statistico)

#### 📌 Cos'è un'architettura protocollare "a strati"? TCP/IP è una architettura "a strati"?
Un arhitettura a strati basa il suo funzionamento su layer che utilizzano servizi forniti dai livelli inferiori, senza conoscerne l'implementazione ma usando interfacce fornite dai SAP e a loro volta svolgono operazioni internamente e forniscono servizi ai livelli superiori. TCP/IP è un arichitettura a strati composta da 4 livelli: Rete (1,2), Internet (3), Trasporto (4) e Applicazione (5,6,7)

#### 📌 Quali livelli protocollari implementa un Router in Internet?
Fisico, Collegamento, Rete

#### 📌 Qual'è la differenza tra la velocità di propagazione del segnale e la velocità di trasmissione dei dati?
La velocità di propagazione dipende dal mezzo fisico, il tempo di propagazione è il tempo necessario al segnale fisico per propagarsi lungo la linea di trasmissione fino al nodo successivo e da qui alla destinazione finale

La velocità di trasmissione (bit rate) è la quantità di dati che possono essere trasferiti su un canale di comunicazione in un dato intervallo di tempo, è dato da il rapporto tra lunghezza in byte del pacchetto e velocità o capacità di linea

#### 📌 Qual è l'unità dati (PDU) del livello fisico?
Bit o simbolo

#### 📌 Perché è uso comune chiamare "banda" la capacità trasmissiva di un canale (ma anche il throughput ottenuto da una rete)?

Il throughput è la frequenza al quale una certa unità dati viene trasmessa tra mittente e ricevente, vista anche come la quantità di dati spostati con successo da un luogo a un altro in un determinato periodo

La banda è una quantità di dati (bit) per unità di tempo (secondi), la stessa unità di misura del throughput. 

Sostanzialmente,il throughput viene chiamato banda e così anche la capacità, poiché alla fine quello che interessa sapere è quanti dati raggiungono effettivamente la destinazione

#### 📌 Cos'è invece in effetti la banda di un segnale? E di un canale trasmissivo?
La banda, è l'ampiezza spettrale di un segnale o di un canale trasmissivo.

#### 📌 Descrivere le principali differenze, in termini di caratteristiche e principi di funzionamento, fra reti locali (LAN) e geografiche (WAN)
Una LAN (Local Area Network) è una rete locale che copre un area limitata come un' abitazione, un azienda o un università

Una WAN (Wide Area Network) ha un estensione geografica più ampia, può connettere fra loro più reti locali e/o metropolitane collegate tra loro da backbone. Molte WAN sono costruite per una particolare organizzazione e sono private come ad esempio la rete GARR. La più grande WAN mai realizzata, Internet, una rete di computer che copre l'intero pianeta, è invece ad accesso pubblico. 
La funzionalità delle WAN è generalmente la connessione, in ambito commerciale, gli ISP di livello 1 sono i fornitori dotati di backbone proprietaria.

#### 📌 Spiegare le caratteristiche trasmissive delle fibre ottiche ed i motivi per cui sono i mezzi di supporto delle trasmissioni preferiti per le reti di dorsale con grande capacità trasmissiva
un cavo in fibra ottica è un cavo sottile e flessibile che conduce la luce, con un alta frequenza trasmissiva e un basso tasso di errore, per questo è il mezzo preferito per i collegamenti a lungo raggio 
