# Problem Report
Describe the observed issue in the notification service.

## Task 1: Define the Problem (PA0101 / IAC0101)
## What’s not working? 
The expected API endpoint `/api/notify` is not working as expected.
When a POST request is sent to http://localhost:5001/api/notify, the response is:
404 Not Found.

## When does it fail?
It fails when attempting to send a POST request to the notification-service API 
endpoint at:http://localhost:5001/api/notify
The failure occurs after the service starts successfully in Docker, and the user
tries to test the API using curl amd postman, VS code terminal (Invoke-RestMethod)

## Error messages or symptoms
the following error message is returned:
404 Not Found
The requested URL was not found on the server. If you entered the URL manually please check your spelling and try again.

## Task 2
Discussion Summary - Stake holders meeting

1. Registrar Thandolwethu: "Our concern is that students aren't receiving notifications. Is the notification API even functional?"
2. Developer Thandazo: "I tested the /api/notify endpoint with curl/PowerShell, but it returns a 404 Not Found error. The service runs on port 5001, but the endpoint doesn't seem to exist."
3. Team Lead Nhlanhla:"Let's double-check the Flask app in notification-service/app.py. Maybe the route is different — like /notify instead of /api/notify — or uses GET instead of POST."

After the discussion with the stakeholders, this is what was agreed upon:

1. Open and inspect notification-service/app.py.
2. Confirm the correct route and method.
3. Compare actual route with the one we are testing in Postman and curl.
4. If the route is missing, define it or correct the test URL.






