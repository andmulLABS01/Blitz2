
# Blitz 2
October 9, 2023

By: Andrew Mullen

- What was the purpose?
  - The URL Shortener is becoming increasingly popular, and you must ensure that at least 14,000 people may access the program at any time.  We are responsible for deploying the new application version. The quality assurance engineer will send 14,000 requests to the server. The QA engineer will notify you of the results after testing your application.

- What happened during the blitz?
  - During the blitz, the test server simulated increased user traffic to the server.
  - This increased the latency to the server to 40 milliseconds.
    
- What did you do to resolve the issue?
  - To resolve the issue we created a CDN using AWS CloudFront.
  - Other options would be:
    - Optimize application performance
    - Select the right ECT Instance Type
    

A summary of the QA's activities
What steps were taken to remediation the issue (if there were any) 
What was the value of the test results before and after
Include screenshots of any monitoring or log information that helped you discover the issue (if there were any)
      
