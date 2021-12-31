Slido 💻
#### 💡 Perché una cache web è utile?
1. [ ] Perché ospita tutte le componenti di una pagina web e le fornisce localmente a chi ne fa richiesta

2. [ ] Perché controlla automaticamente se una pagina web è cambiata: se non lo e, fornisce la copia locale invece di quella remota
3. [ ] Perché scarica il link di accesso fornendo localmente i contenuti statici
4. [ ] Perché scarica i contenuti dal web usando un link separato da quello di tutti gli altri host

<details><summary>risposte:</summary>
2 - 3
</details>

#### 💡 Che differenze ci sono tra le connessioni persistenti e quelle non persistenti in HTTP 1.0 e 1.11?
1. [ ] Con connessioni persistenti, si usa una sola connessione per chiedere uno dopo l'altro tutti gli oggetti al server, e la si distrugge subito dopo
2. [ ] Con connessioni NON persistenti, si usa una sola connessione per tutti gli oggeti da richiedere al server, e la si distrugge subito dopo 
3. [ ] Con connessioni NON persistenti, si attivano N connessioni in parallelo, una per ciascun oggetto da richiedere al server, e le si distrugge subito dopo

4. [ ] Con connessioni persistenti, si usa una sola connessione per chiedere contemporaneamente tutti gli oggetti al server, e la si distrugge subito dopo 

<details><summary>risposta:</summary>
1
</details>



#### 💡 Quali tra queste funzionalità NON è introdotta da HTTP 2?
1. [ ] Connessioni TCP persistenti
2. [ ] Controllo di errore a livello applicazione nella comunicazione con il client
3. [ ] Servizi di sicurezza nell'instaurazione della sessione (TLS)

4. [ ] Stream paralleli di dati e priorità degli stessi
5. [ ] Server push, per cui il server invia al client dati non ancora esplicitamente richiesti

<details><summary>risposta:</summary>
2
</details>

#### 💡 Per quale ragione, principalmente, un utente non usa il prot SMTP per leggere la posta elettronica?
1. [ ] Perché il server dell'utente dovrebbe essere sempre attivo per ricevere i messaggi che gli vengono inviati
2. [ ] Perché questo cancellerebbe i messaggi dal server di posta
3. [ ] Perché SMTP non consente di ricevere posta da altri server

4. [ ] Perché SMTP funziona solo tra server

<details><summary>risposta:</summary>
1
</details>

#### 💡 Perché si usa la codifica base64 nella trasmissione di allegati di messaggi email?
1. [ ] Perché questo permette di rappresentare ogni 6 bit usano un byte, assicurandosi quindi che l'informazione venga rappresentata solo tramite lettere maiuscole e minuscole, numeri e pochi catatteri speciali
2. [ ] Per retrocompatibilità con i sistemi più datati di trasmissione email, che funzionavano solo con messaggi testuali
3. [ ] Perché si tratta di uno schema di compressione molto efficiente che riduce la dimensione dei messaggi inviati

4. [ ] Per aiutare l'utente, rendedo intellegibile anche gli allegati nel testo di un messaggio

<details><summary>risposte:</summary> 
1 - 2
</details>

#### 💡 Che differenza c'è tra una query DNS ricorsiva e una iterativa?
1. [ ] Quella ricorsiva prevede che l'host richiedente deleghi il server DNS locale, che, a catena, delega tutti i server incontrati percorrendo la gerarchia DNS fino a quello autoritativo del dominio cercato
2. [ ] Quella iterativa delega il recupero delle informazione a un server DNS locale
3. [ ] Quella ricorsiva delega il recupero delle informazioni a un server DNS locale

4. [ ] Quella ricorsiva prevede che l'host richiedente interroghi uno per uno tutti i server nella gerarchia DNS fino a quello autoritativo del dominio cercato

<details><summary>risposte:</summary>
1 - 3
</details>

#### 💡 Cosa si intende per query flooding?
1. [ ]  Nel contesto di una distributed hash table è l'inoltro di una query ai peer in una rete di copertura
2. [ ] E' un processo usato da Bit torrent per recuperare frammenti dei file da scaricare
3. [ ] Nel contesto di un app. client/server è l'inoltro di una query a molteplici server

4. [ ] E' il sistema con cui un browser richiede in parallelo tutti i componenti di una pagina web scaricata

<details><summary>risposta:</summary>
1
</details>

#### 💡 Perché la distribuzione di file in modalità peer-to-peer può essere conveniente?
1. [ ] Perché risolve il problema del collo di bottigli sul link di upload del client
2. [ ] Perché permette a più host di collaborare all'upload di file
3. [ ] Perché non richiede al server di inviare N copie del file, una per ogni host
4. [ ] Perché risolve il problema del collo di bottiglia sul link di download dei client

5. [ ] Perché risolve il problema del collo di bottiglia sul link di upload del server

<details><summary>risposte:</summary>
2 - 3 - 5
</details>

####
---

Domande Esami 🗂

#### 📌 1. Spiegare cosa sono le socket, qual'è il relativo layer ISO/OSI motivando la risposta
Una socket è una porta di comunicazione utilizzata per identificare un processo di un host. Sono utilizzati dal protocollo IP per indirizzare correttamente i dati tramite protocollo di trasporto (TCP/UDP).

Fanno riferimento al livello Applicazione e al livello di Trasporto: ogni applicazione comunica con processi che sono trasportati con comunicazione ad esempio TCP uscendo da una socket di un host sorgente e arrivando alla socket di un host destinazione. 

#### 📌 2. Descrivere il protocollo SMTP e le principali componenti architetturali utilizzate nella posta elettronica e il suo funzionamento.
Per la posta elettronica ci sono 3 componenti architetturali principali, *agente utente* che permette a un utente di editare, visualizzare e comporre un messaggio, *server di posta* che contiene tutti i messaggi in una coda. 
I server di posta comunicano attraverso il protocollo SMTP (Simple Mail Transmition Protocol ) che mette in comunicazione server posta mittente e destinatario (si noti che in questo modo il server di posta mittente diventa client).

Utilizza il protocollo TCP sulla porta 25 da server a server, con tre
fasi di trasferimento: handshaking, trasferimento dei messaggi e chiusura.  connessioni persistenti, messaggi in formato ASCII

Si noti la necessità di avere anche un protocollo di accesso alla porta per permettere al cliente di scaricare i messaggi dal server di posta (esempi sono POP3 (scaricare e mantenere i propri messaggi sul client e sul server, stateless, no sincronizzazione) e IMAP (statefull, avanzato, organizzazione dei messaggi e sincronizzazione))

#### 📌 3. Spiegare l’organizzazione dei nomi nel DNS e la differenza di significato dei termini “zona” e “dominio"
DNS (Domain Name System) prevede la traduzione di hostname in indirizzi di rete, l'aliasing di hostname o di posta.
Un nome di dominio è per esempio *godaddy.com*, si noti che la parte più importante è quella a destra cioè ".com" il dominio di primo livello o Top Level Domain (TLD) mentre il dominio di secondo livello è "godaddy.com" e così via per le altre eventuali divisioni.

DNS è un sistema gerarchico diviso in zone, i domini di primo livello formano la zona radice DNS, abbiamo poi le zone dei domini di secondo livello e inferiori.

Fanno poi parte della gerarchia dei DNS i server di competenza (authoriative server)

E ci sono poi i server dns locali


#### 📌 4. Spiegare le principali funzioni messe a disposizione dal linguaggio C per implementare un server TCP
(non parte dell'esame)

- `socket` per creare una socket
- `bind` per associarsi a una porta
- `listen` per ascoltare una porta
- `accept` peraccettare una connessione
- `send` per trasmettere dati
- `recv` per ricevere dati



