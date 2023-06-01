# Vue

pages instead of controllers
pages will draw in router view

start with pages
in components add cars page with router-link to nav bar

router link :to="{name:'Cars'}"

>in CarsPage  setup-- async function getCars() try catch logger.log 
life cycle hook - onMounted= run code as soon as page mounts or renders.
>onMounted(()=>{
>  getCars()
>})

create carService

make car model

profile needs to be made to separate from account. [CHECK POINT NOTICE!]

add template in pages

add carCard in components 
move template to components

make prop in components for car

>make a new page to show car details
/cars/:carId
path: 'CarDetails',
name: 'carDetails',
component: loadPage('CarDetailsPage')

add router link to car card template

>in carDetailPage useRoute()- to find the current route url and grab info for the page

make a modal component

slot = is for forms

const editable = refs({})  
> ref can be any data type we want. We need to format an object to POST to the server. 
> ref is a placeholder. 

v-model uses the ref. editable.

> [FOR UI] if you use an icon on a button. Have a title to denote the purpose

>Components should not be more than 150 lines of code.

>DAY 4 Ref Projects from Jake
On home page see posts only by a user.

>In router
beforeEnter: authSettled checks if user is logged in.

beforeEnter(to, from, next){
 if AppState.account?.id{
 return next('/home')
 }
 next()
}

>edit accounts
Account page is for editing a user account.
lots of data not being used.
bool for user show public or not.

style
page-img

.page-img{

.account-picture{
  aspect-ratio: 1/1
}

}
background-image: v-bind(coverImg)

>In account Page - <accountForm />

>account form

<form @submit.prevent="editAccount"
<input type="text" required v-model="account.name"


setup
<!-- const editable = ref(AppState.account) -->
use this --> const editable = ref({})
>watchEffect(()=> {  = Keeps an ear out for changes to editable.value below
  editable.value = {...AppState.account}  = spread operator
})
return{
  editable,
  async editAccount(){
    try
   await accountService.editAccount(editable.value)
    catch
  }
}


compute to retrieve data
account: compute(()=> AppState.account)


>Service
async editAccount(formData)
res = await api.put('/account', {...formData, github: formData.socialPlatform})

appState.account = new Account(res.data)

new router link for user profile to pull up everything they created
create new ProfilePage

const route = useRoute()

function
 await profileService.getProfileById(route.params.id)
onMounted
getProfile()

create service
profile service(id)

getProfileById(id)
const res = await api.get('api/profile/' + id)
log
appState.activeProfile = new Profile(id)

profile computed active profile

getProjectsByProfile()
params:
creatorId: id