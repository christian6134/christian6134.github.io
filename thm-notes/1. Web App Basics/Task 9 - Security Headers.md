
HTTP Security Headers:
- Improve **overall security of web application** by providing mitigations against Cross-Site Scripting (XSS)

**Digging Deeper**
- Content-Security Policy (CSP)
- Strict Transport Security (HSTS)
- X Content Type Options
- Referrer Policy


### **Content-Security-Policy (CSP)**
-----
CSP Header:
- Additional security layer that mitigates **Cross-Site-Scripting (XSS)**
- Malicious Code hosted on a **separate site** injected into the vulnerable site
- Provides a means to say what domains or sources are considered **safe**

Example; CSP Header:
- `Content-Security-Policy: default-src 'self' ; scrip-src 'self' https://cdn.tryhackme.com; style-src'self`

(1) default-src
- specifies the default policy of self -> only the current website

(2) script-src
- specifies the policy for where scrips can be **loaded from**, which is self along with scripts hosted on `https://cdn.tryhackme.com`

(3) style-src
- specifies policy for where **CSS** style sheets can be loaded from (self)

------------------------



### **Strict-Transport-Security (HSTS)**
----
HSTS Header:
- Ensures web browser always connect over **HTTPS**

Example; HSTS Header:
- `Strict-Transport-Security: max-age=600000; includeSubDomins; preload`

(1) max-age:
- Expiry time in seconds for this setting

(2) includeSubDomains:
- Optional Setting -> Instructs browser to apply this setting on all **subdomains**

(3) preload:
- Optional Setting -> Allows website to be included in preloaded lists
- Browsers use preloaded lists to enforce HSTS before having to visit the website



### X-Content-Type-Options
--------------------------------------------
The X-Content-Type-Options header can be used to instruct browsers not to guess the MIME time of a resource but only use the Content-Type header. Here’s an example:

`X-Content-Type-Options: nosniff`

Here’s a breakdown of the X-Content-Type-Options header by directives:

- **nosniff**  
    - This directive instructs the browser not to sniff or guess the MIME type.



### **Referrer Policy**
-----------------------
Refferer-Policy-Header:
- Controls amount of information sent to the destination web server when a user is redirected from the source web server e.g. **clicking hyperlinks**
- Allows a web admin to control what is shared

Examples:
- `Referrer-Policy: no-referrer`: Completely disables any information being sent about the referrer
- `same-origin`: Only sends referrer information when destination is apart of the same origin.
- `strict-origin`: Sends referrer as origin when the protocol stays the same. E.g a referrer is sent when an HTTPS connection goes to another HTTPS connection
- `strict-origin-when-cross-origin`: similar, but for same origin requests
