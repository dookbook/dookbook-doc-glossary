TOPIC: CSRF
AUTHORS: Heather; hbloomer@mozilla.net; mdn:hbloomer
         Federico Culloca; federicoculloca@github.com; github:federicoculloca
         Andrew Pfeiffer; Andrew_Pfeiffer@mozilla.net; mdn:Andrew_Pfeiffer

# CSRF

**CSRF** (Cross-Site Request Forgery) is an attack that impersonates a trusted user and sends a
website unwanted commands. This can be done, for example, by including malicious parameters in a URL
behind a link that purports to go somewhere else:

```html
<img src="https://www.example.com/index.php?action=delete&id=123">
```

For users who have some permissions on `https://www.example.com`, the `<img>` element will execute
action on `https://www.example.com` without their noticed, even if the element is not at `https://www.example.com`.

There are many ways to prevent CSRF, such as implement RESTful API, add secure token, etc.

## Learn More

### General Knowledge

- [Cross-site request forgery](https://en.wikipedia.org/wiki/Cross-site%20request%20forgery) on Wikipedia
- [Prevention measures](https://www.owasp.org/index.php/Cross-Site_Request_Forgery_(CSRF)_Prevention_Cheat_Sheet)
- [MDN security tutorial](https://wiki.developer.mozilla.org/en-US/Learn/tutorial/Information_Security_Basics)
