TOPIC: Cross-site Scripting
AUTHORS: larson reever; larsonreever@github.com; github:larsonreever
         Spencer Corwin; spencercorwin@icloud.com; github:spencercorwin
         Heather; hbloomer@mozilla.net; mdn:hbloomer
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer
         Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Chris Anderson; chrisAnderson@mozilla.net; mdn:chrisAnderson
         Jérémie Patonnier; Jeremie@mozilla.net; mdn:Jeremie
         Ajinkya Patil; ajinkya_p@mozilla.net; mdn:ajinkya_p

# Cross-site Scripting

Cross-site scripting (XSS) is a security exploit which allows an attacker to inject into a website
malicious client-side code. This code is executed by the victims and lets the attackers bypass access
controls and impersonate users. According to the Open Web Application Security Project,
XSS was the
[seventh most common Web app vulnerability](https://www.owasp.org/images/7/72/OWASP_Top_10-2017_%28en%29.pdf.pdf)
in 2017.

These attacks succeed if the Web app does not employ enough validation or encoding. The user's
browser cannot detect the malicious script is untrustworthy, and so gives it access to any cookies,
session tokens, or other sensitive site-specific information, or lets the malicious script
rewrite the HTML content.

Cross-site scripting attacks usually occur when 1) data enters a Web app through an untrusted source
(most often a Web request) or 2) dynamic content is sent to a Web user without being validated for
malicious content.

The malicious content often includes JavaScript, but sometimes HTML, Flash, or any other code the
browser can execute. The variety of attacks based on XSS is almost limitless, but they commonly
include transmitting private data like cookies or other session information to the attacker,
redirecting the victim to a webpage controlled by the attacker, or performing other malicious
operations on the user's machine under the guise of the vulnerable site.

XSS attacks can be put into three categories: stored (also called persistent), reflected (also
called non-persistent), or DOM-based.

## Stored XSS Attacks

The injected script is stored permanently on the target servers. The victim then retrieves this
malicious script from the server when the browser sends a request for data.

## Reflected XSS Attacks

When a user is tricked into clicking a malicious link, submitting a specially crafted form, or
browsing to a malicious site, the injected code travels to the vulnerable website. The Web server
reflects the injected script back to the user's browser, such as in an error message, search result,
or any other response that includes data sent to the server as part of the request.
The browser executes the code because it assumes the response is from a "trusted" server which the
user has already interacted with.

## DOM-based XSS Attacks

The payload is executed as a result of modifying the DOM environment (in the victim’s browser) used
by the original client-side script. That is, the page itself does not change, but the client side
code contained in the page runs in an unexpected manner because of the malicious modifications
to the DOM environment.

## Learn More

### General Knowledge

- [Cross-site Scripting](https://en.wikipedia.org/wiki/Cross-site%20scripting) on Wikipedia
- [Cross-site Scripting on OWASP](https://www.owasp.org/index.php/XSS)
- [Another article about Cross-site scripting](http://www.acunetix.com/blog/web-security-zone/articles/dom-xss-explained/)
- [XSS Attack – Exploit & Protection](https://secure.wphackedhelp.com/blog/wordpress-xss-attack/)
