This is an example on how to create a basic API using FastAPI and integrate authenticate with JWT tokens.

Before testing create a .env file to place you token in.

![image](https://github.com/bbonser/Python/assets/26509652/0815027d-16ce-4b5f-923d-84345538fb57)

To generate a token, make sure OpenSSL is insalled on your local machine. Open a cmd prompt and type:

```openssl rand -hex 32```

This will outout a sting you can add to a variable called ```"SECRET_KEY"``` in your .env file

