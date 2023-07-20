### To Create DEP Database
Name the database as DEP_TEST

Views

Learner View
dtv_bv_learners
1. LEARNER_ID char(20 byte)
2. LEARNER_EMAIL varchar(100 byte)

MS SQL Server:

```sql
create table dbo.dtv_bv_learners(LEARNER_ID char(20) primary key, LEARNER_EMAIL varchar(100));
```

Course View
dtv_courses
1. COURSE_ID varchar(20) Primary Key
2. COURSE_TITLE varchar(225)

MS SQL Server:

```sql
create table dbo.dtv_courses(COURSE_ID varchar(20) primary key, COURSE_TITLE varchar(225));
```

EVL View
dtv_bv_evl_data
1. EVL_ID varchar(20) Primary Key
2. LEARNER_ID char(20) Foreign Key from Learner View
3. DURATION_HOURS int | should be number(22, 2) in plsql |
4. EVL_STATUS varhcar(50)
5. SCORE int | should be number(22) in plsql 

MS SQL Server:

```sql
create table dbo.dtv_bv_evl_data(EVL_ID varchar(20) primary key, LEARNER_ID char(20), DURATION_HOURS int, EVL_STATUS varchar(50), SCORE int);
```

### To Create Main Database
Name the database as MainDB_TEST

Views

Courses View
Courses
1. Id int unique not null identity(1,1)
1. COURSES_ID varchar(20) unique
3. COURSE_TITLE varchar(225)

MS SQL Server:

```sql
create table dbo.Courses(Id int unique not null identity(1,1), COURSE_ID varchar(20) unique, COURSE_TITLE varchar(225));
```

Learners View
Learners
1. Id int unique not null identity(1,1)
1. LEARNER_ID varchar(20) unique
3. LEARNER_EMAIL varchar(225)

MS SQL Server:

```sql
create table dbo.Learners(Id int unique not null identity(1,1), LEARNER_ID varchar(20) unique, LEARNER_EMAIL varchar(225));
```

CourseHistory View
CourseHistory
1. Id int unique not null identity(1,1)
2. LEARNER_ID char(20) Foreign Key from Learner View
3. COURSE_TITLE varchar(225)
4. LEARNER_EMAIL varchar(225)
5. DURATION_HOURS int
6. EVL_STATUS varhcar(50)
7. SCORE int

MS SQL Server:

```sql
create table dbo.CourseHistory(
Id int unique not null identity(1,1), 
LEARNER_ID varchar(20),
COURSE_TITLE varchar(225),
LEARNER_EMAIL varchar(225),
DURATION_HOURS int,
EVL_STATUS varchar(50),
SCORE int,
foreign key(LEARNER_ID) references dbo.Learners(LEARNER_ID)
)
```

### To update Learner Id according to the LMS:
Please use the following trigger code to update the Learners Id in the Course History

MS SQL Server:

```sql
CREATE TRIGGER CourseHistoryInsert
ON CourseHistory
AFTER INSERT
AS
BEGIN
    UPDATE ch
    SET ch.LEARNER_ID = l.LEARNER_ID
    FROM CourseHistory ch
    INNER JOIN dbo.Learners l ON ch.LEARNER_EMAIL = l.LEARNER_EMAIL;
END;

CREATE TRIGGER CourseHistoryUpdate
ON CourseHistory
AFTER UPDATE
AS
BEGIN
    UPDATE ch
    SET ch.LEARNER_ID = l.LEARNER_ID
    FROM CourseHistory ch
    INNER JOIN dbo.Learners l ON ch.LEARNER_EMAIL = l.LEARNER_EMAIL;
END;
```
