+++
title = "Where To Store JWT Tokens"
description = "Explains the proper place to store JWT Tokens"
date = 2020-02-05
author = "Jonathan Greene"

+++## Introduction

Welcome my name is Jonathan Greene I am Full Stack Developer that focuses on building clean easily scalable code.

## Step 1. What is a JWT

The official site describes a JWT as the following.

```
JSON Web Token (JWT) is an open standard (RFC 7519)
that defines a compact and self-contained way for securely
transmitting information between parties as a JSON object.
This information can be verified and trusted because it is digitally signed.
JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.
```

What does this actually mean though?

By doing a little research we can come to understand that a JWT or JSON web token as it is called. Is a way to move information between parties in a secure way that protects that information and allows both parties to know they are dealing with the correct party.

### Step 2. Why don't we store JWT in local storage

A common practice for beginners is to store the JWT tokens in local store. The reason for this is because it allows for a universal place to grab the token for when you need it and its pretty simple to do. However it is not a very good idea and leaves you open to cross-site scripting (XSS) attacks. Tom Abbott explains in post Where to Store your JWTs – Cookies vs HTML5 Web Storage

```
Web Storage (localStorage/sessionStorage) is accessible through JavaScript on the same domain.
This means that any JavaScript running on your site will have access to web storage,
and because of this can be vulnerable to cross-site scripting (XSS) attacks.
XSS, in a nutshell, is a type of vulnerability where an attacker can inject
JavaScript that will run on your page. Basic XSS attacks attempt to inject
JavaScript through form inputs, where the attacker puts
<script>alert('You are Hacked');</script>
into a form to see if it is run by the browser and can be viewed by other users.

In regards to using 3rd party libraries and tools he also expands on it with the following:


Modern web apps include 3rd party JavaScript libraries for A/B testing, funnel/market analysis,
and ads. We use package managers like Bower to import other peoples’ code into our apps.

What if only one of the scripts you use is compromised?
Malicious JavaScript can be embedded on the page,
and Web Storage is compromised. These types of XSS attacks can get everyone’s
Web Storage that visits your site, without their knowledge.
This is probably why a bunch of organizations advise not to store
anything of value or trust any information in web storage.
This includes session identifiers and tokens.
```

### Step 3. Where is the right place to store JWT then

As it turns out when used with the `HttpOnly` cookie flag the JWT are not accessible through JavaScript. Setting the `Secure` cookie flag also guarantees the cookie is only sent over HTTPS.

While storing in cookies allows for another type of attack cross-site request forgery or CSRF this is prevented by using synchronized token patterns which all modern JavaScript frameworks support. The only real down side to this is Cross Origin Resource Sharing (CORS) issues but that is a topic for another day.

Thank you for reading

I hope this blog helps you to better understand and solve where to store your JWT for the best security.

References:

https://jwt.io/introduction/

https://stackoverflow.com/questions/44133536/is-it-safe-to-store-a-jwt-in-localstorage-with-reactjs

https://stormpath.com/blog/where-to-store-your-jwts-cookies-vs-html5-web-storage
