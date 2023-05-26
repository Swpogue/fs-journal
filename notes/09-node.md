# Node
MVC Again!!!
<DATABASE NEVER TALKS TO CLIENT>
bcw create node-server-auth


package.json
has js object

dependencies library's if you want to run = in directory where json is, run - npm i
cors
dotenv
esm
express 
helmet = security
mongoose = talks to database
socket.io = live chats

terminal is the browser. node index.js will display in terminal

npm init

scripts
start node index.js

start button connects to json

<env auth is important>disable connect to database

no spaces or quotes in env
localhost:3000/api/values

every <Controller must extend baseController>
constructor(){
  <super('api/values')
  this.router
        v no modification - runs function
  .get('', this.getAll) = appState.on
}
reSpin = restart server if you change it.


[new code]
controller
export class banana extends BaseController
constructor
super(api/endpoint)

this.router
.get('', this.getTigers)

2nd step after service
.get('/:placeholder', this.getTiger)

3rd step
put('/:tigerId', this.editTiger)

4th step
post('', this.createTiger)

5th step('')



async getTiger(req,res,next){
try{
 logger.log req.params.tigerId
    log res 
    
  const tigers = await tigerService.getAllTigers()

    res.send('add')
}catch(error){
next(error)
}
}

debug console = logger.log

tigerService = same


controller
getAllTigers(){
  return DB.tigers

  const tiger = await tigersevice.gettigerbyid(req.params.tigerid)
 > res.send(tiger)
}

createTiger
const tiger = await tigerService  push in service

if !tiger 400 bad request
throw new BadRequest(invalid)
return tiger

>get and deletes dont have a body, put and post do.

>GregsList
<!-- express-mvc -->

gregslist.node click open workspace bottom right

reopen VS code outside of workspace to publish

env and use notpad - in client and server
be in client for bcw serve


>open server

schema gets put in data base

<!-- model -->
car.js
import mongoose

const schema = mongoose.schema

export const CarSchema = new Schema(
  {
    model: {type: String, required: true}
    make: {type: String, required: true}
    year: {type: Number, required: true}
    leaksOil: {type: Boolean, default: false}
    engineType: {type: String, enum:['8 cyl', '6 cyl', '4 cyl'], required: true}
    description: {type: String, required: true, maxLength: 500}
    creatorId: {type:Schema.type.Objectid, required: true}
    
  }
{timestamps: true}
)

>next - register to DbContext.js - create collections in our database

<!-- leftSide is how we reference in our local app code, think appState.cars -->
>v this should be plural, v-this should be singular and same naming convention
 Cars  = mongoose.model('Car', CarSchema)


>next make controller and service

carsController

export class carsController extends BaseController
constructor
super('api/cars')
this.router.get
>.use(Auth0Provider.getAuthorizedUserInfo)  everything after this line will be required to be auth.
.put.post.push.delete
CarService

>edit = put
const carData = req.body
const carId = req.param.carId
const editedCar await carService

>getCars
const cars = await dbContext.Cars.find()
return cars

>service
dbContext.Cars.create()
Add model to postman

"model": "ford", this format in postman


> carService 
editCar(carData, carId)
const originalCar = this.getCarById(carId)
originalCar.model = carData.model || originalCar.model
originalCar.make = carData.make ? carData.make : original.make
>originalCar.leaksOil = carData.leaksOil ? carData.leaksOil : original.leaksOil - for BOOLEANS


await car.remove() for delete in service

relationship types - 1 to 1  uniq pairing.  1 to many.   Many to many



timestamps: true, toJSON: { virtuals: true }

CourseSchema.virtual('school',{
localField: 'schoolId',   - matches the id you put in the model.
ref: 'School', - what model does this reference
foreignField: '_id', - what does mongoose add to the model when made.
justOne: true - only 1 userId
})

.find(query).populate('school')


<!-- view= #/about  -  A New way to do MVC for html draws-->




