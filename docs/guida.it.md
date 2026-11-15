# Guida di BoomCast

*English: [guide.md](guide.md)*

## Prima di cominciare

1. PC e altoparlante devono essere sulla stessa rete di casa.
2. Nell'app **Casa** di Apple apri *Impostazioni casa → Altoparlanti e TV* e in *Consenti accesso* scegli **Chiunque sulla stessa rete**. Senza questo l'altoparlante rifiuta il collegamento.
3. Avvia `BoomCast.exe`. Se Windows mostra "PC protetto da Windows", scegli *Ulteriori informazioni → Esegui comunque*: succede perché il file non ha una firma digitale.

## Altoparlanti

Ogni altoparlante trovato in rete ha la sua scheda.

- **Interruttore in alto a destra:** inizia o ferma la trasmissione su quell'altoparlante.
- **Volume:** vale solo per quell'altoparlante. Il *Volume generale* nella colonna sinistra li scala tutti insieme.
- **Ritardo extra:** aggiunge ritardo a quel solo altoparlante, per allinearlo ad altri o all'immagine di un video.
- **Riconnessione automatica:** se un telefono prende l'altoparlante, BoomCast si fa da parte e torna da solo quando il telefono ha finito. Vale anche se cade la connessione. Spenta: resta scollegato finché non lo riaccendi tu.
- **Attesa per ricollegarsi:** quanti secondi senza audio dal telefono devono passare prima che BoomCast torni a trasmettere (da 5 secondi a 5 minuti, 30 di partenza). Mentre aspetta, accanto al nome compare il conto alla rovescia.

In alto, **Ferma tutto** scollega tutti gli altoparlanti.

## Suono

- **Interruttore "Miglioramenti audio":** spento, il suono passa senza modifiche.
- **Modalità:** nove di serie (Neutro, Bassi+, Voce, Film, Musica, Notte, Gioco, Spaziale, Concerto) più le tue. *Neutro* è il suono normale, con tutto a zero.
- **Ogni modalità ricorda le tue modifiche.** Se sposti uno slider mentre una modalità è attiva, la modifica resta sua, anche dopo il riavvio; un puntino arancione segna le modalità modificate. **Azzera** riporta la modalità attiva alla sua regolazione di base e non tocca le altre.
- **Salva impostazioni audio…** salva tutto quello che c'è nella pagina con il nome che vuoi. Crea sempre una modalità nuova; se il nome esiste già aggiunge un numero. La × su una modalità tua la elimina.
- **Riordinare:** tieni premuta una modalità e trascinala dove vuoi.
- **Equalizzatore:** dieci bande da 31 Hz a 16 kHz, più la preamplificazione (*Pre*). Abbassa *Pre* se alzi molto le bande, per evitare distorsione. Un doppio clic su uno slider lo riporta al valore neutro.
- **Suono spaziale:** larghezza stereo, surround, riverbero, dimensione della stanza, fusione dei canali, bilanciamento.
- **Dinamica:** compressione, volume uniforme, limitatore, dithering.

Le barre in alto mostrano il livello per banda; ai lati dell'equalizzatore ci sono canale sinistro, centro, lati e canale destro.

## Impostazioni

- **Avvio:** avvio con Windows, chiusura nell'area di notifica (la X nasconde la finestra e l'audio continua), lingua. *Auto* usa la lingua di Windows, o l'inglese se non è disponibile.
- **Audio da trasmettere:** l'uscita di Windows da catturare. *Predefinita* segue quella che scegli in Windows.
- **Ritardo:** quanto l'altoparlante aspetta prima di suonare. Più basso è più reattivo; più alto regge meglio un Wi-Fi debole.
- **Trasmissione:**
  - *Solo HomePod* silenzia le casse del PC mentre trasmette.
  - *Compressione ALAC* rimpicciolisce i pacchetti senza perdere qualità, e riduce gli scatti sul Wi-Fi. Spenta, si usa PCM non compresso.
  - *Buffer PC* è una piccola riserva di audio sul PC: alzalo se nel log compaiono "buchi".
- **Firewall:** stato del permesso e pulsante per concederlo.
- **Aggiungi per indirizzo IP:** per altoparlanti che la ricerca automatica non trova.
- **Log:** quello che l'app ha fatto, utile per capire un problema.

## Area di notifica

L'icona resta accanto all'orologio. Clic sinistro: apre la finestra. Clic destro: apre un pannello con gli altoparlanti (interruttore e volume), le impostazioni e l'uscita dall'app.

## Problemi comuni

| Cosa succede | Cosa fare |
|---|---|
| Nessun altoparlante trovato | Controlla che PC e altoparlante siano sulla stessa rete e che nell'app Casa l'accesso sia su "Chiunque sulla stessa rete". Su reti con più punti di accesso o con isolamento dei dispositivi la ricerca può fallire: usa *Aggiungi per indirizzo IP*. |
| "Bloccato dal firewall di Windows" | Premi *Consenti nel firewall* e conferma la richiesta di Windows. Se hai spostato o rinominato il file, il permesso va dato di nuovo. |
| Il collegamento viene rifiutato | Quasi sempre è l'impostazione di accesso nell'app Casa. Un altoparlante protetto da password o codice non è supportato. |
| Si sente a scatti | Tieni accesa la compressione ALAC e alza il ritardo (*Video* o *Musica*). Gli scatti vengono dalla rete Wi-Fi dell'altoparlante: avvicinarlo al router o usare un canale meno affollato aiuta. |
| L'audio è in ritardo rispetto al video | Abbassa il ritardo, oppure ritarda il video nel lettore dello stesso valore. |
| Dopo l'iPhone il PC non torna | Controlla che *Riconnessione automatica* sia accesa su quell'altoparlante e guarda il conto alla rovescia. Parte solo quando il telefono non manda più audio. |
| Suono distorto | Abbassa *Pre* nell'equalizzatore e tieni acceso il limitatore. |

Se non si risolve, apri una segnalazione nella sezione **Issues** allegando il testo del Log.

## Dove stanno i dati

BoomCast è un file solo e non installa niente. Tutto quello che scrive finisce in una cartella del tuo utente Windows:

`%APPDATA%\BoomCast` — cioè `C:\Users\<il tuo nome>\AppData\Roaming\BoomCast`. Per aprirla premi Win+R, scrivi `%APPDATA%\BoomCast` e premi Invio. Ogni utente Windows del PC ha la sua.

| File o cartella | Cosa contiene |
|---|---|
| `settings.json` | Tutte le impostazioni: altoparlanti accesi, loro volume, ritardo extra e opzioni per il telefono, il ritardo, l'uscita audio, le tue modalità audio, le modifiche fatte a ogni modalità, il loro ordine, lingua, tema, grandezza della finestra. Viene scritto a ogni modifica. |
| `boomcast.log` | Il registro che vedi in *Impostazioni → Log*. Si accorcia da solo quando supera 1 MB. |
| `webview` (cartella) | File di lavoro del componente di Windows che disegna l'interfaccia (cache). Si può eliminare a BoomCast chiusa. |
| `debug.log`, `probe.log` | Presenti solo se sono state fatte prove di diagnosi. |

Fuori da quella cartella BoomCast lascia due cose, entrambe create solo quando le chiedi tu:

- **Avvia con Windows** aggiunge il valore `BoomCast` nella chiave di registro `HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Run`. Spegnendo l'opzione viene tolto.
- **Consenti nel firewall** aggiunge al firewall di Windows una regola in ingresso chiamata `BoomCast` per l'eseguibile. Si toglie da *Sicurezza di Windows → Firewall → Impostazioni avanzate → Regole connessioni in entrata*.

Niente viene salvato online, e dal PC non esce niente tranne l'audio mandato ai tuoi altoparlanti.

- **Copia di sicurezza o passaggio a un altro PC:** copia `settings.json` nella stessa cartella dell'altro PC.
- **Ripartire da zero:** chiudi BoomCast ed elimina la cartella.
- **Rimuovere BoomCast:** spegni *Avvia con Windows*, chiudila, elimina `BoomCast.exe` e la cartella; togli la regola del firewall se l'avevi aggiunta.
