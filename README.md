# Progetto_forma_temp
Simulazione sito web universitario

Competenze utilizzate:
	- servlet con metodi GET e POST in Java per back-end
	- HTML e Css per front-end
	- mySQL workbench per creazione del DB


Struttura DB

	- 4 tabelle: professore, studente, prenotazione, corso, appello
	- professore: idProfessore(chiave primaria), username, password, tipo_utente, nome, cognome
	- studente: Matricola(chiave primaria), username, password, tipo_utente, nome, cognome
	- corso: idCorso, materia, cattedra
	- appello: idAppello, Data, materia
	- prenotazione: idpren, stud_prenotato, app_prenotato
  
  
Funzionalità:

	-utenti possono registrarsi come professori e studenti
	-controlli vari se campi non sono compilati correttamente/ dati gia presenti nel db
	-studenti possono prenotare un esame negli appelli disponibili dell'esame scelto in precedenza
	-professori possono controllare studenti prenotati
	-nel dettaglio:
		- servlet prenotazione permette con metodo post di accedere a seconda del corso scelto agli appelli
		- servlet prenota permette con metodo post allo studente di prenotare l'appello e salvare la sua prenotazione attraverso la sua matricola nella tabella prenotazione del db
		- servlet StampaStudenti permette con metodo post di far visionare al professore nome e cognome degli studenti prenotati per uno specifico appello
		- servlet Registrazione con metodo post permette all'utente di registrarsi ed essere aggiunto alla tabella professori o studenti del db
