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

- id INT 
- name VARCHAR(30)
- address VARCHAR(60)
- telephone VARCHAR(11)
- mail VARCHAR(60)
- website VARCHAR(60)
- director VARCHAR(60)


### Table: teachers

- id INT
- first_name VARCHAR(60)
- last_name VARCHAR(60)
- telephone VARCHAR(11)
- mail VARCHAR(60)
- tax_id_code CHAR(16)
- role VARCHAR(11)
- office VARCHAR(5)
- department_id (FK) INT


### Table: degree_courses

- id  INT
- name VARCHAR(60)
- type VARCHAR(20)
- duration TINYINT
- department_id (FK) INT


### Table: courses

- id  INT
- name VARCHAR(60)
- cfu TINYINT
- description TEXT
- degree_course_id INT


### Table: students

- id  INT
- first_name VARCHAR(60)
- last_name VARCHAR(60)
- freshman CHAR(6)
- enrollment_year YEAR
- mail VARCHAR(60)
- birth_date DATE
- degree_course_id (FK) INT

### Table: exams

- id  INT
- name VARCHAR(60)
- room VARCHAR(5)
- date DATE


### Table pivot: exams_students_teachers

- id  INT
- course_id (FK)  INT
- teacher_id (FK)  INT
- student_id (FK)  INT
- vote TINYINT
- attempt_number TINYINT
- passed TINYINT

### Table Pivot: courses_teachers

- id  INT
- teacher_id INT
- course_id INT