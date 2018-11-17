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

Vulnerability #1: __________________

Vulnerability #2: __________________


## Red

Vulnerability #1: __________________

Vulnerability #2: __________________


## Notes

Describe any challenges encountered while doing the work
