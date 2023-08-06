# FastAPI Auth example

## This is an example on how to create a basic API using FastAPI and integrate authentication with JWT tokens.

Before testing create a .env file to place you token in.

![image](https://github.com/bbonser/Python/assets/26509652/0815027d-16ce-4b5f-923d-84345538fb57)

To generate a token, make sure OpenSSL is insalled on your local machine. Open a cmd prompt and type:

```cmd
openssl rand -hex 32
```

This will outout a sting you can add to a variable called ```"SECRET_KEY"``` in your .env file

To test this API locally, we'll need to generate a quick hash we cann add to the ```db``` on line 19 ```"hashed_password"```

Enter the following code at the very end of ```main.py```.

```python
pwd = get_password_hash("john123")
print(pwd)
```

Save it and make sure you're in the correct directy where ```main.py``` lives and then run:
```python
python main.py
```

Take the hashed password and enter it next to the ```"hased_password"``` entry on line 19.

Remove the code snippet from above and save the file.
In your IDE terminal run:
```python
uvicorn main:app --reload
```
and navigate to ```http://127.0.0.1:8000/docs``` where you can click ```Authenticate``` and test.
