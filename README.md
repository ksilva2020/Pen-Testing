# Pen-Testing
Pen Testing of Live Targets
# Project 9 - Pentesting Live Targets

Time spent: **10** hours spent in total

> Objective: Identify vulnerabilities in three different versions of the Globitek website: blue, green, and red.
The six possible exploits are:
* Username Enumeration
* Insecure Direct Object Reference (IDOR)
* SQL Injection (SQLi)
* Cross-Site Scripting (XSS)
* Cross-Site Request Forgery (CSRF)
* Session Hijacking/Fixation

Each color is vulnerable to only 2 of the 6 possible exploits. First discover which color has the specific vulnerability, then write a short description of how to exploit it, and finally demonstrate it using screenshots compiled into a GIF.

## A) Blue
Vulnerability #1: SQL Injection
Description:
Modified the URL by injecting '1' or '1'='1' after the Id. 
<img src="blue-vuln1.gif">


https://user-images.githubusercontent.com/98780052/203152825-62c5c34b-9692-49b8-99ee-f63b5cd0ae2e.mp4


Vulnerability #2: Session Fixation
Got attacker’s ID by using the tool from instructions
Inserted the session ID in the Request in Burp
Forwarded to target




https://user-images.githubusercontent.com/98780052/203152995-dd9568b8-b1ed-4aab-b0bb-684284fbd37b.mp4


## B) Green
Vulnerability #1: Username Enumeration
Description:
-When trying different usernames, the failed messages are different when the user name exists from when it doesn’t. 
-When the username was existent, the warning was written in bold letters.
 -When analyzing the element, we see tow words that result from the failed logging: the one for the existent username message says “failure”; while the one with the nonexistent username says “failed”. 
<img src="green-vuln1.gif">




https://user-images.githubusercontent.com/98780052/203153070-070b5de7-f0b6-444c-ad67-8c10d9eb8f51.mp4


<img src="green-vuln1.2.gif">




![green-vuln1 2](https://user-images.githubusercontent.com/98780052/203153089-912dcd4b-e15c-4fa4-af1b-c0247a4e8ad9.png)


Vulnerability #2: Cross Site Scripting (XSS)
-Entered fake username, fake email address, injected a script in the comments
-When I openned the Feedback as a legitimate user, the script ran
<img src="green-vuln2.gif">vvmm




https://user-images.githubusercontent.com/98780052/203153119-f25951df-c5f9-4cb6-b690-1dfb67d97021.mp4


## C) Red
Vulnerability #1: IDOR
Description:
Clicking on the element of the pages, “Salesperson Details” URL shows an ID number. 
Using the Intruder feature of Burp, I manipulated the numbers to find information on the salespeople. 
<img src="red-vuln1.gif">




https://user-images.githubusercontent.com/98780052/203153148-71354afa-cc28-4683-9d65-07a803ef25e8.mp4




## Notes

To find most vulnerablities was difficult except for the IDOR. However, when I found similar cases it all became suddenly obvious. 

## Gifs created with Camtasia (Camtasia.com)
