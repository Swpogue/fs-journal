# Async
<!-- API -->
Build an export class in model to parse through th data you want and don't want. Character.js. Match the API data names.
API is async. 





get CardTemplate (){
  return /*html*/`
  <div>
  ${this.name}
  </div>
  `
}
async goGetMyCharacters()
await characterService.goGetMyCharacters()
const res = await hpApi.get('/api/characters') brings in the data from the axiosService. 
console.log(res.data)

axios script- this returns raw data. Object or Pojos. Pass through class.
axiosService export const hpApi = axios.create(
  baseUrl:
)

<!-- Make a model to map to -->
appState.char = res.data.map(c => new char(c))

.map(f => 'banana') function takes data to something else. Returns 

when submitting form data. send to API
instead of get, do post


<!-- CODEWORKS API -->

F2 on api to chang to sandboxApi

ADD links to cars
build controller - connect to router

build service

appState.on accounts

bcw create - mvc auth


#/about  hash change

env.js
localhost

add domain: codeworksClassroom.auth0.com
audience: https://codeworksclassroom.com
clientId: pOXw2OGv1LsYi7LEBmDF04RLkXQvldml

base url sandbox.codeworksacademy.com twice for ternary.


router.js
path and a controller

appState.on('account' draw)

const yes = await Pop.confirm

const res = await api.delete(`api/cars/${id}`)

create
read
update
delete

add a new axios api for dnd