1. Selezionare tutti gli studenti nati nel 1990 (160);

SELECT * FROM `students` WHERE YEAR (`date_of_birth`) = 1990;

2. Selezionare tutti i corsi che valgono più di 10 crediti (479);

SELECT * FROM `courses` WHERE `cfu` BETWEEN 11 AND 99;

3. Selezionare tutti gli studenti che hanno più di 30 anni;

SELECT * FROM `students` WHERE `date_of_birth` BETWEEN '1900-1-1' AND '1994-1-1';