1111111111111
1)Create table student(name char(10), regno number(2) primary key not null, class number(2),major 
char(2));
Create table course(coursename char(20), course_number varchar(10) primary key not null, 
credithours number(1), department char(5));
Create table section(section_identifier number(3) primary key not null, year number(2), instructor 
char(10), course_number varchar(10), foreign key(course_number) references 
course(course_number) on delete cascade);
Create table grade_report(grade char(1), regno number(2),foreign key(regno) references 
student(regno) on delete cascade, section_identifier number(3), foreign key(section_identifier) 
references section(section_identifier) on delete cascade);
2)insert into studen
3)Alter table section
add section1 char(1);
update section 
set section1=’D’;
4)delete grade_report
where regno in (select regno
from student
where name=’brown’);
5)drop table section;

222222222222222222222
Table: Employee.create table employee(empid number(5)primary key not null, firstname char(10),lastname char(10),hire_date date,address varchar(20),city char(15));Table: Empsalary.create table empsalary(salary number(5),benefits number(5),designation char(10),empid number(5),foreign key (empid)references employee(empid) on delete cascade);
1)select firstname,lastname,address,cityfrom employee where city=’Paris’;
2)select * from employee order by firstname desc;
3)select e.firstname,es.salaryfrom employee e,empsalary eswhere e,empid=es.empid and designation=’salesman’;
4)Select e.firstname,e.lastname,(es.salary+es.benefits)as total salaryfrom employee e,empsalary eswhere e.empid=es.empid;
5)Select firstname,lastname from employeewhere (hire_date –sysdate)>365;
6)select count(distinct designation)from empsalary;
8)Alter table employeeadd phone_no number(10);update employeeset phone_no=’1234567890’;
9)select * from employeewhere hire_date ’16-Jun-07’ and ’15-Jun-08’;
10)Select es.salary,e.firstname.es.benefits(es.salary*0.5+es.salary*0.3+es.salary*0.12)as grossfrom employee e,empsalary eswhere e.empid=es.empidorder by gross desc;
