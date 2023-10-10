
# Blitz 2
October 9, 2023

By: Andrew Mullen

- What was the purpose?
  - The URL Shortener is becoming increasingly popular and must be capable of ensuring that at least 14,000 people may access the program at any time.  We are responsible for deploying the new application version. The quality assurance engineer will send 14,000 requests to the server. The QA engineer will notify you of the results after testing your application.

- What happened during the blitz?
  - During the blitz, the QA engineer sent 14,000 requests to the production server on port 5000.
    - Test was run using stress-ng, a tool used to stress system components, and a bash script called blitz.sh
    - blitz.sh utilized the following
      -  Run the nice command and modify the priority of stress-ng on the server
      -  Make stress-ng run at the highest priority and utilize 2 CPUs
      -  Used the "&" special character to run the script in the background and to allow access to the terminal.
  - Our monitoring system, AWS CloudWatch, alerted us that our configured threshold of 20% was tripped and the server CPU usage spiked to 100%.
  - The test not only increased our server CPU usage to 100%, we dropped 710 of the 14,000 test connections to the server.
    
- What did you do to resolve the issue?
  - To resolve the issue, we created a more robust EC2 instance of our production server.
  - The new EC2 instance (T2.xlarge) has 4 vCPUs while the original (T2.medium) only has 2 vCPUs.
  - We are going to ask the QA engineer to run the test again on the updated server and record the results.
 

# Diagram:
Click to see the visual diagram [HERE](https://github.com/andmulLABS01/Blitz2/blob/main/Blitz2.drawio.png)
         
