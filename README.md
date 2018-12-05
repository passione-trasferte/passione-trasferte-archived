# Passione Trasferte

Links:

* <https://www.thepolyglotdeveloper.com/2017/03/authenticate-a-golang-api-with-json-web-tokens/>
* <https://www.thepolyglotdeveloper.com/2017/03/authenticate-a-golang-api-with-json-web-tokens/>

```
$ curl -X POST \
  -d '{"username":"foobar", "password":"123456"}' \
  http://0.0.0.0:12345/authenticate
{"token":"eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXNzd29yZCI6IjEyMzQ1NiIsInVzZXJuYW1lIjoiZm9vYmFyIn0.IjpDuR7hcLp4Itd-zETHtSmp7g3-NRMLm6cxYo7IfLA"}

$ curl http://0.0.0.0:12345/protected?token=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXNzd29yZCI6IjEyMzQ1NiIsInVzZXJuYW1lIjoiZm9vYmFyIn0.IjpDuR7hcLp4Itd-zETHtSmp7g3-NRMLm6cxYo7IfLA

{"username":"foobar","password":"123456"}

curl http://0.0.0.0:12345/test -H "authorization: Bearer eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJwYXNzd29yZCI6IjEyMzQ1NiIsInVzZXJuYW1lIjoiZm9vYmFyIn0.IjpDuR7hcLp4Itd-zETHtSmp7g3-NRMLm6cxYo7IfLA"

{"username":"foobar","password":"123456"}
```
