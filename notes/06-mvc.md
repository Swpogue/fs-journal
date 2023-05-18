# MVC
MODEL FIRST!! Model is the Blueprint of items to draw. Definition or templates.

AppState is where where all the apps data will be stored. Draws from Model/class

Controller is Info from Action on html and draws data to Html. 
class ""{
}
export const ''

Service is responsible for business logic. Anything that modifies data goes here. Business Logic.

Html-app.js-controller.js-appState.js-model.js = order of hiearchy


<!-- Model. View. Controller.
mvc patten is tried and true pattern.
design patten: is underlying code -->

application patten: scales an entire application
View is HTML


bcw create

class/ does not need function in controller.js

Model- constructors(rawMaterial or data)= is a key word; special function used for instantiating a class or instance of a class. Builds something.

constructors(rawMaterial or data){
  this.id = data.id || generateId()
  this.name = data.name
  this.heath = data.health
  this.level = data.level
}

this= this instance this time around.
new/ is a keyword

singleton pattern- for export const- only 1 service= e

<!-- Need to use to grab from somewhere-->
appState.on('banana', drawBanana)
appState.emit('banana') triggers listeners.

key, value/ pairs

ctrl . to set a method to the next level

<!-- Getters and Setters -->
Get= an additional property for a class and can access them with dot notation.


<!-- ORDER OF THE STARTING CODE IN MVC -->
STEP 1= 'Controller'- export class controller {constructor}  Register controller in app.js

Step 2= router

Step 3= Get api data from an open api 

STEP 4= 'Service'- export const ??Service = new ??Service(); appState.on('something')  log is important!!!

STEP 5= 'MODEL'- add the blueprints. Export class{ constructor then this.data *n }

STEP 6= 'AppState'- arrays  <import Model>


Step 7= Build an html model to import to- MODEL with 'get ??template'{ return` div stuff `}

Step 8= 'Controller' make a function _draw??() "declare method"

Step 9= Set actives in controllers and call  setActive(??Id) ??Service.setActive(??Id)

Step 10= appSate setActive /** @type {import('./Models/Car').Car|null} */
  activeCar = null

Step 11=Controller setActive(carId) {
        let foundCar = appState.cars.find(c => c.id == carId)
        console.log(foundCar);
        appState.activeCar = foundCar
    }

Step 12= make template in model = get Active??Template(){return` div stuff` }

