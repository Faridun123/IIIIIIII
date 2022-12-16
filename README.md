# API
# «Application Programming Interface»
![](./README%20IMAGES/img-01.webp)

# В чем разница между API и REST API?

## API - это общий термин, который означает "программный  
## интерфейс приложения"

## Rest API - это конкретный API, под названием REST, 
## описывающий протокол взаимодействия с веб-сервисом.

# Fetch()
## Fetch API предоставляет интерфейс JavaScript для работы с 
## запросами и ответами HTTP. Он также предоставляет 
## глобальный метод fetch() (en-US), который позволяет легко и 
## логично получать ресурсы по сети асинхрониний


# GET
const getUsers = async ( ) => {
try {
const response = await fetch("“);
const data = await response.json();
console.log(data);
}
catch (error) {
console.log(error)
}

# POST
const postUser = async (user) => {
try {
const response = await fetch(“...“,
{ 
method: "POST",
headers: {
Accept: "application/json",
"Content-Type": "application/json",
},
body: JSON.stringify(user),
});
}
catch (error) {
console.log(error)
}
# PUT
const putUser= async (id,edituser) => {
try {
const response = await fetch(“...“,
{ 
method: “PUT",
headers: {
Accept: "application/json",
"Content-Type": "application/json",
},
body: JSON.stringify(edituser),
});
}
catch (error) {
console.log(error)
}

# DELETE

const deleteUser= async (id) => {
try {
const response = await fetch(“...“,
{ 
method: “DELETE",
});
}
catch (error) {
console.log(error)
}

# axios
# Axios - это HTTP-клиент, основанный на Promise для node.js и
# браузера. Он может работать в браузере и node.js с той же базой кодов.

# <script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>

# GET
const postCreate = async () => {
try {
const { data } = await axios.get(`url`)
} catch (error) {
}
}

# POST
const postCreate = async (editUser) => {
try {
const { data } = await axios.post(`url`, editUser)
} catch (error) {
}
}

# PUT
const postCreate = async (id,editUser) => {
try {
const { data } = await axios.post(`url/${id}`, editUser)
} catch (error) {
}
}
# Delete 
const postCreate = async (id) => {
try {
const { data } = await axios.delete(`url/${id}`)
} catch (error) {
}
}