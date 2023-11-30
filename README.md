# Milestone 1

Replica della grafica con la possibilità di avere messaggi scritti dall’utente (verdi) e dall’interlocutore (bianco) assegnando due classi CSS diverse

Visualizzazione dinamica della lista contatti: tramite la direttiva v-for, visualizzare nome e immagine di ogni contatto

# Logica

1. Strutturare Html. Iniziamo sempre da fuori a dentro, quidni prima i contenitori e poi i contenuti. ci possiamo aiutare con qualche classe di Debug per dare altezze e colori.


# Milestone 2

Visualizzazione dinamica dei messaggi: tramite la direttiva v-for, visualizzare tutti i messaggi relativi al contatto attivo all’interno del pannello della conversazione.

Click sul contatto mostra la conversazione del contatto cliccato

# Logica

1. Nell html, Aggiungiamo un ciclo for, dove scorriamo l'Array di contatti, fino ad arrivare ai messaggi. Nella stessa riga aggiungiamo una classe in base al valore di status usando un operatore ternario.

2. Nella sezione delle chat, Aggiungiamo un evento click sui <li>, richiamiamo una funzione  dove "i" che abbiamo passato come argomento è === a "indexCurrent".


# Milestone 3

Aggiunta di un messaggio: l’utente scrive un testo nella parte bassa e digitando “enter” il testo viene aggiunto al thread sopra, come messaggio verde.

Risposta dall’interlocutore: ad ogni inserimento di un messaggio, l’utente riceverà un “ok” come risposta, che apparirà dopo 1 secondo.

# Logica 

1. Nel Js creiamo un propietà vuota, dove questa grazie al v-model sarà collegata all input di testo per inviare il mesaggio. 

2. Nella stessa riga aggiugiamo un "keyup.enter", e richiamiamo la funzione "sendText", dove pushiamo un oggetto, che ha come messaggio input inserito, e status "sent", cosi verrà visualizzato come messaggio inviato.

3. Nella stessa funzione, aggiungiamo un "setTimout" in modo che ogni volta che inviamo un messaggio, ci risponde automaticamente dopo un intervallo.

# Milestone 4

Ricerca utenti: scrivendo qualcosa nell’input a sinistra, vengono visualizzati solo i contatti il cui nome contiene le lettere inserite (es, Marco, Matteo Martina -> Scrivo “mar” rimangono solo Marco e Martina)

# Logica