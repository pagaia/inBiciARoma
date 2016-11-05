
Use:

Questo bot esegue query su un documento di gdrive dove sono caricate alcune informazioni georeferenziate
Cliccando su KEYWORDS si ha il numero di informazioni raggruppate per una parola chiave. Al momento esistono sono i kit di pronto soccorso per le bici.
Cliccnado su kit, si ottiene la lista di luogi che offrono un kit di pronto soccorso per la bici
Inviando la propria posizione, e poi la parola da ricercare, i risultati che si ottengono includeranno anche la distanza con la posizione inviata
Infine puoi fare una ricerca per parola chiave anteponendo il carattere ? tipo ?bar.

Lic. MIT @pagaia

Config:
In localhost is possible to launch
php start.php 'sethook' per impostare start.php come webhook (inserire https il link per start.php)
php start.php 'sethook' 'cert' per impostare start.php come webhook (inserire https il link per start.php) ed inviare il proprio certificato self-signed
php start.php 'removehook' per rimuovere start.php come webhook
php start.php 'getupdates' per eseguire manualmente getupdates.php (se non hai https puoi settare un crontab ogni minuto che esegue questa istruzione)

Installazione libreria mongoDB
Nella cartella lib devi installare la libreria MongoDB per php usando questa procedura https://docs.mongodb.com/php-library/master/

Configurazione del file sheet su GoogleDrive
Devi compilare un file sheet su GoogleDrive e compilare il file settings_t.php.

1) cerca su Telegram l'utente botfather e fai /newbot per creare un nuovo bot. scelto il nome ti verrà indicata l'API key riservata da inserire in settings_t.php
2) apri questo file e fai "crea una copia" https://goo.gl/oaSmdh ogni documento gdrive ha una propria key che è quel codice lungo nell'url tra https://docs.google.com/spreadsheets/d/ e edit#gid=. Incollare questa key nel file settings.php nel campo GDRIVEKEY 
3) compila il primo foglio di calcolo che ho chiamato faq. segnati il valore numerico che hai dopo gid= nell'url e inseriscilo in settings_t.php come GDRIVEGID1
4) compila il secondo foglio di calcolo che ho chiamato risposte. segnati il valore numerico che hai dopo gid= nell'url e inseriscilo in settings_t.php come GDRIVEGID2. Gli ID delle risposte devono corrispondere alla relativa domanda nel foglio faq
5) compila il terzo foglio di calcolo che ho chiamato sedi. segnati il valore numerico che hai dopo gid= nell'url e inseriscilo in settings_t.php come GDRIVEGID3. le coordinate devi incollarle anteponendo il carattere ' esempio '40.123456 cosi "avvisi" google che è un campo testo
6) logo.png aggiorna il logo della tua azienda/sindacato

In sintesi crei un bot da botfather, compili foglio google con domande risposte e faq, compili il file settings_t.php e poi o lanci manualmente php start.php 'getupdates' (o tramite crontab) oppure attivi https e inserisci il link del file start.php nel file settings_t.php (esempio https://www.nomesito/tuobot/start.php)




Buona fortuna
