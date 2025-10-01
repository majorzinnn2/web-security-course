# Web Security Lab Write-ups

Welcome to my collection of web security lab write-ups. This repository contains detailed walkthroughs and analyses of various web security vulnerabilities, based on labs from PortSwigger's Web Security Academy and other sources.

Each entry documents the process of identifying, exploiting, and remediating a specific vulnerability, complete with code snippets, HTTP requests, and explanations.

## Labs & Vulnerabilities

Here is a list of the vulnerabilities covered in this repository.

### Authentication & Access Control

*   **Forced OAuth Profile Linking**
    *   Exploits a flawed OAuth 2.0 implementation missing the `state` parameter to perform account takeover by linking the attacker's social media account to the victim's profile.

### Server-Side Vulnerabilities

*   **Information Disclosure in Version Control History**
    *   Discovers and exploits a publicly exposed `.git` directory to find a hardcoded password in the commit history.

*   **Insecure Deserialization**
    *   Leverages insecure deserialization of a PHP session cookie to manipulate application functionality and delete arbitrary files from the server.

*   **File Path Traversal**
    *   Bypasses a non-recursive filter for traversal sequences (`../`) to read sensitive system files, such as `/etc/passwd`.

*   **Server-Side Template Injection (SSTI)**
    *   Identifies a Handlebars template engine from an error message and uses a documented prototype pollution exploit to achieve remote code execution.

### Client-Side Vulnerabilities

*   **Multistep Clickjacking**
    *   Demonstrates a clickjacking attack that requires tricking a user into performing multiple actions on a hidden, overlaid iframe.

*   **Cross-Site Scripting (XSS) to Steal Cookies**
    *   Uses a stored XSS vulnerability in a comment field to inject a script that captures and exfiltrates a user's session cookie.

### Advanced Web Vulnerabilities

*   **CORS Vulnerability with Trusted Insecure Protocols**
    *   Exploits a misconfigured CORS policy that trusts subdomains over insecure protocols (HTTP) to steal a user's API key via an XSS payload.

*   **Manipulating the WebSocket Handshake**
    *   Exploits a WebSocket vulnerability by manipulating the handshake with an `X-Forwarded-For` header to bypass IP-based blocking and execute an XSS payload.

*   **Web Cache Poisoning with Multiple Headers**
    *   Poisons the web cache by manipulating unkeyed HTTP headers (`X-Forwarded-Host`) to cause the server to cache and serve malicious content to all users.
