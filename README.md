# crud-javafx-jdbc

### Application
<details><summary>Home screen</summary>
  
  Application home screen 
  
  <img src="https://user-images.githubusercontent.com/52088266/175179272-b2634caf-b1e4-4a1b-b762-9cea5bb9a1be.png" width="50%">
    
</details>

<details><summary>Adding/Editing/Remove department</summary>

  Select: Registration > Department
    
  <img src="https://user-images.githubusercontent.com/52088266/175182879-7ee28243-4d61-4718-b4dd-9325ed5fc308.png" width="50%">
  
  You can add a new Department, edit an existing one or also delete
    
  <img src="https://user-images.githubusercontent.com/52088266/175182955-8800664c-648d-46ec-8b06-8263994a3a12.png" width="50%">
  
  Creating a new department

  <img src="https://user-images.githubusercontent.com/52088266/175183059-30d819fc-3d50-44b4-924e-36c958a7b183.png" width="50%">
  <img src="https://user-images.githubusercontent.com/52088266/175183126-51e4ef73-2451-43f1-a90c-70161c06e54a.png" width="50%">

</details>


<details><summary>Adding/Editing/Remove seller</summary>

  Select: Registration > Seller
  
  <img src="https://user-images.githubusercontent.com/52088266/175180808-db866f58-6c95-4f9e-b077-a0a8539ffa4d.png" width="50%">
  
  You can add a new seller, edit an existing one or also delete
    
  <img src="https://user-images.githubusercontent.com/52088266/175182621-3eb94f74-734d-44b0-aadb-584bdfb09127.png" width="50%">
   
  Creating a new seller in the new department

  <img src="https://user-images.githubusercontent.com/52088266/175183271-b73daf1c-97c8-4d92-8e18-ae9fb96246c1.png" width="50%">
  <img src="https://user-images.githubusercontent.com/52088266/175183339-5beeba23-d687-4a70-be50-c56d1079e73b.png" width="50%">

  
</details>

####

#### MySQL Query
```mysql
CREATE TABLE department (
  Id int(11) NOT NULL AUTO_INCREMENT,
  Name varchar(60) DEFAULT NULL,
  PRIMARY KEY (Id)
);

CREATE TABLE seller (
  Id int(11) NOT NULL AUTO_INCREMENT,
  Name varchar(60) NOT NULL,
  Email varchar(100) NOT NULL,
  BirthDate datetime NOT NULL,
  BaseSalary double NOT NULL,
  DepartmentId int(11) NOT NULL,
  PRIMARY KEY (Id),
  FOREIGN KEY (DepartmentId) REFERENCES department (id)
);

INSERT INTO department (Name) VALUES 
  ('Computers'),
  ('Electronics'),
  ('Fashion'),
  ('Books');

INSERT INTO seller (Name, Email, BirthDate, BaseSalary, DepartmentId) VALUES 
  ('Bob Brown','bob@gmail.com','1998-04-21 00:00:00',1000,1),
  ('Maria Green','maria@gmail.com','1979-12-31 00:00:00',3500,2),
  ('Alex Grey','alex@gmail.com','1988-01-15 00:00:00',2200,1),
  ('Martha Red','martha@gmail.com','1993-11-30 00:00:00',3000,4),
  ('Donald Blue','donald@gmail.com','2000-01-09 00:00:00',4000,3),
  ('Alex Pink','bob@gmail.com','1997-03-04 00:00:00',3000,2);
  ```
