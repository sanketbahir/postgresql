# postgresql

sudo -i -u postgres =>  we use this  command  to swich  too postgres user

psql =>  to swich  postgres client

\q => to exit postgres client

createdb =  nameof database  => to create data base 


psql  -d nameof database => to  swich  to database


To Create  a table  

CREATE TABLE cars (
  brand VARCHAR(255),
  model VARCHAR(255),
  year INT
);

  To Display Table
You can "display" the empty table you just created with another SQL statement:

SELECT * FROM cars;

To insert data in table
INSERT INTO cars (brand, model, year)
VALUES ('Ford', 'Mustang', 1964);

To fetch data
SELECT brand, year FROM car;


TO add colum into table  Add a column named color:
ALTER TABLE cars
ADD color VARCHAR(255);

TO update 
UPDATE cars
SET color = 'red'
WHERE brand = 'Volvo';

TO update  mulltipal things we use 
UPDATE car SET color = 'white',year= 1234 WHERE brand ='toyota';


TO update the year column from INT to VARCHAR(4):
ALTER TABLE cars
ALTER COLUMN year TYPE VARCHAR(4);

TO  Change the color column from VARCHAR(255) to VARCHAR(30):
ALTER TABLE cars
ALTER COLUMN color TYPE VARCHAR(30);


TO delete the  columnwe   use 
ALTER TABLE car  DROP COLUMN color;

TO  Delete all records where brand is 'Volvo':
DELETE FROM cars
WHERE brand = 'Volvo';

TO  Delete all records in the cars table:
DELETE FROM cars;

TO Delete all records in the cars table:
TRUNCATE TABLE cars;


