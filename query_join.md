<!--
-- 1. Selezionare tutti gli studenti iscritti al Corso di Laurea in Economia

--//

  SELECT *
  FROM `students`
  INNER JOIN `degrees`
  ON `students`.`degree_id` = `degrees`.`id`
  WHERE `degrees`.`id`='53';

//--




-- 2. Selezionare tutti i Corsi di Laurea Magistrale del Dipartimento di Neuroscienze

--//



//--



-- 3. Selezionare tutti i corsi in cui insegna Fulvio Amato (id=44)

--//

  SELECT * FROM `course_teacher`
  INNER JOIN `courses`
  ON `course_teacher`.`course_id` = `courses`.`id`
  WHERE `course_teacher`.`teacher_id`='44';

//--



-- 4. Selezionare tutti gli studenti con i dati relativi al corso di laurea a cui sono iscritti e il relativo dipartimento, in ordine alfabetico per cognome e nome

--//

  SELECT * FROM `students`
  INNER JOIN `degrees`
  ON `students`.`degree_id` = `degrees`.`id`
  INNER JOIN `departments`
  ON `degrees`.`department_id` = `departments`.`id`
  ORDER BY `students`.`surname` ASC;

//--




-- 5. Selezionare tutti i corsi di laurea con i relativi corsi e insegnanti

--//

  SELECT * FROM `degrees`
  INNER JOIN `courses`
  ON `degrees`.`id` = `courses`.`degree_id`
  INNER JOIN `course_teacher`
  ON `courses`.`id` = `course_teacher`.`course_id`

//--



-- 6. Selezionare tutti i docenti che insegnano nel Dipartimento di Matematica (54)

--//



//--



-- 7. BONUS: Selezionare per ogni studente quanti tentativi d’esame ha sostenuto per
superare ciascuno dei suoi esami

--//



//--





-->
