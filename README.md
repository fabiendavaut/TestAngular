# TestAngular

##Subject: Implement a simple web application with a sign in.
 
###Detail: 
Implement a web application with a login page. The user have to set its username, password and company name.
 
When the user click on “sign in” button, a rest api of the backend is used to validate the credential (see below the detail of the rest api). 
 
If the credential is bad, a message “Failed to sign in! Please check your credentials and try again.” is displayed.
 
If the credential is good, the user will go to an empty main view.
 
###Technical constraint:
You have to use Angular2 or Angular4 with Webpack and bootstrap. 
 
###Constraint for styles:
There is no constraint, you can use any components and any design. 
 
###What we expect:
clean code
unit test(s)
end2end test(s)
 
###Available backend service:
In the backend, a stateless authentication is available with an api rest.
The parameters are:
username: the login of the user 
password: the password of the user
slug: the company name
 
Example with Curl:
 
```curl -X POST \
'https://develop-be.viadialog.com/uaa/oauth/token?username=secaadm&password=secaadm&grant_type=password&slug=seca' \
  -H 'accept: application/json' \
  -H 'authorization: Basic d2ViX2FwcDo=' \
  -H 'content-type: application/x-www-form-urlencoded'
 ```
If the credential is bad, the backend response is a status code 401.
If the credential is good, the backend response is a status code 200 with a JWT:
{"access_token":"eyJhbGciOiJSUzI1……...3b493-MPCparL3SVG_zSDdcrRvJgRdCAKw","expires_in":43199,"scope":"openid"}
This access_token is not necessary for that test. 
