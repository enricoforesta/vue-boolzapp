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

1. Nel Js, ci creiamo una propietà dove inseriremo la stringa della barra di ricerca.

2. Creiamo una funzione, per filtrare le parole
---SE 
    il campo di testo per la ricerca è diverso da vuoto, filtriamo il contenuto e con ".includes" per controllare se la stringa è presente, poi usiamo ".map" cosi ci restituisce un array, con lo stesso contenuto del precedente, ma solo con i nomi presenti nella ricerca.
--- ALTRIMENTI 
    ritorna l 'array di oggetti iniziale.

3. Nel ciclo "v-for" che abbiamo usato per creare la chat, dobbiamo sostituire il ciclo che scorreva nell array iniziale, con il nostro nuovo Array filtrato. quindi passiamo direttamente la funzione.

# Milestone 5 

Cancella messaggio: cliccando sul messaggio appare un menu a tendina che permette di cancellare il messaggio selezionato.

Visualizzazione ora e ultimo messaggio inviato/ricevuto nella lista dei contatti.

1. riga 72 devo cambiare date: in modo che ci sia prima l orario e poi la data, e poi stampare solo le prime 5 stringhe.
