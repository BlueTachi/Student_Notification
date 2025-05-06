# Agreement

Document the final problem definition and roles.

The main reason this is happening is because the Flask app may not have the route /notifications/send defined, or it may be misspelled or using the wrong HTTP method (e.g., GET instead of POST).

We think this:
The server runs file (Running on http://127.0.0.1:5001), so Flask is not crashing.  When wwe try to call /notifictions/send , it says "Not Found" which usually means:
- The endpoint doesn't exist.
- The URL is incorrect.
- The route is defined but using wrong method (e.g., we POST but the route only accepts GET).



Testing Tools and Techniques

POSTMAN - This is used to send test requests to the API (GET/POST). E.g., When you send a POST request to http://localhost:5001/notifications/send with test JSON data.

Curl - Command-line way to test endpoints. E.g., curl -X POST http://localhost:5001/notifications/send -d '{"user_id":"1","message":"Hi","type":"email"}' -H "Content-Type: application/json

docker-compose logs -  To view the service logs and see if the server responds or crashes. E.g.,docker-compose logs notification-service.

VS Code/ Code Editor - To check if the route is defined in app.py or main.py. E.g.,Look for: @app.route('/notifications/send', methods=['POST'])



Further details on line of code
curl -X POST - This line tells curl to use the POST method. POST is used when you want to send 
               data to a server (like submitting a form).

http://localhost:5001/notifications/send
              - This is the URL of the API endpoint you're calling.
              - localhost:5001 means you're calling a server running on your own machine on port
              5001.
              -/notifications/send is the specific function you're asking the server top run. In 
             this case, sending a notification.
             
-d '{"user_id":"1","message":"Hi","type":"email"}'
              -d stands for data - you're sending this JSON object as the body of the request.
              - This is the actual notification you're asking the server to send:
                  -"user_id": "1" - The ID of the user to notify.
                  -"message": "Hi" - The message your want to send
                  -"type": "email" - The type of notification (email,SMS, etc.)

-H "Content-Type: application/json"
              -H adds a header to the request
              -This header tells the server:
                  "I am sending data in JSON format."
              -If this left out, the server might not understand the data you're sending.

Team Roles

Thandolwethu Phakathi - Backend Developer
                      - He checks the Flask code and confirm the route /notifications/send is
                        correctly defined and uses the correct HTTP method.

Nhlanhla Shabangu/    - Testers
Thandazo Sithole      - We use Postman or Curl to test different cases (e.g., wrong URL,
                        missing fields) and confirm when errors happen.

Nhlanhla Shabangu     - DevOps
                      - Restart Docker containers when changes are made and fix warnings like                            the deprecated version and docker-compose.yml

Thandazo Sithole      - TeamLead
                      - She keeps track of findings, make decisions about fixing the root cause,                         and update the documentation.

