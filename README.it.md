# BoomCast

**Tutto quello che suona sul tuo PC Windows, sul tuo HomePod.** BoomCast manda l'audio del PC a HomePod e altri altoparlanti AirPlay 2 attraverso la rete di casa. Nessun driver da installare, nessun account, gratis.

*English: [README.md](README.md)*

> BoomCast è un progetto indipendente. Non è affiliato ad Apple, né approvato o sostenuto da Apple. AirPlay, HomePod, HomeKit e iPhone sono marchi di Apple Inc.

## Cosa fa

- **L'audio del PC sull'altoparlante.** Tutto quello che suona sull'uscita di Windows scelta (musica, video, giochi, chiamate) va agli altoparlanti che accendi. Più altoparlanti possono suonare insieme.
- **Ritardo basso.** Quattro modalità di ritardo, da *Istante* (0,15 s) per giochi e video a *Musica* (0,9 s) per il Wi-Fi debole, più uno slider libero.
- **Senza perdita.** 44,1 kHz / 16 bit, inviato in ALAC (pacchetti più piccoli, meno scatti sul Wi-Fi) oppure in PCM non compresso.
- **Regolazione del suono.** Equalizzatore a 10 bande, bassi, brillantezza, voce, larghezza stereo, surround, riverbero, compressore, limitatore. Nove modalità di serie; ogni modalità ricorda le tue modifiche, e puoi salvare le tue con il nome che vuoi e trascinarle nell'ordine che preferisci.
- **Misuratori dal vivo.** Spettro per banda, sinistra/destra, centro e lati.
- **Condivide l'altoparlante con il telefono.** Quando un iPhone inizia a suonare sull'HomePod, BoomCast si fa da parte. Quando il telefono smette (pausa o scollegamento) parte un conto alla rovescia e l'audio del PC torna da solo.
- **Non dà fastidio.** Vive nell'area di notifica, con un piccolo pannello per interruttori e volume; può partire con Windows.
- **28 lingue**, tema chiaro e scuro.

## Requisiti

- Windows 10 o 11 a 64 bit.
- Microsoft Edge WebView2 Runtime (fa già parte di Windows 11 e di Windows 10 aggiornato).
- Un HomePod, HomePod mini o altro altoparlante AirPlay 2 sulla **stessa rete** del PC.
- Nell'app **Casa** di Apple: *Impostazioni casa → Altoparlanti e TV → Consenti accesso → Chiunque sulla stessa rete*.

Sviluppato e provato con un HomePod (2ª generazione). Gli altri altoparlanti AirPlay 2 dovrebbero funzionare ma non sono stati provati.

## Download e primo avvio

1. Scarica `BoomCast.exe` dall'[ultima versione](https://github.com/Lorenzo8484/BoomCast/releases/latest). Non c'è niente da installare: metti il file dove vuoi e avvialo.
2. Il file non ha una firma digitale, quindi Windows mostra *"PC protetto da Windows"*. Scegli **Ulteriori informazioni → Esegui comunque**.
3. I tuoi altoparlanti compaiono in **Altoparlanti**. Accendine uno.
4. La prima volta il firewall di Windows deve lasciar arrivare a BoomCast le risposte dell'altoparlante: premi **Consenti nel firewall** quando l'app lo chiede e conferma la richiesta di Windows. Serve una volta sola.

Più dettagli, ogni impostazione spiegata e un elenco di soluzioni ai problemi: **[Guida](docs/guida.it.md)**.

## Da sapere

- **Scatti sul Wi-Fi.** Con un ritardo molto basso un pacchetto perso sul Wi-Fi non si recupera in tempo e si sente uno scatto. Se succede, alza il ritardo oppure tieni accesa la compressione ALAC.
- **Le traduzioni** sono automatiche e non sono state riviste da madrelingua. Il log è in italiano.
- **Privacy.** BoomCast parla solo con gli altoparlanti della tua rete locale. Non raccoglie niente e non manda niente su Internet. Le impostazioni restano sul tuo PC, in `%APPDATA%\BoomCast`.
- BoomCast usa AirPlay 2 senza il coinvolgimento di Apple, quindi un futuro aggiornamento del software dell'altoparlante può farlo smettere di funzionare finché BoomCast non viene aggiornato.

## Problemi e suggerimenti

Apri una [segnalazione](https://github.com/Lorenzo8484/BoomCast/issues). Indica che altoparlante hai, la versione di Windows, e allega il testo di *Impostazioni → Log*.

## Diritti e responsabilità

© 2026 Lorenzo. Tutti i diritti riservati. BoomCast è gratuito per uso personale; non può essere modificato, ridistribuito o venduto senza il permesso scritto dell'autore. È fornito "così com'è", senza garanzie di alcun tipo: lo usi a tuo rischio. Termini completi: [LICENSE.md](LICENSE.md).

Il codice sorgente non è pubblicato. BoomCast contiene librerie open source, elencate con le loro licenze in [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md).
