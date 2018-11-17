# Project 8 - Pentesting Live Targets

Time spent: 5 hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.

The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each version of the site has been given two of the six vulnerabilities. (In other words, all six of the exploits should be assignable to one of the sites.)

## Blue

Vulnerability #1 - SQL Injection (SQLi):  <br />
* In "salesperson" page, attackers can perform a time delay attack to the database by typing salesperson.php?id=1' or sleep(5)=1--' 
GIF Walkthrough: <br />
<img src="https://github.com/edwin0108/WebSecurity_Week8/blob/master/blue_SQLATTACK.gif" width="700">

Vulnerability #2 -  Session Hijacking/Fixation:  <br />
* Since all websites within the blue side are sharing the same session id for login, attackers can get the session id after login and reuse the session id on other browser as logged in user.
GIF Walkthrough: <br />
<img src="https://github.com/edwin0108/WebSecurity_Week8/blob/master/blue_SESSION.gif" width="700">

## Green

Vulnerability #1 - Username Enumeration: <br />
* The green site expose the correctness of the user name, letting attackers can brute force all the combination of the user info stores in this site. For instances:
     - If the username is accurate, with the user name pperson
        **Log in was unsuccessful**
     - If the username is not a user,
        *Log in was unsuccessful*
GIF Walkthrough: <br />
<img src="https://github.com/edwin0108/WebSecurity_Week8/blob/master/green_USERNAME_EM.gif" width="700">

Vulnerability #2 - Cross-Site Scripting (XSS): <br />
* Under the contact option, the feedback textbox is allow to type in a script, attackers can use this vulnerability and perform advance hacking with this, in this example I just entered \<script\>alert('You have been hacked!');\</script\> <br />
GIF Walkthrough: <br />
<img src="https://github.com/edwin0108/WebSecurity_Week8/blob/master/green_XSS.gif" width="700">

## Red

Vulnerability #1 - Insecure Direct Object Reference (IDOR): <br />
* Under the salesperson page: https://35.184.88.145/red/public/salesperson.php?id=X, I can change X to any id that is exist, after that I can change "red" to some other site such as "green" or "blue", but these are private page and should not be shared across different sites. Therefore a protect route is needed.
GIF Walkthrough: <br />
<img src="https://github.com/edwin0108/WebSecurity_Week8/blob/master/red_IDOR.gif" width="700">

Vulnerability #2 -  Cross-Site Request Forgery (CSRF)
* Red site does not required a CSRF token to perform any modification within user's information. After attacker login as admin, they can  edit the user's information.
GIF Walkthrough: <br />
<img src="https://github.com/edwin0108/WebSecurity_Week8/blob/master/red_CSRF.gif" width="700">

