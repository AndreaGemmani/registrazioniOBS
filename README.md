# registrazioniOBS

### Cosa
Git di riferimento per consigli sulla registrazione delle Lezioni Online su Teams attraverso OBS.


### Come 
Gran parte delle Lezioni universitarie viene tenuta attraverso la piattaforma Microsoft Teams, software che permetterebbe la registrazione delle "riunioni" (videochiamate), tuttavia l'opzione è disabilitata per gli studenti; mentre buona parte dei professori si è dimostrata contraria a diffondere _personalmente_ il contenuto delle loro lezioni (non tutti ad ogni modo), molti sono favorevoli alle registrazioni in senso generale.


### Perché 
La necessità e la convenienza delle registrazioni delle Lezioni pare indubbia, soprattutto per chiunque abbia qualsivoglia difficoltà nel partecipare alle lezioni in real time. 


## Disclaimer 
**Questa guida vuole essere un aiuto per chiunque abbia volontà o necessità di registrare le Lezioni, non un incentivo ad un uso scorretto o illecito dei software e/o delle proprietà intellettuali del contenuto delle Lezioni. La condivisione delle registrazinoi rimanere a discapito di chi le produce e dei singoli professori oltre che alle singole Università, si consiglia quindi di accertarsi del consenso di tutte le parti in gioco prima di condividerle. Si ritiene inoltre necessario sottolineare che per Università non telematiche, la condivisione di materiale e proprietà intellettuali di proprietà delle Università _al di fuori del bacino di utenza delle singole Università (studenti, professori, tutor)_ è quasi sempre proibito.**


# Guida 
La guida fa riferimento alla versione più recente di Open Broadcast Software per Windows10 (v24.0.3 a marzo 2020)(e in minima parte nel TroubleShooting a v24.0.6 per MacOS).

### Quick Start
+ Innanzitutto scaricare il software [Open Broadcast Software dal sito](https://obsproject.com).

   Una volta scaricato ed installato, aprendo il software viene visualizzata una finestra simile alla seguente
   
   ![alt text](/cartellaScreen/init.jpg) 
   
   Se invece venisse visualizzato un riquadro nero ci si riferisca al TroubleShooting
   
+ Al primo avvio dovrebbero già essere presenti tutte le informazioni minime necessarie alla registrazione, fra cui
  * Una Scena
  * Una fonte di registrazione video
  * Una o più fonti di registrazione audio 
  * Pannello di controllo delle registrazioni
  
![alt text](/cartellaScreen/initRit.jpg) 



## Salvataggio registrazioni e conversione 
Per avviare una registrazione cliccare su Avvia registrazione nella parte in basso a destra della schermata di OBS o tramite shortcut (vedi più avanti). Una volta premuto la registrazione è in corso e il bottone diventerà Termina Registrazione. 

Una volta cliccato su Termina Registrazione questa verrà salvata in automatica in una cartella predefinita (normalmente la cartella Video) che può essere cambiata nelle impostazioni, per il salvataggio non viene richiesta conferma all'utente.

Si consiglia vivamente di **TOGLIERE IL PROPRIO MICROFONO dalla registrazione mutandolo** quando non lo si usa per fare interventi.

Le impostazioni predefinite di OBS consigliano di registrare in formato .mkv (è una sorta di ......), che è però scomodo per la condivisione e la visulizzazione soprattutto da browser (formato file non supportato per visualizzazione automatica), ma è tuttavia l'unico formato che preserva il salvataggio del file in caso di crash improvvisi (a me mai accaduti, però...),  quindi una volta fatto Termina Registrazione il file viene salvato in automatico e si può convertire semplicemente andando su File -> Converti le Registrazioni

![alt text](/cartellaScreen/convReg.png) 

Si apre una finestra, click sui tre puntini al centro (Sfoglia file), scegliete il file, fate Apri, poi Converti. 

![alt text](/cartellaScreen/finConv.png) 

Il processo dura sui 10s, potete cambiare nome e destinazione del file covertito, si consiglia di lasciare il nome dato da OBS.


  
## Impostazioni Consigliate per dimensioni file
Certamente una qualità audio e video ottima sarebbe sempre da preferirsi a qualità minori, tuttavia la dimensione dei file ne poterebbe risentire notevolmente, quindi in caso si pianifichi di mantenere a lungo le registrazioni che si accumulano e non avendo a disposizione uno storage infinito si consigliano impostazioni che mantengono la dimensione dei file nell'intorno dei 200-900MB per la lunghezza media di una lezione (da una a quattro ore). 
  * Qualità video: 1920x1080 scalata a 1280x720 (calcolando comunque eventuali bande ritagliate) a 30fps, scalatura bicubica
  * Qualità audio: 44.1KHz (impostazioni di base, non hanno grande influenza sulle dimensioni, salva con 160 di bitrate normalmente)
  * Qualità file: **Alta qualità, dimesione dei file medie**, salvata in .mkv poi convertita in .mp4 (sempre tramite OBS, vedi Conversione).

![alt text](/cartellaScreen/impVid.png) 

![alt text](/cartellaScreen/impUsc.png) 

## Ritagliare la parte di schermo da registrare
Per ritagliare e registrare una parte dello schermo andate sulla fonte video che volete modificare, click destro, vi comparirà un menù a tendina e selezionate Filtro.

Vi si aprirà una finestra da cui potete gestire i filtri attivi per la fonte video, aggiungerne quindi uno con il tasto "+" e selzionare un filtro di ritaglio. Nella selezione di ritaglio (soon...)

(screen(s) soon...)



### Creazione ShortCut
Può ritornare utile avere degli shortcut per avviare/terminare la registrazione, mettere in pausa / riprendere, cambiare scena o mutare, senza dover aprire la finestra di OBS. Per farlo basta andare su 
L'uso di questi shortcut funziona anche con OBS in background (non come scheda principale aperta), si consiglia comunque di evitare shortcut che possano attivare comandi anche su altri programmi aperti o shortcut di sistema (CTRL+ALT+CANC), quindi di controllare in anticipo.

![alt text](/cartellaScreen/short.png) 



## Consigli Vari
**TOGLIERE IL PROPRIO MICROFONO dalla registrazione mutandolo.**

Mettere in pausa durante le pause delle lezioni piuttosto che terminare la registrazione in modo da dover gestire molti meno file.

Togliere la visualizzazione del mouse nella selezione della fonte di registrazione video (c'è una checkbox da tickare).

Tenere la finestra di Teams a schermo intero, se possibile, per evitare di abbassare troppo la qualità video, nonostante la scalatura bicubica risolva in parte il problema.

Salvare in .mkv poi convertire in .mp4 una volta finite le registrazioni.

Cancellare i file .mkv dopo la conversione ma non prima di aver controllato che le conversioni .mp4 siano non corrotte.


## Editing e Compressione File
(soon...)




## TroubleShooting
### Schermo nero 
La principale causa dello schermo nero al posto della fonte di registrazione video è la gestione non adeguata delle molteplici fonti video causata ad esempio dalla compresenza di una scheda Grafica Integrata e di una dedicata (molto frequente nei pc). 

Per risolvere questo problema potrebbe essere necessario
  * **Installare driver grafici** che possono essere stati cancellati ad esempio in seguito ad un backup e ripristino del pc.
  * Agire sulle modalità di switch fra le schede grafiche per il risparmio energetico in **Impostazioni di sistema**.
  * Agire sulle **impostazioni** della scheda grafica dedicata, problematica ricorrente per **schede NVidia**.
(mancano ancora link a siti e video che risolvono questi problemi)

### Riverbero Audio
Se notate che un suono viene riverberato potreste avere uno o più microfoni aperti, probabilmente cuffie vicino al microfono esterno del pc, per disattivare l'audio di un'entrata potete ridurre a zero il relativo slider o disattivare direttamente cliccando sul simbolo della fonte sonora, o eliminarla. 


### Periferica Audio inesistente (MacOS)
#### (testato su OBS v24.0.6)
La versione per MacOS di OBS non permette da subito la registrazione audio desktop senza l'installazione di un driver apposito. Il software che sopperisce a questa mancanza è ["iShowU Audio Capture" scaricabile da qui](https://support.shinywhitebox.com/hc/en-us/articles/204161459-Installing-iShowU-Audio-Capture-Mojave-and-earlier-).

Una volta scaricato seguire i passaggi (linari ma che si trovano anche sul sito di dowload) di installazione che potrebbe venire bloccata in quanto lo sviluppatore non è certificato da Apple, andare quindi su Preferenze di Sistema -> Sicurezza e Privacy e cliccare in basso su "acconsenti". 

Finita l'installazione andare in Preferenze di Sistema -> Audio, e in "Uscita" selezionare la checkbox in basso "Mostra volume nella barra del Menù".

Cercare da Spotlight (cmd+SPACE) "Configuratore MIDI Audio" ed aprirlo; sulla sinistra avrete diversi canali fra cui iShowU Audio Capture, ma dovrete crearne un altro. Cliccate sul tasto "+" in basso e su "Crea dispositivo con uscite multiple", rinominatelo "OBS" cliccando sul nome (facoltativo ma utile per distinguerla facilmente), e selezionate **entrambe** le sucite audio: iShowU e Uscita Integrata.

Ora potrete scegliere quale uscita audio utilizzare, in due modi: 
   * Da Preferenze di Sistema -> Suono selezionare OBS (o l'altro nomoe lungo se non l'avete rinominata OBS) 
   * Dalla barra in alto del Mac cliccando sull'icona del suono dovrebbe comparire una tendina da cui selezionare OBS (o l'altro nomoe lungo se non l'avete rinominata OBS).
   
**Attenzione:** dall'uscita mixata non si può regolare più l'audio perché e una sorta di periferica virtuale!

Ora aprendo OBS potrete aggiungere l'uscita audio e tenendo l'uscita audio del Mac su "OBS" (o l'altro nomoe lungo se non l'avete rinominata OBS) potrete registrare l'audio desktop.

## Licensing 
Essendo questa solo una guida, non affiliata ad altri progetti, non si ritiene necessario l'uso di specifiche licenze, tuttavia si consiglia la lettura e la comprensione dei Disclaimer.


