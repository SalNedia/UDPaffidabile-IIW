# UDPaffidabile- progetto IIW

### Manuale d'uso

Per eseguire i programmi del client e del server, dopo essersi
opportunamente spostati nella cartella, bisogna
effettuare i seguenti passi:
  1. Digitare a linea di comando make server e make client per creare gli eseguibili server_udp e client_udp;
  2. Digitare ./server_udp per eseguire il server e ./client_udp <server IP address> per eseguire il client, dove <server IP address> deve essere opportunamente sostituita dall’indirizzo IP del server;

### I parametri configurabili nei due programmi sono:

• Finestra di spedizione/ricezione: per modificarla è necessario entrare nel file basic.h e cambiare il valore della costante SLIDING_WNDW;

• Probabilità di perdita: modificare la costante failure_prob nel file basic.h;

• Timer fisso: per attivarlo bisogna porre la variabile is_dyn = 0 in client.c/server.c, la variabile timeout = 0 in timer.c dopodiché impostare la variabile timer_fisso al valore desiderato;

• Timer dinamico: per scegliere il timer adattativo è necessario porre, a differenza del precedente caso, la variabile is_dyn = 1 in
client.c/server.c, la variabile timeout in timer.c pari al valore desiderato e la variabile timer_fisso = 0 

### Per eseguire i comandi ammessi 
 -LIST: Digitare LIST e, dopo aver premuto Invio, verrà mostrata la lista dei file sul server.
 
 -PUT: Digitare PUT e premere Invio; o Successivamente digitare il nome del file di cui si vuole effettuare l’upload e premere Invio.
 
 -GET: Digitare GET e premere Invio; o Successivamente digitare il nome del file di cui si vuole effettuare il download e premere Invio.
 
 -END: Dopo aver digitato END e premuto invio, il client chiuderà la connessione col server.
