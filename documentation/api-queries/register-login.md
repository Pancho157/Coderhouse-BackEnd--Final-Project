# Useful information

---

- Token returned by login is used for query params on all the other endpoints

- Hosting link: (replace for http://localhost:8080/)

  - https://backend-coderhouse-francisco-muniz.onrender.com

---

# Login-Register quieries

---

## GET

---

        GET - http://localhost:8080/

- Returns the view of the login and registration forms

          GET - http://localhost:8080/?token=${token}

- If a token is passed via query param to the "/" route, it is redirected to "/products" using the token passed earlier

---

## POST

---

        POST - http://localhost:8080/

- Requires the next body parameters: { "email": String, "password": Sting }

- Returns jwt token if user and password are correct

        POST - http://localhost:8080/register

- Requires the next body parameters:

  - { "name": String, "lastName": String, "password": String, "passwordDup": String, "email": String, "phone": Int, "rol": String, "deliveryAdress": String }

- Returns new user data if succeed
