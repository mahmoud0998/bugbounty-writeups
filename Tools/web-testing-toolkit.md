# Web Application Testing Tools

This document outlines the core tools I use during web application security testing, with a strong focus on manual analysis, request manipulation, and vulnerability discovery.

---

## Burp Suite
Burp Suite is the core tool in my web application testing workflow and is primarily used for deep HTTP request and response analysis.

**Usage:**
- Intercepting, modifying, and replaying HTTP requests and responses
- Analyzing authentication and session handling mechanisms
- Testing authorization logic such as IDOR and broken access control
- Manipulating headers, parameters, cookies, and tokens
- Comparing authorized vs unauthorized requests to identify privilege escalation issues
- Supporting manual testing of CSRF, business logic flaws, and workflow bypasses

Burp Suite is my primary tool for understanding how the application processes user input and enforces access controls.

---

## Subfinder
Used to enumerate subdomains associated with a target domain as part of the reconnaissance phase.  
Helps expand the attack surface by discovering hidden or forgotten subdomains.

---

## WaybackURLs
Used to collect historical URLs from archived sources.  
Very useful for discovering old endpoints, deprecated parameters, and legacy functionalities that may still be accessible.

---

## httpx
Used to probe live hosts and endpoints efficiently.  
Helps identify reachable services, HTTP status codes, redirects, and technology fingerprints during reconnaissance.

---

## ParamSpider
Used to extract parameters from URLs automatically.  
Useful for identifying potential injection points and parameters suitable for vulnerabilities such as XSS, SQLi, and IDOR.

---

## ffuf
Used for content discovery and fuzzing.  
Commonly applied to:
- Discover hidden directories and files
- Bruteforce parameters and endpoints
- Test access control and authorization boundaries

---

## Nuclei
Used for automated vulnerability scanning with templates.  
Findings are always manually verified to reduce false positives and better understand the root cause of the issue.

---

## Arjun
Used to discover hidden or undocumented HTTP parameters.  
Helpful when testing APIs and web applications that rely heavily on backend parameters.

---

## Hashcat
Used for offline hash cracking scenarios only.  
Applied in specific cases such as analyzing encoded or hashed tokens (e.g., JWT-related components) when legally permitted.

---

## grep
Used for fast pattern searching within output files, logs, and responses.  
Helps identify sensitive keywords, parameters, or indicators during analysis.

---

## Dalfox
Used specifically for automated and semi-manual XSS testing.  
Supports detecting reflected and DOM-based XSS issues efficiently.

---

## Mantra
Used to analyze JavaScript files for exposed secrets or sensitive information.  
Helpful for identifying API keys, endpoints, and misconfigurations leaked within frontend JavaScript code.

---

## Disclaimer
All testing activities are performed strictly on authorized environments, including labs, CTF platforms, and permitted targets only.
