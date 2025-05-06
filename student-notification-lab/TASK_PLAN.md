# Task Plan

Outline tasks, timeline, and responsibilities .

* Team : Thando , Nhlanhla, Thandazo


* Task list andd responsibilities 

Tasks :                                       Assugned TO   :              Estimated Time :

Inspect notification-service logs             Thandazo                      05/05  13:00 - 14:30 
Test API using curl/postman                   Nhlanhla                      05/05  13:00 - 14:30
Validates Flask routes and input              Thando                        05/05  13:00 - 14:30
Investigate port conflict issue               All                           06/05  09:00 - 11:00
Documents results and errors                  All                           06/05  09:00 - 11:00 
Final team review of findings                 All                           06/05  12:00 - 12:30


* Task List
  - Test retry logic for failed notification
  - Check redis configurations (is used as a queue or cache)
  - investigate port binding issue in notification-service
  - Validates JSON payload format in '/send-notification'
  - Ensure '/status' endpoint returns correct service status
  - Check docker container logs for runtime errors
  - Verify all services start correctly with 'docker-compose up'
  - Test API endpoint with invalid HTTP methods (e.g., GET on POST routes)
  - Document expected vs. actual responses for API testing
  - Clean up and rebuild container to verify stability 
 
*Goals for Execution 
- Ensure 'notification-service' runs correctly
- verify that '/status' and '/send- notification' endpoints responds as expected.
- Identify and document any bugs or missing features.
- submit clean and clear document with testing evidence.

* Tools to be Used
  - Visual Studio code (with docker extension)
  - Docker & Docker Compose
  - Postman and Curl for API testing
  - Github for Collaboration
 
  * Notes
    - Prioritize testing the system via Docker to avoid local port issues.
    - Each member should back up finding in 'problem-report.md' before merging.
    - Stick to time slots as best as possible to stay within the 2-hour window.




