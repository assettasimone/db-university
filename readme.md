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
- department_id


### Table: degree_courses

- id
- name
- type
- duration
- department_id


