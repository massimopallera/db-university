> DB UNVERSITA`


sono presenti diversi Dipartimenti (es.: Lettere e Filosofia, Matematica, Ingegneria ecc.);
ogni Dipartimento offre più Corsi di Laurea (es.: Civiltà e Letterature Classiche, Informatica, Ingegneria Elettronica ecc..)
ogni Corso di Laurea prevede diversi Corsi (es.: Letteratura Latina, Sistemi Operativi 1, Analisi Matematica 2 ecc.);
ogni Corso può essere tenuto da diversi Insegnanti;
ogni Corso prevede più appelli d'Esame;
ogni Studente è iscritto ad un solo Corso di Laurea;
ogni Studente può iscriversi a più appelli di Esame;
per ogni appello d'Esame a cui lo Studente ha partecipato, è necessario memorizzare il voto ottenuto, anche se non sufficiente. Pensiamo a quali entità (tabelle) creare per il nostro database e cerchiamo poi di stabilirne le relazioni. Infine, andiamo a definire le colonne e i tipi di dato di ogni tabella.


## Dipartimenti (one to many -> corsi_di_laurea)
- id
- nome_dipartimento

## Corso di laurea (one to many -> courses)
- id
- dipartimento_id (FK)
- nome_corso

## Corso (many to many -> studenti)
- id
- corso_laurea_id (FK)
- nome_corso


## Esami 
- id
- corso_id (FK)
- data

## Pivot: esame_studente
- corso_id (FK)
- studente_id (FK)
- voto

## Pivot: corso_professore
- corso_id (FK)
- teacher_id (FK)

## Studente (one to one -> corso di laurea)
- matricola
- nome
- cognome
- corso
  
## Professore (one to many -> corsi)
- id
- nome
- cognome