# registrazioniOBS

### Cosa
Git di riferimento per consigli sulla registrazione delle Lezioni Online su Teams attraverso OBS.

### Perché 
La necessità e la convenienza delle registrazioni delle Lezioni pare indubbia, soprattutto per chiunque abbia qualsivoglia difficoltà nel partecipare alle lezioni in real time. 

### Come 
Le lezioni vengono tenute su Microsoft Teams, software che permetterebbe la registrazione delle "riunioni" (videochiamate), tuttavia l'opzione è disabilitata per gli studenti, mentre buona parte dei professori si è dimostrata contraria a diffondere personalmente il contenuto delle lezioni (non tutti ad ogni modo), ma non alle registrazioni in senso generale.



## Disclaimer 
**Questa guida vuole essere un aiuto per chiunque abbia volontà o necessità di registrare le Lezioni, non un incentivo ad un uso scorretto o illecito dei software e/o delle proprietà intellettuali del contenuto delle Lezioni. La condivisione delle registrazinoi rimanere a discapito di chi le produce e dei singoli professori oltre che alle singole Università, si consiglia quindi di accertarsi del consenso di tutte le parti in gioco prima di condividerle. Si ritiene inoltre necessario sottolineare che per Università non telematiche, la condivisione _al di fuori del bacino di utenza delle singole Università_ è quasi sempre proibito.**


# Guida 
La guida fa riferimento alla versione più recente di Open Broadcast Software per Windows10 (v24.0.3 a marzo 2020).

### Quick Start
+ Innanzitutto scaricare il software [Open Broadcast Software dal sito](https://obsproject.com).

   Una volta scaricato ed installato, aprendo il software viene visualizzata una finestra simile alla seguente
   
   ![alt text](/cartellaScreen/init.jpg) 
   
   Se invece venisse visualizzato un riquadro nero ci si riferisca la TroubleShooting
   
+ Al primo avvio dovrebbero già essere presenti tutte le informazioni minime necessarie alla registrazione, fra cui
  * Una Scena
  * Una fonte di registrazione video
  * Una o più fonti di registrazione audio 
  * Pannello di controllo delle registrazioni
  
![alt text](/cartellaScreen/init.jpg) 



## Salvataggio registrazioni e conversione 
Per avviare una registrazione cliccare su Avvia registrazione nella parte in basso a destra della schermata di OBS o tramite shortcut (vedi più avanti). Una volta premuto la registrazione è in corso e il bottone diventerà Termina Registrazione. 

Una volta cliccato su Termina Registrazione questa verrà salvata in automatica in una cartella predefinita (normalmente la cartella Video) che può essere cambiata nelle impostazioni, per il salvataggio non viene richiesta conferma all'utente.

Si consiglia vivamente di **TOGLIERE IL PROPRIO MICROFONO dalla registrazione mutandolo** quando non li usa per fare interventi.

Le impostazioni predefinite di OBS consigliano di registrare in formato .mkv (è una sorta di ......), che è però scomodo per la condivisione e la visulizzazione soprattutto da browser (formato file non supportato per visualizzazione automatica), ma è tuttavia l'unico formato che preserva il salvataggio del file in caso di crash improvvisi (a me mai accaduti, però...),  quindi una volta fatto Termina Registrazione il file viene salvato in automatico e si può convertire semplicemente andando su File -> Converti le Registrazioni

![alt text](/cartellaScreen/convReg.png) 

Si apre una finestra, click sui tre puntini al centro (Sfoglia file), scegliete il file, fate Apri, poi Converti. 

![alt text](/cartellaScreen/finConv.png) 

Il processo dura sui 10s, potete cambiare nome e destinazione del file covertito, si consiglia di lasciare il nome dato da OBS.


  
## Impostazioni Consigliate per dimensioni file
Certamente una qualità audio e video ottima sarebbe sempre da preferirsi a qualità minori, tuttavia la dimensione dei file ne poterebbe risentire notevolmente, quindi in caso si pianifichi di mantenere a lungo le registrazioni che si accumulano e non avendo a disposizione uno storage infinito si consigliano impostazioni che mantengono la dimensione dei file nell'intorno dei 300-900MB per una lezione che va da una a quattro ore. 
  * Qualità video: 1920x1080 scalata a 1280x720 (calcolando comunque eventuali bande ritagliate) a 30fps, scalatura bicubica
  * Qualità audio: 44.1KHz (impostazioni di base, non hanno grande influenza sulle dimensioni, salva con 160 di bitrate normalmente)
  * Qualità file: **Alta qualità, dimesione dei file medie**, salvata in .mkv poi convertita in .mp4 (sempre tramite OBS, vedi Conversione).

![alt text](/cartellaScreen/impVid.png) 

![alt text](/cartellaScreen/impUsc.png) 

## Ritagliare la parte di schermo da registrare
Per avere un'immagine (.........)



### Creazione ShortCut
Può ritornare utile avere degli shortcut per avviare/terminare la registrazione, mettere in pausa / riprendere, cambiare scena o mutare, senza dover aprire la finestra di OBS. Per farlo basta andare su 
L'uso di questi shortcut funziona anche con OBS in background (non come scheda principale aperta), si consiglia comunque di evitare shortcut che possano attivare comandi anche su altri programmi aperti o shortcut di sistema (CTRL+ALT+CANC), quindi di controllare in anticipo.

![alt text](/cartellaScreen/short.png) 



## Consigli Vari
**TOGLIERE IL PROPRIO MICROFONO dalla registrazione mutandolo.**

Mettere in pausa durante le pause delle lezioni piuttosto che terminare la registrazione in modo da dover gestire molti meno file.

Salvare in .mkv poi convertire in .mp4 una volta finite le registrazioni

Cancellare i file .mkv dopo la conversione ma non prima di aver controllato che le conversioni .mp4 siano non corrotte.




## TroubleShooting
### Schermo nero 
La principale causa dello schermo nero al posto della fonte di registrazione video è la gestione non adeguata delle molteplici fonti video causata ad esempio dalla compresenza di una scheda Grafica Integrata e di una dedicata (molto frequente nei pc). 

Per risolvere questo problema potrebbe essere necessario
  * **Installare driver grafici** che possono essere stati cancellati ad esempio in seguito ad un backup e ripristino del pc.
  * Agire sulle modalità di switch fra le schede grafiche generico in **Impostazioni di sistema**.
  * Agire sulle **impostazioni** della scheda grafica dedicata problematica ricorrente per **schede NVidia**.


## Licensing 
Essendo questa solo una guida, non affiliata ad altri progetti, non si ritiene necessario l'uso di specifiche licenze, tuttavia si consiglia la lettura e la comprensione dei Disclaimer.



