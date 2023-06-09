# CSharp and SQL Fundamentals
01. What is the purpose of a `namespace`?

  > To help with naming conflicts.

02. What is the difference between a `class` and an `interface`?

  > A class can be instantiated. An interface cannot be instantiated.

03. What is the method that returns an instance of a class, yet it has no return type?

  > A constructor.

05. In the Car example what is the access modifier of the `Start()` method?

  ```c#
  [HttpPUT]
  abstract class Car
  {
    public string Start()
    {

      return "Vroooom";

    }
  }
  ```

  > Public

06. In the Car example what is `string` an indication of?

  > A return type. 

07. In the Car example what is `abstract` preventing?

  > Preventing the class from being instantiated.

08. In a SQL table, what is the difference between information in a row and information in a column?

  > Row is a data item in a table. A column is 1 data item that a table represents.

09. Demonstrate the necessary SQL for creating a table called `characters` with the values `name, age, description` as strings, and an `int` id.

  > CREATE TABLE characters(
    id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(200) NOT NULL,
    age INT NOT NULL,
    description VARCHAR(500) NOT NULL
  ) default charset utf8 COMMENT '';

10. In SQL how can you query more than a single table? Provide an example.

  > SELECT 
    characters.*,
    account.*
    FROM characters
    JOIN accounts ON characters.id = account.id;

