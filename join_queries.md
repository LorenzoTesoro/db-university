## Join queries:

# Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia:

- SELECT `students`.`degree_id`, `degrees`.`name` FROM `degrees` JOIN `students` ON `students`.`degree_id` = `degrees`.`id` WHERE `degrees`.`name` = 'Corso di Laurea in Economia';

# Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze:

- SELECT `department_id`, `level` FROM `degrees` JOIN `departments` ON departments.id = degrees.department_id WHERE level = 'magistrale';

# Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44):

- SELECT `department_id`, `level` FROM `degrees` JOIN `departments` ON departments.id = degrees.department_id WHERE level = 'magistrale';



Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome
Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti
Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)
