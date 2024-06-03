Configurazione di DNS Risolutivo con INetSim
Questo progetto descrive i passaggi per configurare un DNS risolutivo utilizzando INetSim, permettendo l'accesso a un dominio interno tramite browser su una macchina con Windows 7.

Descrizione del Progetto
Per questo esercizio, è stata configurata una rete di test in cui un server DNS risolve il dominio epicode.internal utilizzando INetSim. Il progetto include anche la configurazione necessaria per permettere l'accesso al dominio sia tramite protocollo HTTP che HTTPS.

Passaggi per la Configurazione
Assegnazione IP Statico:

Assegnare un IP statico alle macchine coinvolte.
Configurare Windows 7 per utilizzare il server DNS creato su INetSim.
Configurazione di INetSim:

Eseguire sulla Bash di Kali il comando sudo nano -c /etc/inetsim/inetsim.conf.
Aggiungere la riga dns_static epicode.internal 192.168.32.100 nel file di configurazione.
Avvio di INetSim:

Avviare INetSim con il comando sudo inetsim --bind-address 0.0.0.0.
Controllo delle Connessioni:

Utilizzare Wireshark per monitorare il traffico HTTP e HTTPS.
Requisiti
Kali Linux: Versione 2021.3 o precedente compatibile con INetSim.
Windows 7: Configurato per utilizzare il server DNS di INetSim.
INetSim: Configurato per risolvere il dominio epicode.internal.
Note
È importante considerare le implicazioni di sicurezza quando si configura INetSim per ascoltare su tutte le interfacce di rete.
Le versioni più recenti di Kali Linux potrebbero non essere compatibili con INetSim a causa di aggiornamenti nei pacchetti di sistema.
Immagini Dimostrative
Assegnazione IP Statico

Configurazione di INetSim

Comando di avvio di INetSim

Controllo delle connessioni con Wireshark
