# Securing Software

Note: Nazu

Here's a brief summary of the main topics covered in the CS50 cyber security lecture on Securing Software:

## SQL Injection (SQLi)

* SQLi is a type of injection attack where an attacker injects malicious SQL code into a web application's database.
* Attackers can use SQLi to steal sensitive data, modify data, or even take control of the database.
* Prevention methods include:
	+ Using prepared statements (parameterized queries)
	+ Validating user input
	+ Limiting database privileges

## Cross-Site Scripting (XSS)

* XSS is a type of attack where an attacker injects malicious JavaScript code into a web page.
* Attackers can use XSS to steal sensitive data, hijack user sessions, or take control of the user's browser.
* Prevention methods include:
	+ Validating user input
	+ Encoding special characters
	+ Using Content Security Policy (CSP)

For more: owasp top 10

## Phishing

* Phishing is a type of social engineering attack where attackers trick users into revealing sensitive information (e.g., passwords, credit card numbers).
* Prevention methods include:
	+ Educating users about phishing attacks
	+ Implementing two-factor authentication
	+ Using secure communication protocols (e.g., HTTPS)
