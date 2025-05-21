# UserAuth
I started the practical by installing the key packages express, pg, dotenv, bcryptjs. Depending on
the needs, jsonwebtoken, nodemailer, and various other options need to be added, along with
managing the dependencies with npm. The use of MVC framework helped us make a directory
structure that separates issues come up from the interactions between controllers, models, views,
and routes. Writing SQL queries within the function body. A table called users was created and
implemented in the PostgreSQL database through code in userModel.js model. These are the fields
found in the table: id, username, email address, password, role, is_verified, special codes sent by
email to validate the user. All the database connection code can be found in a separate db.js file.
kept safe by specifying them as environment variables.
The authController.js manages all the basic logic used for authentication. The user’s password is
personally hashed during registration (signup) thanks to bcryptjs, and that continues until
verification. token is produced using jsonwebtoken. In an email sent to users, a link is included
that needs to be clicked to verify their account using nodemailer; When the user clicks on the link,
their status gets updated to is_verified = true. The login It ensures that email addresses are valid
and that a user has valid credentials before they can continue. access. If a user doesn’t have their
login credentials, they can ask for a reset link via email, where they will receive it. address they
registered. Once they click the link, they will be directed to a page where they change their
password.
The landing page front end is created by using EJS templates. There are different options for login,
signup, forgetting your password, and resetting it. They are expressed with different types of
compositions. POST data to the proper data locations. It uses a basic CSS stylesheet to keep things
looking the same on all pages. an eye-pleasing layout for all of the views on the app. The app uses
the Express and certain authRoutes for handling its routes. Every Specific GET and POST requests
for the user are stated within the js file. Static file handling, session and cookie middleware, setting
up the view engine, and finally setting up the PostgreSQL table as the app is launched You can
ensure the database contains a user table by looking at the server configuration in the file app.js.
