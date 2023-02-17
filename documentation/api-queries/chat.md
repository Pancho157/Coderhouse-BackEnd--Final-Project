# Useful information

---

- Token returned by login is used for query params on all the other endpoints

- Hosting link: (replace for http://localhost:8080/)

  - https://backend-coderhouse-francisco-muniz.onrender.com

---

# Chat quieries

---

## GET

---

        GET - http://localhost:8080/chat?token=${token}

- Returns the chat page (works with sockets)

          GET - http://localhost:8080/chat/:email?token=${token}

- Returns all messages sent by the requested email
