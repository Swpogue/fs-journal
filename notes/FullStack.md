>backend = server
vue starter
start workstation 
env
start client and server
login
make model schema export AlbumSchema = new Schema
>model schema = many to many collabs
object1id
accountId 
virtuals
>account controller to get my objects
.get('/collaborators', this.getAccountCollabs)
getAccountCollabs
collabsService userInfo.id

service getAccountCollabs


make controller, service 
add db info

setup controller
test postman is gonna test your code
get bearer token

start code with create
gets
archive=
const album = await albumService.archiveAlbum(req.params.albumsId, req.user.id)

>service archive
archiveAlbum(albumId, userId)
const album = await this.findAlbumById(albumId)
albumId.archived = !album.archived
await album.save()



>Client
.env for server
if cloning{
npm i
start servers
}
models first
profile if account  ref: (PostIt) 

home page
get data - service get data
home- computed appState

make html then move to a card.vue make a props 
v-for a in albums key a.id

create a new path in router anf make new page for it
router-link in card :to page, params id

in new page 
const route = useRoute

.getByObject1Id
const object = route.params.objectId
.getObject2ByObject1Id
AppState.activeObject
computed bot Objects


service
getByObjectId
create appState activeObject1
getObject2ByObject1Id


create service for object2

useRouter
router.push({name:Object1Details, params: {id: newObject.id}})

make modal component



virtual in object1
memberCount

local _id
fField object1Id
ref object2
count true


