# Template

---

    ENV = "prod" # or "dev"
    PERS = "MONGO"

    ADMIN_EMAIL = ""

    NODEMAILER_EMAIL = ""
    NODEMAILER_PASS = ""

    MONGO_ATLAS_URL = ""
    MONGO_LOCAL_URL = ""

    SESSION_TIME = "300"

---

## Observations

---

- For nodemailer email is required some pre configuration on your email account

  - If config was not done, check the next link (minute 1:20): https://www.youtube.com/watch?v=KjheexBLY4A

- Only "MONGO" persistance is avaliable for now

- Dev environment uses local mongo server, so it's needed to run a local server

  - it also don't generate logs

- Local environment uses a DaaS (MongoDB Atlas) and generates a logs folder

- Session time sets the expiration time for tokens and it's value represents minutes
