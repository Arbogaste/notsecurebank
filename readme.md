Istruzioni:
• Per ogni vulnerabilità fixata creare un singolo commit.
• Il nome del commit dovrà essere nel seguente formato:
“Fix <NumeroVulnerabilità>_<Tipologia>”
• Facoltativo: ri-buildare e ri-deployare l’applicazione per verificare l’effettivo
fix delle vulnerabilità. Le istruzioni per effettuare questo step sono riportate
alla fine di questo documento.
4. Allo scadere delle 4 ore o al termine della giornata, compilare il form al
seguente link:
https://forms.office.com/e/trFUP2pba9

build & deploy

Requirements:
• Gradle (Gradle 8.1.1)
• Java 11
All’interno del file build.gradle, necessario per effettuare la build, è già presente
un’istruzione che forza l’utilizzo di Java 11.

gradle war

Il file war si troverà nella cartella “build”. Il file build.gradle si dovrà trovare allo
stesso livello della cartella src.
Deploy dell’applicazione (da eseguire sulla macchina virtuale NotSecureBank)
Sostituire il war precedente contenuto in /opt/tomcat/webapps con il file war
appena generato.
Per fare ciò è consigliato accedere alla cartella attraverso il comando

sudo xdg-open ./

Potrebbe essere necessario riavviare tomcat: a tal fine si lancino gli script
shutdown.sh e startup.sh presenti all’interno della cartella /opt/tomcat/bin
(tra un comando e l’altro attendere qualche istante affinchè tomcat venga
realmente chiuso)
