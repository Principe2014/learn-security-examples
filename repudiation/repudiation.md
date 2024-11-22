# Repudiation

The example demonstrates a vulnerability that can lead to repudiation by malicious users attempting to access the services provided by a server.

## Steps to reproduce

1. Install all dependencies

    `$ npm install`

2. Run the server __insecure.ts__.

3. Pretend to be a malicous user and interact with the services by sending requests from the browser.

4. Do you think your actions can be repudiated?

## For you to do

1. Briefly explain the vulnerability.
2. Briefly explain why the vulnerability is addressed in __secure.ts__.
3. Which design pattern is used in the secure version to address the vulnerability? Briefly explain how it works?

ANSWER: 

1. As the insecure server does not have any methods of identifying a user beyond the userid, it is nearly impossible to identify who is responsible for changes or determining who is accessing sensitive information. This could allow a hacker to corrupt data without being identified.
2. In secure.ts, authentication and authorization prevent a hacker from exploiting the server. Authentication ensures that the session is valid, while Authorization checks that a user has the right permissions to perform an action.
3. Session-based authentication is used to address the vulnerability. It works by creating a unique session on log in. It saves the session in the user's browser cookie, allowing it to authenticate subsequent requests. The session also expires after a fixed time, limiting the window a hacker might have to launch their attack.
