# Tampering

This example demonstrates tampering through script injection.

## Steps to reproduce

1. Install all dependencies

    `npm install`

2. Start the **insecure.ts** server

    `npx ts-node insecure.ts`

3. In the browser, type a potentially malicious script in the name field of the form

    ```
        <script> document.body.innerHTML = "<a href='https://google.com'> Gotcha </a>"</script>
    ```

4. Do you see the potentially malicious hyperlink being injected into the form?

## For you to do

Answer the following:

1. Briefly explain the potential vulnerabilities in **insecure.ts**
2. Briefly explain how a malicious attacker can exploit them.
3. Briefly explain why **secure.ts** does not have the same vulnerabilties?

Answers: 

1. Though the first code has session authentication, it does not filter special HTML characters. By not 'sanitizing' input, the first code snippet is vulnerable to the injection of malicious scripts through common input fields.
2. A hacker could use this vulnerability to steal data, or redirect a user to a malicious website.
3. The escapeHTML function in the secure code sanitizes input by removing potentially dangerous characters with safer HTML alternatives(like & -> &amp;) This cleanses user input, making sure no malicious scripts are injected into the server.
