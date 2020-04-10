# A RESTful API using the Express framework.

Use Postman, CURL or any other HTTP request agent to test your server. If you want to use Postman, download it from https://www.getpostman.com, then use its graphical user interface (GUI) to make requests. When using Postman for the POST request, make sure to select body, raw and JSON (application/json) settings to avoid a common mistake of not providing the right request payload format.

I recommend using CURL because the CURL commands are plain text, not GUI and they are easier to replicate from the text of this lab. The CURL tool is built into the most POSIX (macOS and Linux) distributions but it's also available for Windows via https://curl.haxx.se/download.html.

Here's the CURL code which you can execute to create a new account (POST), update it (PUT), retrieve it account (GET) and then delete it (DELETE).

//posts account data
curl -H "Content-Type: application/json" -X POST -d '{"balance": 100, "name":"checking"}' "http://localhost:3000/accounts"

//updates account data at a specified id
curl -H 'Content-Type: application/json' -X PUT -d '{"balance": 200, "name": "savings"}' "http://localhost:3000/accounts/0"

//gets account data
curl "http://localhost:3000/accounts"

//deletes account data and a specified id
curl -X DELETE "http://localhost:3000/accounts/0"
