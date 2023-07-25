# Step by Step This Project

## **- Create new project and install the dependencies:**

```bash
# ESLint, Tailwind CSS and App Router will be 'YES'
npx create-next-app@latest

npm i mongoose react-icons
```

## **- Frontend Part:**

I pass the `Frontend Part` fast because it is the `Backend Part` I want to focus on...

## **- Backend Part:**

### Database:

- Creating a new project in MongoDB Atlas
- Build Database in this project
- Give a name to this Database (MongoDB assigns the password itself)
- Create `.env` file to main project folder and add the password here
- Give the IP address 0.0.0.0 to access the database from anywhere.
- Go to: 'Cluster -> Connect -> MongoDB for VS Code' and copy your connection string.
- Add this connection string to your .env file and replace `<password>` area with your password
- Also add your connection string of the end of '/crud_db'

### Create CRUD Requests:

- Create `libs/mongodb.js` file : Here we create the function of connecting to mongobd thru the mongoose and connection string
- Create `models/topic.js` file : Here we create the database schema
- Create `api/topics/route.js` file : Create 'POST()' function.
- Use 'Postman' to check POST() function is working properly;

```bash
# *** POSTING DATA WITH POSTMAN ***

# Request Type
POST
# Request URL
http://localhost:3000/api/topics
# Object Example (Body / raw / JSON)
{
    "title": "HTML",
    "description": "A markup language for websites."
}
```

- After the above process, you should be able to see the object you POSTed in the MongoDB database.
- **_api/topics/route.js_** => Create 'GET()' function.
- Use 'Postman' to check GET() function is working properly;

```bash
# *** GETTING ALL DATA IN POSTMAN ***

# Request Type
GET
# Request URL
http://localhost:3000/api/topics

```

- **_api/topics/route.js_** => Create 'DELETE()' function.
- Use 'Postman' to check DELETE() function is working properly;

```bash
# *** DELETING DATA WITH POSTMAN ***

# Request Type
DELETE
# Request URL
http://localhost:3000/api/topics
# Object Example ( Params )
key : id
value : ___id from mongodb___
```

- After the above process, you can check that the object has been DELETEd from the MongoDB database.

- Create `api/topics/[id]/route.js` file : Create 'PUT()' function.

```bash
# *** PUTTING DATA WITH POSTMAN ***

# Request Type
PUT
# Request URL
http://localhost:3000/api/topics/___id from mongodb___
# Object Example (Body / raw / JSON)
{
    "newTitle": "CSS Updated",
    "description": "Cascading Style Sheet Updated"
}
```

- After the above process, you can check that the object has been UPDATED from the MongoDB database.
- **_api/topics/[id]/route.js_** => Create 'GET()' function.

```bash
# *** GETTING A SPECIFIC DATA IN DATABASE ***

# Request Type
GET
# Request URL
http://localhost:3000/api/topics/___id from mongodb___

```

### Connecting the Backedn to Frontend:

38:44
