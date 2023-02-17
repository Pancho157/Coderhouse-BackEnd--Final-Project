# Useful information

---

Products structure:

    {
        "_id": String,
        "title": String,
        "thumbnail": String,
        "category": String
        "price": Int,
        "stock": Int,
    }

- Hosting link: (replace for http://localhost:8080/)

  - https://backend-coderhouse-francisco-muniz.onrender.com

- It is a requirement that the queries be given the token as a query param (Given by login)

  - GET type queries are available for all types of users

  - POST, PUT, DELETE type queries are available only for admins

---

# Products quieries

---

## GET

---

        GET - All - http://localhost:8080/productos?token=${token}

- Returns an array with all products

      GET - By ID - http://localhost:8080/productos/:id?token=${token}

- Returns the requested product (MongoId)

        GET - By Category - http://localhost:8080/productos/:category/categoria?token=${token}

- Returns an array with all products that match category #CapitalsMatters

---

## POST

---

        POST - http://localhost:8080/productos?token=${token}

- Generates a new product

- Requires the following parameters within the body of the request

  - { "title": String, "thumbnail": String, "category": String, "price": Int, "stock": Int }

---

## PUT

---

        PUT - http://localhost:8080/productos?token=${token}

- Updates a product, as long as it is passed the product id and some property within the request body

  - Ejemplo: { "id": String, "title": String }

---

## DELETE

---

        PUT - http://localhost:8080/productos/:id?token=${token}

- Removes a product (as long as the specified product exists)

  - Success response: { "acknowledged": true, "deletedCount": 1 }
