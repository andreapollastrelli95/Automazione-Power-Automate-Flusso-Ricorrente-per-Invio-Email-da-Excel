Questo repository documenta la creazione di un flusso ricorrente in Microsoft Power Automate progettato per automatizzare l’invio quotidiano di email ai contatti registrati in un file Excel archiviato su OneDrive.
L’esercizio riproduce uno scenario aziendale in cui il team eventi di Contoso raccoglie i dati dei partecipanti e desidera inviare automaticamente informazioni aggiornate sull’evento.

🎯 Obiettivo del progetto
Realizzare un flusso cloud che:
recupera ogni giorno le righe di una tabella Excel contenente i contatti;
estrae per ogni riga l’indirizzo email e il nome del contatto;
genera e invia automaticamente un’email personalizzata;
elimina la necessità di inviare manualmente messaggi ai singoli interessati.

📂 Prerequisiti
Per eseguire correttamente il flusso è necessario:

un file Excel salvato su OneDrive:
una tabella formattata con le seguenti colonne:
Nome
Cognome
Contatto E-mail


Formattazione della tabella Excel
Selezionare l’intervallo contenente i dati.
Scheda Inserisci → Tabella.
Assicurarsi che l’opzione Tabella con intestazioni sia attiva.
Salvare il file su OneDrive.

⚙️ Struttura del flusso
Il flusso è composto dai seguenti elementi principali:

1. Trigger – Ricorrenza
Frequenza: Giornaliera
Orario di esecuzione: configurabile (es. 10:00)

2. Azione – Elenca le righe presenti in una tabella (Excel Online)
Posizione: OneDrive

File: selezione del file Excel creato
Tabella: es. Table1

3. Azione – For Each
Itera su ogni riga della tabella Excel.

4. Azione – Invia un messaggio di posta elettronica
Per ogni contatto:
A: valore dinamico Contatto E-mail
Oggetto: Informazioni Evento Contoso
Corpo: email personalizzata con Nome e testo informativo sull’evento

📬 Risultato finale
Una volta attivato, il flusso:

si esegue automaticamente ogni giorno;
legge i nuovi contatti aggiunti al file Excel;
invia un’email personalizzata a ciascun indirizzo;
semplifica la gestione delle comunicazioni per il team eventi.

▶️ Test del flusso
Il flusso può essere testato manualmente tramite:

Test → Manualmente
Esegui flusso

Verifica dell’esecuzione tramite indicatori verdi e ricezione dell’email.
<img width="405" height="592" alt="image" src="https://github.com/user-attachments/assets/2bb91646-fef4-4db4-a217-37dd15f4f795" />

