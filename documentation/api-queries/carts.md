# Useful information

---

- Token returned by login is used for query params on all the other endpoints

- User is validated via token, so it wont modify other user cart

- Hosting link: (replace for http://localhost:8080/)

  - https://backend-coderhouse-francisco-muniz.onrender.com

---

# Carts quieries

---

## GET

---

    GET - http://localhost:8080/carrito?token=${token}

- Returns the user cart info
  - Success response: { "cart": Array, "total": Int, "userEmail": String, "delivery": String }

---

## POST

---

    POST - http://localhost:8080/carrito?token=${token}

- Requires the next body parameters: { "productId": String }

- Adds product to cart / Increments product quantity

- Returns the following object: { "\_id": String, "user": String, "cart": Array, "deliveryAddress": String }

      POST - http://localhost:8080/carrito?token=${token}

- Only requires the token

- Generates new purchase order, sends email to admin and empties user cart

---

## DELETE

---

    DELETE - http://localhost:8080/carrito?token=${token}

- Requires the next body parameters: { "productId": String }

- Reduces product quantity

- Returns the following object: { "\_id": String, "user": String, "cart": Array, "deliveryAddress": String }

        DELETE - http://localhost:8080/carrito/:productId?token=${token}

- Only requires the productId and the token params

- Delete product from cart

- Returns the following object: { "\_id": String, "user": String, "cart": Array, "deliveryAddress": String }
