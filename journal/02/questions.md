# Intro to JavaScript
01. Which keywords are used to declare a variable in JavaScript?

    > let or var

02. What is the definition of a function?

    >A subprogram to preform a task.

03. What are the `SOLID` principles?

    >S - Single-responsiblity Principle
    >O - Open-closed Principle
    >L - Liskov Substitution Principle
    >I - Interface Segregation Principle
    >D - Dependency Inversion Principle

04. Given this array: How could you remove the `pineapple`?

    ```js
    let fruit = ['apple', 'banana', 'pineapple', 'orange', 'strawberry']
    ```
    
    > fruit.splice(2,1)
05. Given these two objects: How could you add each to the others friends arrays?

    ```js
    let you = {
        name: "You",
        hair: true,
        friends: []
    }
    let them = {
        name: "Them",
        hair: false,
        friends: []
    }
    ```

    > you.friends.push(them)
    > them.friends.push(you)

06. Give an example of a JavaScript `Conditional`:
    >let js = hard
    > if (js == hard) {
    console.log("YES")
    }

07. What is the main difference between `parameters` and `arguments`?

    > Parameters takes in an argument. Arguments has a value.

08. Instead of writing everything to the console, what is a better way to debug your code?

    > use a debugger

09. What is the difference between a `primitive` value and a `reference` value?

    >Primitive type always has a value. It can never be null. Reference type can be null.

10. Demonstrate a loop that prints the numbers between -100 and 100?

    > for (let i = -100; i <= 100; i++) {
   console.log(i);
}
