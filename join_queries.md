## Join queries:

# Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia:
- SELECT `students`.*, `degrees`.name FROM `students` JOIN `degrees` ON `degrees`.id = `students.degree_id` WHERE `degrees`.`name` = 'Corso di Laurea in Economia';
# Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze:

- select degrees.*, departments.name from degrees join departments on departments.id = degrees.department_id where departments.name = 'Dipartimento di Neuroscienze' and degrees.level = 'magistrale'
# Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44):

- select courses.*, teachers.name, teachers.surname, teachers.id from courses join course_teacher on course_teacher.course_id = courses.id join teachers on course_teacher.teacher_id =teachers.id where teachers.name = 'Fulvio' and teachers.surname = 'Amato'
# Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome

- select students.name, students.surname, degrees.name, deparments.* from students join degrees on students.degree_id = degrees.id join departments on degrees.department_id = departments.id order by students.name, students.surname

# Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

- select degrees.name, courses.name, courses.period, courses.year, courses.cfu, teachers.name, teachers.surname from degrees join courses on courses.degree_id = degrees.id join course_teacher on course_teacher.course_id = courses.id join teachers on course_teacher.teacher_id = teachers.id 

# Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

- select distinct teachers.* from teachers join course_teacher on course_teacher.teacher_id = teacher.id join courses on course_teacher.course_id = course.id join degrees on courses.degree_id = degrees.id join departments on degrees.department_id = departments.id where departments.name = 'Dipartimento di Matematica' 
