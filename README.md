# my-todo-list-backed
simple todo-list-api (Work In Progress)

# Installation
1. Install Mongodb locally and check mongodb server already running on your device OR you can use cloud mongodb, in https://cloud.mongodb.com/  
2. clone git repository : `git clone https://github.com/fikrihashfi/my-todo-list-backend.git`
3. go to folder : `cd my-todo-list-backend`
4. install all dependencies : `npm install`
5. create .env on folder and insert `DB_URI_Local=<your-db-server>/my-db`.
6. start project : `nodemon index.js`

# Todo Schema

    { 
        validator: { $jsonSchema: { 
        bsonType: "object", 
        required: [
            "description", 
            "username",
        ], 
        properties: { 
            description:{
                bsonType: "string", 
                description: "required and must be a string" }, 
            username: { 
                bsonType: "string", 
                description: "required and must be a string" }, 
        }
    }
   
# Get
<your_base_url>/api/todos (get method)

<your_base_url>/api/todos/:id (get method)

# Insert
<your_base_url>/api/todos/add (post method)

example insertion data body:

{"description":"todo api","subject":"Make todo api","username":"fikrihashfi","priority":"low","time":"2020-02-02","completed":false}

# Update
<your_base_url>/api/todos/update/:id (post method)

{"description":"todo","username":"fikrihashfi","priority":"high","time":"2020-01-01","completed":false}

# Delete
<your_base_url>/api/todos/delete/:id (delete method)

*Note : if dependencies not fully installed try to delete package-lock.json




