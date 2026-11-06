# Flusso Power Automate per email da Excel

Esercizio guidato su uno scenario di esempio (Contoso): un flusso cloud legge ogni giorno i contatti da una tabella Excel su OneDrive e invia a ciascuno un'email personalizzata.

## Struttura del flusso

1. **Ricorrenza:** si avvia una volta al giorno all'orario scelto.
2. **Elenca le righe presenti in una tabella (Excel Online):** legge `Tabella1` dal file su OneDrive.
3. **Applica a ciascuno:** ripete i passaggi per ogni riga.
4. **Invia un messaggio di posta elettronica:** usa come destinatario la colonna `E-mail` e inserisce il `Nome` nel testo.

<img width="405" height="592" alt="image" src="https://github.com/user-attachments/assets/2bb91646-fef4-4db4-a217-37dd15f4f795" />

## Provarlo

1. Carica `EsempioPA1.xlsx` su OneDrive. Contiene contatti fittizi: sostituiscili con indirizzi di test tuoi.
2. Ricrea il flusso seguendo i passaggi precedenti.
3. Avvialo da **Test → Manualmente** e controlla la ricezione dell'email.

## Limiti

- Scrive ogni giorno a **tutte** le righe, non solo ai nuovi contatti. Per evitare invii ripetuti servirebbe una colonna `Inviato` da filtrare e aggiornare dopo ogni email.
- Non gestisce gli errori di invio né la disiscrizione, necessari per un uso reale.
- Il repository documenta il flusso, ma non include il suo export.
