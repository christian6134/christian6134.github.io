
![[Pasted image 20250710120355.png]]

**Scheme**

The **scheme** is the protocol used to access the website. The most common are **HTTP** (Hypertext Transfer Protocol) and **HTTPS** (Hypertext Transfer Protocol Secure). HTTPS is more secure because it encrypts the connection, which is why browsers and cyber security experts recommend it. Websites often enforce HTTPS for added protection.

**User**

Some URLs can include a user’s login details (usually a username) for sites that require authentication. This happens mostly in URLs that need credentials to access certain resources. However, it’s rare nowadays because putting login details in the URL isn’t very safe—it can expose sensitive information, which is a security risk.

**Host/Domain**

The **host** or **domain** is the most important part of the URL because it tells you which website you’re accessing. Every domain name has to be unique and is registered through domain registrars. From a security standpoint, look for domain names that appear almost like real ones but have small differences (this is called **typo squatting**). These fake domains are often used in phishing attacks to trick people into giving up sensitive info.

**Port**

The **port number** helps direct your browser to the right service on the web server. It’s like telling the server which doorway to use for communication. Port numbers range from 1 to 65,535, but the most common are **80** for HTTP and **443** for HTTPS.

**Path**

The **path** points to the specific file or page on the server that you’re trying to access. It’s like a roadmap that shows the browser where to go. Websites need to secure these paths to make sure only authorized users can access sensitive resources.

**Query String**

The **query string** is the part of the URL that starts with a question mark (?). It’s often used for things like search terms or form inputs. Since users can modify these query strings, it’s important to handle them securely to prevent attacks like **injections**, where malicious code could be added.

**Fragment**

The **fragment** starts with a hash symbol (#) and helps point to a specific section of a webpage—like jumping directly to a particular heading or table. Users can modify this too, so like with query strings, it’s important to check and clean up any data here to avoid issues like injection attacks.

### Exercises
-------------
**Which protocol provides encrypted communication to ensure secure data transmission between a web browser and a web server?**
- HTTP(S)



**What term describes the practice of registering domain names that are misspelt variations of popular websites to exploit user errors and potentially engage in fraudulent activities?**
- typo squatting



**What part of a URL is used to pass additional information, such as search terms or form inputs, to the web server?**
- query string