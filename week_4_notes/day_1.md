# Week 4

## By the end of the week all developers can:

* Build a simple web app with a database
* Follow an effective debugging process for database applications
* Explain the basics of how databases work (e.g. tables, SQL, basic relationships between tables)


## Recap on MVC

Model
- logic
- Computational work
- Manipulating data

View
- How the page looks
- Presentation layer

Controller
- how to get from one page to another

Benefits
- Readability
- Easier to change
- Reuse
- Performance

## Database

Learning Objectives

https://github.com/makersacademy/course/blob/main/bookmark_manager/learning_objectives.md


## PostgresSQL
getting to the psql prompt as postgres superuser

`sudo -u postgres psql`

getting to psql as myself.. needs a database

`psql -U bromley chitter`

Check if postgres 

`pgrep -u postgres -fa -- -D`

Check if a server is up and running:

`pg_lsclusters`


Start a server (version, name)

`sudo pg_ctlcluster 12 main start`

https://mydbanotebook.org/post/troubleshooting-01/

https://www.cybertec-postgresql.com/en/postgresql-on-wsl2-for-windows-install-and-setup/

https://www3.ntu.edu.sg/home/ehchua/programming/sql/PostgreSQL_GetStarted.html