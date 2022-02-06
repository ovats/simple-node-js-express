# node-js / express

This is a very sample of API using node.js, express and mongoose.
This code is based in the course "Building RESTful APIs with Node.js and Express" (https://www.linkedin.com/learning/building-restful-apis-with-node-js-and-express).

## Using the api

To get the Node server running locally:

- Clone this repo
- Run `npm install` to install all dependencies
- Install MongoDB and start it
- Run `npm start` to start the service (port 4000)

## Model

This API is for handling contacts.
Each contact is stored in MongoDB and contains the following information:

```
{
  "_id": "61fd79e80e869e2a7c1fee69",
  "firstName": "John",
  "lastName": "Doe",
  "email": "somemail@mail.com",
  "company": "My company",
  "phone": "555-5555",
  "created_date": "2022-02-04T19:09:28.443Z"
}
```

## Endpoints

### GET /contact

Retrieve the list of all contacts.

```
curl -X GET http://localhost:4000/contact
```  

### POST /contact

Add a new contact.

```
curl -X POST http://localhost:4000/contact \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -d 'firstName=John&lastName=Doe&email=john%40me.com&company=linkedin&phone=5551234'
```

### PUT /contact/:contactId

Update contact data.

```
curl -X PUT http://localhost:4000/contact/61fd79e80e869e2a7c1fee69 \
  -H 'Content-Type: application/x-www-form-urlencoded' \
  -d 'firstName=John2&lastName=Doe2&email=john2%40me.com&company=linkedin&phone=5559876'
```  

### DELETE /contact/:contactId

Delete a contact.

```
curl -X DELETE http://localhost:4000/contact/61fd78dc138bcb0e42d30559
```  

### GET /contact/:contactId

Retrieve the data of a given contact.

```
curl -X GET http://localhost:4000/contact/61fd78dc138bcb0e42d30559 
```

