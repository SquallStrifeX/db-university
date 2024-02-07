GROUP BY

1. Contare quanti iscritti ci sono stati ogni anno;

SELECT YEAR(enrolment_date) AS enrolment_year, COUNT(id) AS number_of_students FROM `students` GROUP BY YEAR(enrolment_date);

2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio;

SELECT COUNT(id), office_number FROM `teachers` GROUP BY office_number ORDER BY `teachers`.`office_number` ASC;

3. Calcolare la media dei voti di ogni appello d'esame;

SELECT exam_id, AVG(vote) AS average_vote FROM `exam_student` GROUP BY exam_id;


JOIN

1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia;

SELECT students.*, degrees.name FROM `degrees` INNER JOIN `students` ON degrees.id = students.degree_id WHERE degrees.name = 'Corso di Laurea in Economia';

2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di
Neuroscienze;

SELECT * FROM `departments` INNER JOIN `degrees` ON departments.id = degrees.department_id WHERE degrees.level = 'magistrale' AND departments.name = 'Dipartimento di Neuroscienze';
