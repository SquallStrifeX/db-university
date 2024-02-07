1. Contare quanti iscritti ci sono stati ogni anno;

SELECT YEAR(enrolment_date) AS enrolment_year, COUNT(id) AS number_of_students FROM `students` GROUP BY YEAR(enrolment_date);

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio