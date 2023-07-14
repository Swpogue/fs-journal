# A bit more CSharp and SQL
1. What does ***inheritance*** accomplish for us in C#?

  > Inheritance is used to create new classes that reuse, extend, and modify the behavior defined in other classes.

2. How does ***member inheritance*** work in C#? Does a `Class` inherit all members of the base `Class`?

  >  The class which inherits the members of another class is called derived class and the class whose members are inherited is called base class. No. They must declare their own constructors.

3. How does ***accessibility*** affect inheritance?

  > Depends on the member’s visibility. Public or private.

4. What is the difference between a `PRIMARY KEY` and a `FOREIGN KEY`

  > PRIMARY KEY has the db take care of adding an Id. FOREIGN KEY references a different table.

5. What is an ***alias***?

  > Allow you to use a different word and still access an object.

6. Demonstrate how you would query a join statement that would get all of a doctors patients from the following collections:

  ```SQL
  CREATE TABLE doctors (
    id INT NOT NULL AUTO_INCREMENT,
    -- CODE OMITTED
    PRIMARY KEY (id)
  )

  CREATE TABLE patients (
    id INT NOT NULL AUTO_INCREMENT,
    -- CODE OMITTED
    PRIMARY KEY (id)
  )

  CREATE TABLE patient_doctors (
    id INT NOT NULL AUTO_INCREMENT,
    doctorId INT NOT NULL,
    patientId INT NOT NULL,

    FOREIGN KEY (doctorId)
      REFERENCES doctors(id),
    FOREIGN KEY (patientId)
      REFERENCES patients(id),
  )

  ```

  >SELECT * FROM doctors JOIN patients ON doctors.id = patients_doctor.id;

