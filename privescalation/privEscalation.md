# Privilege Escalation

The example demonstrates a privilege escalation vulnerability and how to exploit it.

## Steps to reproduce

1. Install all dependencies

    `$ npm install`

2. Start the **insecure.ts** server

    `$ npx ts-node insecure.ts`

3. In the browser, send a GET request

    ```
        http://localhost:3000/send-form
    ```

4. Try different UserIds and see which one gives you authorized access to change the role of that user.

## For you to do

Answer the following:

1. Briefly explain the potential vulnerabilities in **insecure.ts**
2. Briefly explain how a malicious attacker can exploit them.
3. Briefly explain the defensive techniques used in **secure.ts** to prevent the privilege escalation vulnerability?

ANSWERs: 

1. The insecure server is vulnerable to privilege escalation, which would allow a hacker to escalate their user account's role.
2. This could allow a hacker to obtain privileges and abilities they would not otherwise have, which they could use to sabotage the server or steal info.
3. The secure server uses session-based authentication, meaning a hacker who logs in as a basic user cannot upgrade their privileges within the same session.
