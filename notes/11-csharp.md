# CSharp

>Console.WriteLine("Hello World") console log

int x = 6; == var or let
float y = 324.234f;
double dbl =123.123d;
<!-- largest datatype, used for 'm'oney -->
decimal dcl = 234.234m;

string cool = "cool stuff";
char letter = 'c';
string cooler = $"string interpolation {cool}";

bool try = true;
bool no = false;

bool? nothing = null;
int? nada = null;
string zero = null;

if(nothing == null){

}

if(x == 6){
 > Console.WriteLine("no truthy falsey")
}

>2 data type
Dictionary<string, string>dict = new Dictionary<string, string>{};  
dict.Add("one", "another one");
dict.Add("two", "another one");
dict.Remove("two");

class Dog{
  int age;
  string name;

>**public = constructor 
  public Dog(age, name){  
    this.name = name;
    this.age = age;
  }
}

>Arrays need a fixed length
Array nums = new Array[4]

List<int> numbers = new List<list> { };
numbers.add(1);
numbers.add(2);
numbers.add(3);
numbers.add(4);
numbers.add(5);
numbers.Remove(1);
List<int> lowNumbers = numbers.FindAll(n=> n <=3);
int five = numbers.Find(n=> n == 5);

numbers.ForEach(n=>{
Console.WriteLine($"i:{i} n:{numbers[i]}");
})

> Lists don't have length. They have Count.
for (int i = 0; i < numbers.Count; i++)

>START PROJECT
dotnet-auth 
> Don't name with hyphen.

dotnet restore = npm i 

> Model
namespace catRoundUp.Models;

public class Cat{

  public string Name{get; set;}

  public int Age{get; set;}

  public string Color{get; set;}

  public bool LongHair{get; set;}
}

> Controllers
namespace catRoundUp.Controllers;

[ApiController]
[Route("api/cat")]
public class CatsController : ControllerBase
{
  private readonly CatsService _catsService;

[HttpGet]
> public ActionResults <string> Test()
 {
    try{
    <!-- return "hey"; -->
    return Ok("Hey")
    }
    Catch(System.Exception){
    return BadRequest("I can't do that.");
    }
 } 

> public ActionResults<List<Cat>> GetAllCats()
{
  try{
    List<Cat> cats = catsService.GetAllCats  // go to service to get cats
    return Ok(cats);
  }
  Catch(Exception e)
  {
   return BadRequest(e.Message);
  }
}

[HttpPost]
> public ActionResults<Cat> CreateCat([FromBody] Cat catData){
  try{
      Cat cat = _catsService.CreateCat(catData);
      return Ok(cat);
  }
  Catch(Exception e)
  {
   return BadRequest(e.Message);
  }
}

}

>StartUp.cs
>Add Service and Repo to startUp

>Service
using System;
namespace catRoundUp.Services;

> public class CatsService
{

  private readonly CatsRepository _repo;

  public List<Cat> GetAllCats(){
    List<Cat> cats = 
    return cats;
  }
}

>CatsRepository
namespace catRoundUp.Repositories;

public class CatsRepo()
{

  private List<Cat> dbCats;

  public CatsRepo()
  {
    this.dbCats = 
  }

}

