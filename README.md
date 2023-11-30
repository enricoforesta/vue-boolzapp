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
