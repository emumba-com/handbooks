NEVER EVER check-in secret information in your code. This includes but is not limited to
*  database username, password, IP address, port
*  API secret keys and access tokens
*  usernames and passwords

When in doubt if something is secret, ASK. 

# Backend

In a backend environment (Python or Node), create environment files like following:

Create a file `app.env` to define what environment variables are needed in the application. Only define the variables, do not set values. 
```
export OFFICE_365_APP_ID=
export OFFICE_365_APP_SECRET=
export OFFICE_365_APP_TENANT=
```
Create an `app.env.local` file and use this to setup environment variables in your development environment. For the love of God, do not commit this file. Add it into your `.gitignore` file. 
```
export OFFICE_365_APP_ID=abc
export OFFICE_365_APP_SECRET=123
export OFFICE_365_APP_TENANT=xyz
```
In your code, fetch values of secret variables from environment. 

# Frontend

In a front-end app, particularly ones created by `create-react-app` utility, you typically need two files:

- `.env.production.local`
- `.env.development.local`

In both of those files above, you can set values like thus:

```
REACT_APP_API_HOST=random-value
```

Do not forget to include both of those files in `.gitignore`: they must not be checked into the repo. To learn more about handling environment variables, consider reading this [article](https://medium.com/@tacomanator/environments-with-create-react-app-7b645312c09d).