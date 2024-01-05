CREATE DATABASE University;
USE University;
SHOW TABLES;
SELECT * FROM Students;
SELECT * FROM HighSchool_Subjects;
SELECT * FROM Marks;
SELECT * FROM Universities;


CREATE TABLE Students (
    ID INT AUTO_INCREMENT PRIMARY KEY,
    first_name VARCHAR(50),
    last_name VARCHAR(50)
);

CREATE TABLE HighSchool_Subjects (
    ID INT AUTO_INCREMENT PRIMARY KEY,
    Subject_name VARCHAR(50)
);

CREATE TABLE Marks (
    Student_ID INT,
    Subject_ID INT,
    Mark INT,
    FOREIGN KEY (Student_ID) REFERENCES Students(ID),
    FOREIGN KEY (Subject_ID) REFERENCES HighSchool_Subjects(ID),
    CONSTRAINT fk_student_subject UNIQUE (Student_ID, Subject_ID) 
);

CREATE TABLE Universities(
	ID INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(100),
    Lowest_Subject_Mark INT,
    Average_Marks_Entry INT);
    
INSERT INTO Students(first_name, last_name)
VALUES 
('John', 'Smith'),
('Emma', 'Johnson'),
('Michael', 'Williams'),
('Sophia', 'Brown'),
('William', 'Jones'),
('Olivia', 'Garcia'),
('James', 'Miller'),
('Amelia', 'Davis'),
('Benjamin', 'Rodriguez'),
('Isabella', 'Martinez'),
('Daniel', 'Hernandez'),
('Charlotte', 'Lopez'),
('Alexander', 'Gonzalez'),
('Mia', 'Wilson'),
('Henry', 'Anderson'),
('Ella', 'Thomas'),
('Matthew', 'Taylor'),
('Avery', 'Moore'),
('Scarlett', 'Jackson'),
('David', 'White'),
('Grace', 'Harris'),
('Liam', 'Martin'),
('Chloe', 'Thompson'),
('Jackson', 'Robinson'),
('Abigail', 'Clark'),
('Lucas', 'Lewis'),
('Emily', 'Lee'),
('Harper', 'Walker'),
('Evelyn', 'Hall'),
('Sebastian', 'Young'),
('Aria', 'Allen'),
('Owen', 'Sanchez'),
('Camila', 'Wright'),
('Carter', 'King'),
('Sofia', 'Scott'),
('Wyatt', 'Green'),
('Madison', 'Baker'),
('Elijah', 'Adams'),
('Luna', 'Nelson'),
('Grayson', 'Hill'),
('Layla', 'Rivera'),
('Gabriel', 'Campbell'),
('Zoey', 'Mitchell'),
('Lincoln', 'Perez'),
('Penelope', 'Roberts'),
('Anthony', 'Turner'),
('Hannah', 'Phillips'),
('Andrew', 'Evans'),
('Stella', 'Carter'),
('Joshua', 'Flores'),
('Nova', 'Morales'),
('Christopher', 'Reed'),
('Addison', 'Cook'),
('Nathan', 'Bailey'),
('Ellie', 'Parker'),
('Christian', 'Sanders'),
('Brooklyn', 'Price'),
('Isaac', 'Bell'),
('Victoria', 'Wood'),
('Julian', 'Bennett'),
('Leah', 'Barnes'),
('Evan', 'Ross'),
('Aurora', 'Coleman'),
('Nicholas', 'Jenkins'),
('Audrey', 'Perry'),
('Tyler', 'Powell'),
('Claire', 'Long'),
('Luke', 'Howard'),
('Bella', 'Foster'),
('Adam', 'Reyes'),
('Skylar', 'Murphy'),
('Zoe', 'Russell'),
('Charles', 'Griffin'),
('Ellie', 'Diaz'),
('Joseph', 'Hayes'),
('Mila', 'Myers'),
('Axel', 'Ford'),
('Lily', 'Hamilton'),
('Mason', 'Ward'),
('Paisley', 'Sullivan'),
('Jameson', 'Wallace'),
('Sarah', 'Henderson'),
('Emilia', 'Kennedy'),
('Eli', 'Pearson'),
('Aaliyah', 'West'),
('Cooper', 'Collins'),
('Adeline', 'Gomez'),
('Jordan', 'Gutierrez'),
('Violet', 'Murray'),
('Miles', 'Simmons'),
('Caroline', 'Bryant'),
('Eleanor', 'Kim'),
('Mateo', 'Nguyen'),
('Alexa', 'Fuller'),
('Lukas', 'Kovac'),
('Sophie', 'Schmidt'),
('Marius', 'Müller'),
('Laura', 'Fischer'),
('Elias', 'Weber'),
('Julia', 'Wagner'),
('Simon', 'Becker'),
('Emilia', 'Schneider'),
('Andreas', 'Keller'),
('Elena', 'Meier'),
('Finn', 'Schulz'),
('Nora', 'Hofmann'),
('Gabriel', 'Lehmann'),
('Lena', 'Herrmann'),
('Matthias', 'König'),
('Maja', 'Walter'),
('David', 'Schwarz'),
('Klara', 'Bauer'),
('Adrian', 'Hartmann'),
('Lina', 'Böhme'),
('Jonas', 'Krause'),
('Mia', 'Schuster'),
('Lucas', 'Frank'),
('Amelie', 'Jung'),
('Jan', 'Schmid'),
('Clara', 'Wolf'),
('Oskar', 'Neumann'),
('Lea', 'Bayer'),
('Sebastian', 'Vogel'),
('Paulina', 'Hahn'),
('Jakob', 'Zimmermann'),
('Charlotte', 'Kühn'),
('Maximilian', 'Bach'),
('Ida', 'Hermann'),
('Felix', 'Pohl'),
('Emma', 'Lange'),
('Niklas', 'Werner'),
('Hannah', 'Richter'),
('Johannes', 'Schreiber'),
('Theresa', 'Kraus'),
('Philip', 'Arnold'),
('Victoria', 'Schultz'),
('Leonie', 'Kaiser'),
('Tobias', 'Huber'),
('Marie', 'Winkler'),
('Benjamin', 'Bergmann'),
('Emily', 'Lorenz'),
('Tim', 'Fuchs'),
('Valentina', 'Voigt'),
('Anton', 'Stein'),
('Elisa', 'Schumacher'),
('Daniel', 'Graf'),
('Isabelle', 'Sommer'),
('Kevin', 'Seidel'),
('Sara', 'Marx'),
('Erik', 'Kramer'),
('Mila', 'Jäger'),
('Noah', 'Koch'),
('Maria', 'Freitag'),
('Jannis', 'Vogt'),
('Sarah', 'Sauer'),
('Luca', 'Roth'),
('Magdalena', 'Lehmann'),
('Aaron', 'Engel'),
('Anna', 'Friedrich'),
('Samuel', 'Schindler'),
('Sophia', 'Götz'),
('Christian', 'Barth'),
('Isabella', 'Thiel'),
('Jonathan', 'Bayer'),
('Melina', 'Wagner'),
('Fabian', 'Peters'),
('Amalia', 'Schreiber'),
('Luc', 'Vogel'),
('Caroline', 'Kaiser'),
('Liam', 'Schiller'),
('Elisabeth', 'Hansen'),
('Dominik', 'Hoffmann'),
('Valerie', 'Heinrich'),
('Michael', 'Ludwig'),
('Leona', 'Bach'),
('Paul', 'Werner'),
('Hanna', 'Krüger'),
('Alexander', 'Günther'),
('Romy', 'Jansen'),
('Julian', 'Baumann'),
('Emilia', 'Koch'),
('Moritz', 'Schroeder'),
('Rosalie', 'Mayer'),
('Jakob', 'Ziegler'),
('Lara', 'Pfeiffer'),
('Fabienne', 'Kraus'),
('Jonas', 'Brunner'),
('Annelie', 'Berg'),
('David', 'Richter'),
('Julie', 'Schulte'),
('Leon', 'Voigt'),
('Jana', 'Hartmann'),
('Fabio', 'Maurer'),
('Lina', 'Hein'),
('Emil', 'Hermann'),
('Paula', 'Wagner');

INSERT INTO HighSchool_Subjects (Subject_name)
VALUES
('Math'),
('Physics'),
('Chemistry'),
('History'),
('Geography'),
('Computer Science'),
('Economics'),
('Business Studies'),
('Philosophy'),
('Sociology'),
('Art');


INSERT INTO Marks (Student_ID, Subject_ID, Mark)
SELECT 
    s.ID AS Student_ID,
    h.ID AS Subject_ID,
    CASE
        WHEN RAND() < 0.3 THEN FLOOR(70 + RAND() * 11) 
        ELSE FLOOR(81 + RAND() * 20) 
    END AS Mark
FROM 
    Students s
CROSS JOIN 
    HighSchool_Subjects h;


INSERT INTO Universities (Name, Lowest_Subject_Mark, Average_Marks_Entry)
VALUES 
('University of Oxford', 85, 92),
('University of Cambridge', 87, 90),
('ETH Zurich - Swiss Federal Institute of Technology', 80, 88),
('University College London', 82, 89),
('University of Copenhagen', 79, 86),
('Heidelberg University', 81, 88),
('Technical University of Munich', 78, 85),
('Sorbonne University', 83, 91),
('University of Amsterdam', 80, 87),
('University of Helsinki', 79, 85),
('KU Leuven', 85, 92),
('University of Barcelona', 76, 84),
('University of Milan', 78, 86),
('Stockholm University', 75, 82),
('University of Warsaw', 77, 85),
('University of Vienna', 82, 88),
('University of Oslo', 80, 87),
('Charles University in Prague', 77, 83),
('University of Zurich', 84, 91),
('Ludwig Maximilian University of Munich', 86, 93),
('University of Edinburgh', 85, 90),
('University of Manchester', 78, 86),
('University of Bristol', 79, 87),
('University of Gothenburg', 76, 83),
('University of Turin', 77, 85),
('University of Glasgow', 80, 88),
('University of Porto', 75, 81),
('University of Tübingen', 83, 90),
('University of Belgrade', 79, 86),
('University of Salamanca', 81, 87);


-- queries -- 


-- Who passed & who failed -- 
SELECT 
    Students.ID, CONCAT(Students.first_name,' ',Students.last_name) AS full_name, 
    MIN(Marks.Mark) AS lowest_mark, 
    AVG(Marks.Mark) AS average_mark, 
    CASE
        WHEN MIN(Marks.Mark) >= 75 AND AVG(Marks.Mark)>= 81 THEN 'Pass' 
        ELSE 'Fail' 
    END AS Final_Exams
FROM
    Students
JOIN
    Marks ON Students.ID = Marks.Student_ID 
GROUP BY Students.ID 
ORDER BY average_mark DESC;

 -- Highschool Board Mark --
 SELECT 
    Students.ID,
    CONCAT(Students.first_name,' ',Students.last_name) AS full_name,
    MIN(Marks.Mark) AS lowest_mark,
    MAX(Marks.Mark) AS higher_mark,
    AVG(Marks.Mark) AS average_mark
FROM
    Students
JOIN
    Marks ON Students.ID = Marks.Student_ID
GROUP BY Students.ID
ORDER BY average_mark DESC;

-- Average mark by subject --
SELECT 
    HighSchool_Subjects.Subject_name,
    ROUND(AVG(Marks.Mark),2) AS average_mark
FROM HighSchool_Subjects
JOIN
    Marks ON HighSchool_Subjects.ID=Marks.Subject_ID
GROUP BY HighSchool_Subjects.Subject_name
ORDER BY average_mark DESC;

-- Students Pass/Failed Count and Percentage --

SELECT
    SUM(CASE WHEN min_mark >= 75 AND avg_mark >= 81 THEN 1 ELSE 0 END) AS Passed_Students,
    SUM(CASE WHEN min_mark >= 75 AND avg_mark >= 81 THEN 0 ELSE 1 END) AS Failed_Students,
    ROUND((SUM(CASE WHEN min_mark >= 75 AND avg_mark >= 81 THEN 1 ELSE 0 END) / COUNT(*)) * 100,2) AS Pass_Percentage,
    ROUND((SUM(CASE WHEN min_mark >= 75 AND avg_mark >= 81 THEN 0 ELSE 1 END) / COUNT(*)) * 100,2) AS Fail_Percentage
FROM (
    SELECT
        Students.ID,
        MIN(Marks.Mark) AS min_mark,
        AVG(Marks.Mark) AS avg_mark
    FROM
        Students
    JOIN
        Marks ON Students.ID = Marks.Student_ID
    GROUP BY
        Students.ID
) AS subquery;






