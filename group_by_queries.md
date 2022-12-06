### GROUP BY QUERIES:

# 1. Contare quanti iscritti ci sono stati ogni anno:
 - SELECT COUNT(id) AS 'students_per_year', year(`enrolment_date`) AS 'year' FROM `students` GROUP BY year(`enrolment_date`);

# 2. Contare gli insegnanti che hanno l'ufficio nello stesso edificio:
 - SELECT COUNT(id) AS 'teachers', `office_address` FROM `teachers` GROUP BY `office_address`;

# 3. Calcolare la media dei voti di ogni appello d'esame:
 - SELECT CEILING(AVG(`vote`)) as 'exam_vote_average', `exam_id` as 'exam' FROM `exam_student` GROUP BY `exam_id`;

# 4. Contare quanti corsi di laurea ci sono per ogni dipartimento:
- SELECT COUNT(`name`) AS 'degrees', `department_id` AS 'department' FROM `degrees` GROUP BY `department_id`;
