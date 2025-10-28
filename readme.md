# Esercizio

Modellizzare la struttura di un database per memorizzare tutti i dati riguardanti una università

## Tables

- departments
- degree_courses
- courses
- teachers
- students
- exams

### Table: departments 

- id
- name
- address
- telephone
- mail
- website
- director


### Table: teachers

- id
- first_name
- last_name
- telephone
- mail
- tax_id_code
- role
- office
- department_id (FK)


### Table: degree_courses

- id
- name
- type
- duration
- department_id (FK)


### Table: students

- id
- first_name
- last_name
- freshman
- enrollment_year
- mail
- birth_date
- degree_course_id (FK)

### Table: exams

- id
- name
- room
- date
- course_id
- teacher_id
- student_id
- vote
- attempt_number
- passed


### Table Courses

- id
- name
- CFU
- description
- degree_course_id
- department_id


### Table Pivot: Courses_teachers

- id
- teacher_id
- course_id